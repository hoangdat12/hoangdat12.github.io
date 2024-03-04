---
title: 'Configure Jenkins browser'
date: '`r Sys.Date()`'
weight: 1
chapter: false
pre: ' <b> 4.1 </b> '
---

1. Create **Github Access Token**

- Go to the [Github Setting](https://github.com/settings/profile) -> Scroll down and select **Developing Setting** -> Select **Personal access token** and click **Token (classic)**
- Select **Generate new token** and click **Generate new token (classic)**

![Github Access Token](/images/4.cicd/4.1-generategittoken.png)

- Enter `jenkins-access`
- Check all the buttons below
- Click **Generate token**

{{%notice tip%}}
To better understand Github Access Token configuration, we can refer to [here](https://docs.cloudbees.com/docs/cloudbees-ci-kb/latest/client-and-managed-controllers/github-user-scopes-and-organization-permissions-overview)
{{%/notice%}}

![Generate token](/images/4.cicd/4.1-generatetoken.png)

- Coppy **Token** was created
- Go to the **Jenkins Browser**
- At **Dashboard** select **Manages Jenkins**

![Manage Jenkins](/images/4.cicd/4.1-managejenkins.png)

- Select **Credentials**

![Credentials Jenkins](/images/4.cicd/4.1-credentials.png)

- Click **globals**
- Click **Add credentials**
- Select **Kind** is **Username with password**
- Enter Github **username** and **token** was created
- Enter ID `jenkins-git`
- Select **Create**

![Create Github Token](/images/4.cicd/4.1-creategittoken.png)

2. Create **Docker hub Access Token**

- Go to the [Docker hub](https://hub.docker.com/) -> Select **My Account**
- Select **Security**
- Select **New Access Token**

![Create Docker Access Token](/images/4.cicd/4.1-createdockertoken.png)

- Enter **Access token Description**
- Click **Generate**

![Generate Docker Token](/images/4.cicd/4.1-generatedockertoken.png)

- Copy **Docker Access Token** and do the same to create **Github Access Token** in Jenkins
- Go to the **Jenkins Browser**
- At **Dashboard** select **Manages Jenkins**
- Select **Credentials**
- Click **globals**
- Click **Add credentials**
- Select **Kind** is **Username with password**
- Nhập Docker **username** and **token** was created
- Enter ID `docker-crd`
- Select **Create**

![Complete Generate Docker Token](/images/4.cicd/4.1-completegeneratedockertoken.png)
