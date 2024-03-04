---
title: 'Install kubectl'
date: '`r Sys.Date()`'
weight: 1
chapter: false
pre: ' <b> 2.3.1 </b> '
---

1. Go to the [giao diện quản trị của dịch vụ EC2](https://ap-southeast-1.console.aws.amazon.com/ec2/home?region=ap-southeast-1).

   - Select **Instance**.
   - Select **Jenkins-Instance**
   - Click **Connect**

![Connect](/images/2.prerequisite/2.3.1-connectEc2.png)

2. In **Connect** Console, we need to follow the instructions to access **Jenkins-Instance**

3. Install **kubectl**

- Coppy and execute command into **Jenkins Instance** that we just accessed

```bash
curl -LO "https://dl.k8s.io/release/$(curl -L -s https://dl.k8s.io/release/stable.txt)/bin/linux/amd64/kubectl"
curl -LO "https://dl.k8s.io/release/$(curl -L -s https://dl.k8s.io/release/stable.txt)/bin/linux/amd64/kubectl.sha256"
sudo install -o root -g root -m 0755 kubectl /usr/local/bin/kubectl
```

- Once downloaded, run the command `kubectl version --client` to check

![Kubectl](/images/2.prerequisite/2.3.1-kubectl.png)
