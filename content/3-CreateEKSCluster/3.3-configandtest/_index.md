---
title: 'Configure Kubernetes'
date: '`r Sys.Date()`'
weight: 3
chapter: false
pre: ' <b> 3.3 </b> '
---

1. Access to the **Jenkins Instance**

![Access ec2](/images/3.createEksCluster/3.3-accessec2.png)

2. Execute the command `aws configure`

   - Enter **AWS_ACCESS_KEY_ID** and **AWS_SECRET_ACCESS_KEY** from file .csv downloaded when we craete **IAM User**
   - Enter region `ap-southeast-1`

3. Configure kubectl

   - After executing the command `aws configure`, we execute the command `aws eks update-kubeconfig --name Eks-cluster`

![Config kubectl](/images/3.createEksCluster/3.3-configkubectl.png)

4. Test kubectl

   - Execute the command `kubectl get nodes`, If there are no errors then we have configured correctly
