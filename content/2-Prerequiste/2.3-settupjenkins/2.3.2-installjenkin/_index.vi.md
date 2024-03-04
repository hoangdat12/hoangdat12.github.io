---
title: 'Tải Jenkins'
date: '`r Sys.Date()`'
weight: 2
chapter: false
pre: ' <b> 2.3.2 </b> '
---

1. Tải **Jenkins**

- Sao chép câu lênh và dán vào **Jenkins Instance**

```bash
sudo yum update -y
sudo wget -O /etc/yum.repos.d/jenkins.repo \
    https://pkg.jenkins.io/redhat-stable/jenkins.repo
sudo rpm --import https://pkg.jenkins.io/redhat-stable/jenkins.io-2023.key
sudo yum upgrade
sudo dnf install java-17-amazon-corretto -y
sudo yum install jenkins -y
sudo systemctl enable jenkins
sudo systemctl start jenkins
```

2. Truy cập vào [AWS EC2 Console](https://ap-southeast-1.console.aws.amazon.com/ec2/home?region=ap-southeast-1)

   - Chọn **Instance**
   - Chọn **Jenkins-Instance**
   - Coppy **Public IPv4 address**

![Public IPv4](/images/2.prerequisite/2.3.1-publicip.png)

3. Truy cập vào **Public IPv4** với port **8080** ở Browser

![Access Jenkin](/images/2.prerequisite/2.3.1-accessjenkins.png)

4. Ở trong **Jenkins Instance**, chúng ta cần thực thi command `sudo cat /var/lib/jenkins/secrets/initialAdminPassword` và sao chép **Password**

![Get password](/images/2.prerequisite/2.3.1-getjenkinspassword.png)

5. Dán **Password** vừa mới sao chép vào **Jenkins Browser** và click **Continue**

![Unlock Jenkins](/images/2.prerequisite/2.3.1-unlockjenkins.png)

6. Ở bước **Getting started**
   - Chọn **Install suggested plugins**

![Getting started](/images/2.prerequisite/2.3.1-gettingstarted.png)

7. Ở bước **Craete First Admin User**
   - Điền đầy đủ thông tin
   - Chọn **Save and Continue**

![Craete First Admin User](/images/2.prerequisite/2.3.2-createuser.png)

8. Giữ nguyên mặc định ở những bước sau
