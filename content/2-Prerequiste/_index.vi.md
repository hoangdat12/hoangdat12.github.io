---
title: 'Các bước chuẩn bị'
date: '`r Sys.Date()`'
weight: 2
chapter: false
pre: ' <b> 2. </b> '
---

<!-- {{% notice info %}}
Bạn cần tạo sẵn 1 Linux instance thuộc public subnet và 1 Window instance thuộc private subnet để thực hiện bài thực hành này.
{{% /notice %}} -->

### Tổng quan

- Trong bước này, chúng ta sẽ tạo ra VPC và EC2 instance
- Tạo ra IAM User cho EC2 và IAM Role cho EKS cluster
- Tiến hành cấu hình EC2 instance

### Nội dung

- [Chuẩn bị VPC và EC2 Instance](2.1-createvpc/)
- [Tạo IAM Role](2.2-createiamrole/)
- [Cấu hình Jenkins Server](2.3-settupjenkins/)
