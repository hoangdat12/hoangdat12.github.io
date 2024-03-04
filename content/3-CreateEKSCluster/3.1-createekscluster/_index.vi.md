---
title: 'Tạo EKS Cluster'
date: '`r Sys.Date()`'
weight: 1
chapter: false
pre: ' <b> 3.1 </b> '
---

1. Truy cập vào [giao diện quản trị của dịch vụ EKS](https://ap-southeast-1.console.aws.amazon.com/iam/home#/home).

   - Chọn **Cluster**.
   - Chọn **Add cluster**
   - Chọn **Create**

![Create cluster](/images/3.createEksCluster/3.1-createcluster.png)

2. Ở bước **Config cluster**

   - Nhập `Eks-cluster`
   - Chọn **Kubernetes version** là `1.29`
   - Chọn **myEKSClusterRole** mà chúng ta đã tạo ở phần 1

![Config cluster](/images/3.createEksCluster/3.1-configcluster.png)

3. Ở bước **Specify Networking**

   - Chọn VPC tên **Vpc**
   - Chọn **2 Private subnet**
   - Chọn **default Security group**
   - Chọn **Public**
   - Click **Next**

![Specify Networking](/images/3.createEksCluster/3.1-specifynetwork.png)
![Specify Networking](/images/3.createEksCluster/3.1-specifynetwork02.png)

4. Ở bước **Configure Observability**

   - Chọn **Next**

5. Ở bước **Select Add-ons**

   - Bỏ chọn **Amazon EKS Pod Identify agent**
   - Chọn **Next**

![Add-ons](/images/3.createEksCluster/3.1-addons.png)

6. Hoàn tất tạo EKS Cluster

   - Chọn **Next** ở những bước còn lại
