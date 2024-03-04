---
title: 'Create IAM Role'
date: '`r Sys.Date()`'
weight: 2
chapter: false
pre: ' <b> 2.2.2 </b> '
---

1. Go to the [AWS IAM Console](https://ap-southeast-1.console.aws.amazon.com/iam/home#/home).

   - Select **Roles**.
   - Click **Create Role**

![Create Roles](/images/2.prerequisite/2.2.2-createroles.png)

2. In **Select trusted entity** step

   - Select **AWS service**
   - Search and Select **EKS**
   - Select **EKS - Cluster**

![Select trusted entity](/images/2.prerequisite/2.2.2-trustedentitytype.png)

3. In **Add permissions** step

   - Select **Next**

4. In **Name, review and create** step

   - Enter **myEKSClusterRole** at **Role name**
   - Select **Next**

![Name, review and create](/images/2.prerequisite/2.2.2-namereviewcreate.png)

5. Continue creating **myAmazonEKSNodeRole**

![myAmazonEKSNodeRole Role](/images/2.prerequisite/2.2.2-createec2role.png)

- Similar to the previous step, we create **myAmazonEKSNodeRole** Role with 4 Roles:

![Role](/images/2.prerequisite/2.2.2-ec2role.png)
