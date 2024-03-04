---
title: 'Cấu hình Kubernetes'
date: '`r Sys.Date()`'
weight: 3
chapter: false
pre: ' <b> 3.3 </b> '
---

1. Truy cập vào **Jenkins Instance**

![Access ec2](/images/3.createEksCluster/3.3-accessec2.png)

2. Thực hiện câu lệnh `aws configure`

   - Nhập **AWS_ACCESS_KEY_ID** và **AWS_SECRET_ACCESS_KEY** từ file .csv đã tải khi tạo **IAM User**
   - Nhập region `ap-southeast-1`

3. Cấu hình kubectl

   - Sau khi thực thi xong câu lệnh `aws configure`, chúng ta thực thi câu lệnh `aws eks update-kubeconfig --name Eks-cluster`

![Config kubectl](/images/3.createEksCluster/3.3-configkubectl.png)

4. Kiểm tra kubectl

   - Thực thi câu lệnh `kubectl get nodes`, nếu không có lỗi thì chúng ta đã cấu hình đúng
