---
title: 'Tải kubectl'
date: '`r Sys.Date()`'
weight: 1
chapter: false
pre: ' <b> 2.3.1 </b> '
---

1. Truy cập vào [giao diện quản trị của dịch vụ EC2](https://ap-southeast-1.console.aws.amazon.com/ec2/home?region=ap-southeast-1).

   - Chọn **Instance**.
   - Chọn **Jenkins-Instance**
   - Click **Connect**

![Connect](/images/2.prerequisite/2.3.1-connectEc2.png)

2. Ở trong giao diện **Connect**, chúng ta cần làm theo hướng dẫn để truy cập vào **Jenkins-Instance**

3. Tải **kubectl**

- Sao chép câu lênh và dán vào **Jenkins Instance** mà chúng ta vừa truy cập

```bash
curl -LO "https://dl.k8s.io/release/$(curl -L -s https://dl.k8s.io/release/stable.txt)/bin/linux/amd64/kubectl"
curl -LO "https://dl.k8s.io/release/$(curl -L -s https://dl.k8s.io/release/stable.txt)/bin/linux/amd64/kubectl.sha256"
sudo install -o root -g root -m 0755 kubectl /usr/local/bin/kubectl
```

- Sau khi tải xong, chạy lệnh `kubectl version --client` để kiểm tra

![Kubectl](/images/2.prerequisite/2.3.1-kubectl.png)
