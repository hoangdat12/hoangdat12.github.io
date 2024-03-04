---
title: 'Test CICD'
date: '`r Sys.Date()`'
weight: 3
chapter: false
pre: ' <b> 4.3 </b> '
---

1. Truy cập vào **Jenkins Pipeline**

   - Chọn **Build Now** để kiểm tra xem chúng ta cấu hình có đúng không

![Test Build](/images/4.cicd/4.3-testbuild.png)

2. Thực hiện một thay đổi trong code của chúng ta và push lên github để kiếm tra **Webhook trigger**

![Webhook trigger](/images/4.cicd/4.3-pushgithub.png)
![Test Webhook](/images/4.cicd/4.3-testwebhook.png)

3. Kiểm tra trong **EKS cluster**

   - Chạy câu lệnh `kubectl get pods` để xem danh Pods đang chạy
   - Chạy câu lệnh `kubectl get deployments` để kiểm tra danh sách Deployment
   - Chạy câu lệnh `kubectl get services` để kiểm tra danh sách Service

![Kubectl Command](/images/4.cicd/4.3-kubectlcommand.png)
