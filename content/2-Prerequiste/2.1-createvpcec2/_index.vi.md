---
title: 'Chuẩn bị VPC và EC2'
date: '`r Sys.Date()`'
weight: 1
chapter: false
pre: ' <b> 2.1 </b> '
---

Trong bước này, chúng ta sẽ cần tạo một VPC có 2 subnet public / private. Sau đó tạo 1 EC2 Instance Linux nằm trong public subnet

Tổng quan kiến trúc sau khi các bạn hoàn tất bước này sẽ như sau:

![VPC](/images/2.prerequisite/001-vpcoverview.png)
Để tạo VPC chúng ta có thể sử dụng **CloudFormation**

1. Tạo **Key pairs**
   - Truy cập vào [giao diện quản trị EC2](https://ap-southeast-1.console.aws.amazon.com/ec2/home?region=ap-southeast-1#Home:)
   - Chọn **Key pairs**
   - Chọn **Create key pair**

![Key pair](/images/2.prerequisite/2.1-createkeypair.png)

- Ở bước **Create key pair**
- Nhập `jenkins-key`
- Chọn **RSA**
- Chọn **.pem**
- Click **Create**

![Complete](/images/2.prerequisite/2.1-complete.png)

2. Truy cập vào [giao diện quản trị của dịch vụ CloudFormation](https://ap-southeast-1.console.aws.amazon.com/cloudformation/home?region=ap-southeast-1#/).

- Tải file cấu hình CloudFormation [tại đây](/vpcConfig.yaml)

3. Create Stack.
   - Chọn **Create Stack**

![Create Stack](/images/2.prerequisite/2.1-createstack.png)

4. Chọn **Upload a template file**, chọn **vpcConfig.yaml** và sau đó chọn **Next**.

![Upload config file](/images/2.prerequisite/2.1-configStack.png)

5. Nhập **Vpc-stack** và chọn **Next**.

![Stack detail](/images/2.prerequisite/2.1-stackdetail.png)

6. Trong trang **Configure stack options**, giữ nguyên mặc định và chọn **Next**.

![Stack config options](/images/2.prerequisite/2.1-configDetault.png)

7. Trong trang **Review**, kiểm tra thông tin và chọn **Submit**.

![Stack review](/images/2.prerequisite/2.1-stackreview.png)

8. Tạo thành công

![Stakc success](/images/2.prerequisite/2.1-createSuccess.png)
