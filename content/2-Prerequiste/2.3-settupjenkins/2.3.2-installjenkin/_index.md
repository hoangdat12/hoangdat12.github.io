---
title: 'Install Jenkins'
date: '`r Sys.Date()`'
weight: 2
chapter: false
pre: ' <b> 2.3.2 </b> '
---

1. Tải **Jenkins**

- Copy the command and paste it into **Jenkins Instance**

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

2. Go to the [AWS EC2 Console](https://ap-southeast-1.console.aws.amazon.com/ec2/home?region=ap-southeast-1)

   - Select **Instance**
   - Select **Jenkins-Instance**
   - Coppy **Public IPv4 address**

![Public IPv4](/images/2.prerequisite/2.3.1-publicip.png)

3. Access to **Public IPv4** with port **8080** at Browser

![Access Jenkin](/images/2.prerequisite/2.3.1-accessjenkins.png)

4. In **Jenkins Instance**, we need execute command `sudo cat /var/lib/jenkins/secrets/initialAdminPassword` and coppy **Password**

![Get password](/images/2.prerequisite/2.3.1-getjenkinspassword.png)

5. Pass the **Password** that we just coppy into **Jenkins Browser** and click **Continue**

![Unlock Jenkins](/images/2.prerequisite/2.3.1-unlockjenkins.png)

6. In **Getting started** step
   - Select **Install suggested plugins**

![Getting started](/images/2.prerequisite/2.3.1-gettingstarted.png)
