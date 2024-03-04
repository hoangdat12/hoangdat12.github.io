---
title: 'Triển khai Jenkins CICD'
date: '`r Sys.Date()`'
weight: 4
chapter: false
pre: ' <b> 4 </b> '
---

### Tổng quan

{{% notice info %}}
Bạn cần phải tạo 3 images và đẩy lên Docker hub với tên `${DOCKER_USERNAME}/api-gateway`, `${DOCKER_USERNAME}/user-api` và `${DOCKER_USERNAME}/auth-gateway`
{{% /notice %}}
{{% notice info %}}
Bạn có thể tải Code [tại đây](https://github.com/hoangdat12/eks-workshop.git)
{{% /notice %}}

- Trong bước này, chúng ta sẽ triển khai một Jenkins CICD pipeline
- Kiến trúc tổng quan của bước này sẽ như sau:

![Basic CICD](/images/4.cicd/Workshop-CICDPipeline.drawio.png)

### Nội dung

- [Cấu hình Jenkins Browser](configjenkins/)
- [Tạo Jenkins Pipeline](createpipeline/)
- [Kiểm tra CICD](testcicd/)
