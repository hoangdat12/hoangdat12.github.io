---
title: 'Tạo IAM User'
date: '`r Sys.Date()`'
weight: 1
chapter: false
pre: ' <b> 2.2.1 </b> '
---

1. Truy cập vào [giao diện quản trị của dịch vụ IAM](https://ap-southeast-1.console.aws.amazon.com/iam/home#/home).

   - Click chọn **User**.
   - Chọn **Add users**

2. Trong bước **Add user**

   - Nhập **User name**
   - Click vào **Provide user access to the AWS Management Console**
   - Click chọn **I want to create an IAM user**
   - Chọn **Custom password**
   - Nhập **Password**

![Create IAM User](/images/2.prerequisite/2.2.1-createiamuser.png)

3. Gắn Policy

   - Click chọn **Attach policies directly**
   - Tìm **AdministratorAccess** policy
   - Click **Next**

![Attach Policy](/images/2.prerequisite/2.2.1-attachpolicy.png)

4. Trong bước **Review and create**

   - Chọn **Create user**

5. Trong bước **Retrieve password**
   - Click **Download .csv file**
   - Click **Return to users list**

![Retrieve password](/images/2.prerequisite/2.2.1-downloadcsv.png)

6. Tạo **access key**

   - Chọn vào **user** vừa tạo
   - Chọn **Security**
   - Click **Create access key**

![Create access key](/images/2.prerequisite/2.2.1-createaccessky.png)

7. Cấu hình **access key**

   - Chọn **Command Line Interface (CLI)**
   - Click **I understand the above recommendation and want to proceed to create an access key.**
   - Chọn **Next**

![Config access key](/images/2.prerequisite/2.2.1-configaccesskey.png)

8. Hoàn tất tạo **access key**

   - Ở bước **Set description tag** -> Chọn **Create access key**
   - Ở bước **Retrieve access keys** -> Chọn **Download .csv file** và Click **Done**
