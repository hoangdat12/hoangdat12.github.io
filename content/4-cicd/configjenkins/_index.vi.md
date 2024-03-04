---
title: 'Cấu hình Jenkins browser'
date: '`r Sys.Date()`'
weight: 1
chapter: false
pre: ' <b> 4.1 </b> '
---

1. Tạo **Github Access Token**

- Truy cập vào [Github Setting](https://github.com/settings/profile) -> Scroll xuống chọn **Developing Setting** -> Chọn **Personal access token** và click **Token (classic)**
- Chọn **Generate new token** và click **Generate new token (classic)**

![Github Access Token](/images/4.cicd/4.1-generategittoken.png)

- Nhập `jenkins-access`
- Tích chọn tất cả các button ở dưới
- Click **Generate token**

{{%notice tip%}}
Để hiểu hơn về cấu hình Github Access Token, chúng ta có thể tham khảo [tại đây](https://docs.cloudbees.com/docs/cloudbees-ci-kb/latest/client-and-managed-controllers/github-user-scopes-and-organization-permissions-overview)
{{%/notice%}}

![Generate token](/images/4.cicd/4.1-generatetoken.png)

- Coppy **Token** vừa được tạo
- Truy cập **Jenkins Browser**
- Ở trang **Dashboard** chọn **Manages Jenkins**

![Manage Jenkins](/images/4.cicd/4.1-managejenkins.png)

- Chọn **Credentials**

![Credentials Jenkins](/images/4.cicd/4.1-credentials.png)

- Click **globals**
- Click **Add credentials**
- Chọn **Kind** là **Username with password**
- Nhập Github **username** và **token** vừa mới tạo
- Nhập ID `jenkins-git`
- Chọn **Create**

![Create Github Token](/images/4.cicd/4.1-creategittoken.png)

2. Tạo **Docker hub Access Token**

- Truy cập vào [Docker hub](https://hub.docker.com/) -> Chọn **My Account**
- Chọn **Security**
- Chon **New Access Token**

![Create Docker Access Token](/images/4.cicd/4.1-createdockertoken.png)

- Nhập **Access token Description**
- Click **Generate**

![Generate Docker Token](/images/4.cicd/4.1-generatedockertoken.png)

- Coppy **Docker Access Token** và thực hiện tương tự tạo **Github Access Token** trong Jenkins
- Truy cập **Jenkins Browser**
- Ở trang **Dashboard** chọn **Manages Jenkins**
- Chọn **Credentials**
- Click **globals**
- Click **Add credentials**
- Chọn **Kind** là **Username with password**
- Nhập Docker **username** và **token** vừa mới tạo
- Nhập ID `docker-crd`
- Chọn **Create**

![Complete Generate Docker Token](/images/4.cicd/4.1-completegeneratedockertoken.png)
