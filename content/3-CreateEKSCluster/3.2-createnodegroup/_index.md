---
title: 'Create EKS Node Group'
date: '`r Sys.Date()`'
weight: 2
chapter: false
pre: ' <b> 3.2 </b> '
---

1. Access to **Eks-cluster** that we just created

   - Select **Compute**
   - Select **Add node group**

![Add node group](/images/3.createEksCluster/3.2-addnodegroup.png)

2. In **Configure node group** step

   - Enter `NodeGroups`
   - Select IAM Role **myAmazonEKSNodeRole** that we created at chapter 1
   - Select **Next**

![Configure node group](/images/3.createEksCluster/3.2-confignodegroup.png)

3. In **Step compute and scaling configuration** step

   - Select AMI Type
   - Select Capacity type
   - Select instance type is **t2.small**
   - Click **Next**

![Compute and Scaling](/images/3.createEksCluster/3.2-computeandscaling.png)

4. In **Specify Networking** step

   - Select 2 Private subnet
   - Click **Next**

![Specify Networking](/images/3.createEksCluster/3.2-specifynetwork.png)

5. In **Review and create** step

   - Ckick **Create**
