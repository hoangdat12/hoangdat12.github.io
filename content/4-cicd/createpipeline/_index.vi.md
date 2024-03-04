---
title: 'Tạo Jenkins Pipeline'
date: '`r Sys.Date()`'
weight: 2
chapter: false
pre: ' <b> 4.2 </b> '
---

1. Truy cập vào **Jenkins Dashboard** và chọn **New item**

![New item](/images/4.cicd/4.2-newitem.png)

2. Tạo mới **Pipeline**

   - Nhập **Item name**
   - Chọn **Pipeline**
   - Click **Next**

![Create new pipeline](/images/4.cicd/4.2-newitem.png)

3. Cấu hình **Pipeline**

   - Chọn **Github project**
   - Dán link **Github**
   - Chọn **Github hook trigger for GITScm polling**

![Setup Pipeline](/images/4.cicd/4.2-setuppipeline.png)

- Ở **Pipeline** chọn **Pipeline script** và dán đoạn code dưới vào

```bash
pipeline {
    agent any

    environment {
        USER_APP_NAME = "user-api"
        AUTH_APP_NAME = "auth-api"
        GATEWAY_APP_NAME = "api-gateway"
        RELEASE = "1.0.0"
        DOCKER_USER = "hoangdat12" # Đổi thành Username của bạn
        DOCKER_PASS = "docker-crd"
        USER_IMAGE = "${DOCKER_USER}/${USER_APP_NAME}"
        AUTH_IMAGE = "${DOCKER_USER}/${AUTH_APP_NAME}"
        GATEWAY_IMAGE = "${DOCKER_USER}/${GATEWAY_APP_NAME}"
        IMAGE_TAG = "${RELEASE}-${BUILD_NUMBER}"
    }

    stages {
        stage("Checkout SCM") {
            steps {
                script {
                    checkout scmGit(branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[credentialsId: 'github-crd', url: 'https://github.com/hoangdat12/eks-workshop.git']])
                }
            }
        }

        stage("Git Checkout") {
            steps {
                git branch: 'main', credentialsId: 'gtihub-crd', url: 'https://github.com/hoangdat12/eks-workshop'
            }
        }

        stage("Build & Deploy Docker Image") {
            steps {
                script {

                    // Authenticate with Docker registry
                    withCredentials([usernamePassword(credentialsId: 'docker-crd', passwordVariable: 'DOCKER_PASS', usernameVariable: 'DOCKER_USER')]) {
                        // Build and push Docker image
                        sh "echo \$DOCKER_PASS | docker login -u \$DOCKER_USER --password-stdin"

                        // Build and push Docker image
                        sh "docker build -t ${USER_IMAGE}:${IMAGE_TAG} -f users-api/Dockerfile users-api"
                        sh "docker push ${USER_IMAGE}:${IMAGE_TAG}"

                        sh "docker build -t ${AUTH_IMAGE}:${IMAGE_TAG} -f auth-api/Dockerfile auth-api"
                        sh "docker push ${AUTH_IMAGE}:${IMAGE_TAG}"

                        sh "docker build -t ${GATEWAY_IMAGE}:${IMAGE_TAG} -f api-gateway/Dockerfile api-gateway"
                        sh "docker push ${GATEWAY_IMAGE}:${IMAGE_TAG}"
                    }
                }
            }
        }

         stage('Deploying Application To EKS') {
            steps{
                script{
                    // Config EKS
                    dir("kubernetes") {
                        sh "aws eks update-kubeconfig --name eks-cluster"
                        sh "kubectl apply -f api-gateway/Deployment.yaml -f auth-api/Deployment.yaml -f user-api/Deployment.yaml"
                        sh "kubectl apply -f api-gateway/Service.yaml -f auth-api/Service.yaml -f user-api/Service.yaml"
                    }
                }
            }
        }
    }
}
```

4. Tạo **Github webhook**

- Truy cập vào [Github](https://github.com/) và vào project của chúng ta
- Chọn **Setting**

![Github webhook](/images/4.cicd/4.2-createwebhook.png)

- Chọn Webhook
- Dán link `https://54.205.96.61:8080/github-webhook/`, đổi địa chỉ Public IPv4 máy chủ EC2 của bạn
- Chọn **Let me select individual events**

![Config webhook](/images/4.cicd/4.2-configwebhook.png)

- Chọn **Pull requests** và **Pushes**
- Chọn **Active**
- Click **Save**

![Comple](/images/4.cicd/4.2-completewebhook.png)
