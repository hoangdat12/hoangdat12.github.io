---
title: 'Create EKS Cluster'
date: '`r Sys.Date()`'
weight: 1
chapter: false
pre: ' <b> 3.1 </b> '
---

1. Go to the [AWS EKS Console](https://ap-southeast-1.console.aws.amazon.com/iam/home#/home).

   - Select **Cluster**.
   - Select **Add cluster**
   - Select **Create**

![Create cluster](/images/3.createEksCluster/3.1-createcluster.png)

2. At **Config cluster** step

   - Enter `Eks-cluster`
   - Select **Kubernetes version** is `1.29`
   - Select **myEKSClusterRole** that we created at chapter 1

![Config cluster](/images/3.createEksCluster/3.1-configcluster.png)

3. At **Specify Networking** step

   - Select VPC with name **Vpc**
   - Select **2 Private subnet**
   - Select **default Security group**
   - Select **Public**
   - Click **Next**

![Specify Networking](/images/3.createEksCluster/3.1-specifynetwork.png)
![Specify Networking](/images/3.createEksCluster/3.1-specifynetwork02.png)

4. At **Configure Observability** step

   - Select **Next**

5. At **Select Add-ons** step

   - Uncheck **Amazon EKS Pod Identify agent**
   - Select **Next**

![Add-ons](/images/3.createEksCluster/3.1-addons.png)

6. Complete craeting EKS Cluster

   - Select **Next** for the remaining steps
