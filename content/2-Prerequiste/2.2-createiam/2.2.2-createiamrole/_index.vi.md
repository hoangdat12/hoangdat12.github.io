---
title: 'Tạo IAM Role'
date: '`r Sys.Date()`'
weight: 2
chapter: false
pre: ' <b> 2.2.2 </b> '
---

1. Truy cập vào [giao diện quản trị của dịch vụ IAM](https://ap-southeast-1.console.aws.amazon.com/iam/home#/home).

   - Chọn **Roles**.
   - Click **Create Role**

![Create Roles](/images/2.prerequisite/2.2.2-createroles.png)

2. Ở bước **Select trusted entity**

   - Chọn **AWS service**
   - Tìm và chọn **EKS**
   - Chọn **EKS - Cluster**

![Select trusted entity](/images/2.prerequisite/2.2.2-trustedentitytype.png)

3. Ở bước **Add permissions**

   - Chọn **Next**

4. Ở bước **Name, review and create**

   - Nhập **myEKSClusterRole** ở **Role name**
   - Chọn **Next**

![Name, review and create](/images/2.prerequisite/2.2.2-namereviewcreate.png)

5. Tiếp tục tạo **myAmazonEKSNodeRole**

![myAmazonEKSNodeRole Role](/images/2.prerequisite/2.2.2-createec2role.png)

- Tương tự như bước trước, chúng ta tạo **myAmazonEKSNodeRole** Role với 4 Role:

![Role](/images/2.prerequisite/2.2.2-ec2role.png)
