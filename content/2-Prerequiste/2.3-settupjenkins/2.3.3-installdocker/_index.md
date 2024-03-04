---
title: 'Install Docker and Github'
date: '`r Sys.Date()`'
weight: 3
chapter: false
pre: ' <b> 2.3.3 </b> '
---

1. Tải **Docker**

- Sao chép câu lênh và dán vào **Jenkins Instance**

```bash
sudo yum install docker -y
sudo systemctl start docker
sudo groupadd docker
sudo usermod -a -G docker $USER
sudo chmod 666 /var/run/docker.sock
sudo systemctl stop docker
sudo systemctl start docker
```

- Sau khi tải xong, chạy lệnh `docker --version` để kiểm tra

![Kubectl](/images/2.prerequisite/2.3.3-downloaddocker.png)

2. Tải **Github**

```bash
sudo yum install git -y
```

- Sau khi tải xong, chạy lệnh `git --version` để kiểm tra

![Kubectl](/images/2.prerequisite/2.3.3-downloadgithub.png)
