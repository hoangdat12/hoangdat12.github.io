---
title: 'Tạo EKS Node Group'
date: '`r Sys.Date()`'
weight: 2
chapter: false
pre: ' <b> 3.2 </b> '
---

1. Truy cập vào **Eks-cluster** mà chúng ta vừa tạo

   - Chọn **Compute**
   - Chọn **Add node group**

![Add node group](/images/3.createEksCluster/3.2-addnodegroup.png)

2. Ở bước **Configure node group**

   - Nhập `NodeGroups`
   - Chọn IAM Role **myAmazonEKSNodeRole** mà chúng ta đã tạo ở phần 1
   - Chọn **Next**

![Configure node group](/images/3.createEksCluster/3.2-confignodegroup.png)

3. Ở bước **Step compute and scaling configuration**

   - Chọn AMI Type
   - Chọn Capacity type
   - Chọn instance type là **t2.small**
   - Click **Next**

![Compute and Scaling](/images/3.createEksCluster/3.2-computeandscaling.png)

4. Ở bước **Specify Networking**

   - Chọn 2 Private subnet
   - Click **Next**

![Specify Networking](/images/3.createEksCluster/3.2-specifynetwork.png)

5. Ở bước **Review and create**

   - Chọn **Create**
