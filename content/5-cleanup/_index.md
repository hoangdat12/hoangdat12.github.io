+++
title = "Clean up resources"
date = 2021
weight = 5
chapter = false
pre = "<b>5. </b>"
+++

Chúng ta sẽ tiến hành các bước sau để xóa các tài nguyên chúng ta đã tạo trong bài thực hành này.

#### Xóa EC2 instance

1. Go to the [giao diện quản trị dịch vụ CloudFormation](https://ap-southeast-1.console.aws.amazon.com/cloudformation/home?region=ap-southeast-1)

- Click **Stack**.
- Select **Vpc-stack**
- Click **Delete**

![Clean Stack](/images/5.cleanup/5.deletestack.png)

2. Go to the [giao diện quản trị dịch vụ IAM](https://console.aws.amazon.com/iamv2/home#/home)

- Click **Roles**.
- In the search box, enter**myEKSClusterRole**.
- Select **myEKSClusterRole **.
- Click **Delete**, then enter the role name **myEKSClusterRole** and click **Delete** to delete.

![Clean](/images/5.cleanup/5.cleanrole.png)

- Similar to **myAmazonEKSNodeRole**

3. Click **Users**.

- Select **manage-eks**.
- Click **Delete**, then enter User name **manage-eks** and click **Delete** to delete user.

![Clean](/images/5.cleanup/5.deleteuser.png)

#### Xóa EKS Cluster

1. Go to the [giao diện quản trị dịch vụ EKS](https://ap-southeast-1.console.aws.amazon.com/eks/home?region=ap-southeast-1)

- Click **Eks-cluster**.
- Select **Compute** then select **NodeGroups** and select **Delete** to delete Node groups
- After deleted **NodeGroups**
- Go back and delete **\*Eks-cluster**
