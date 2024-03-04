+++
title = "Dọn dẹp tài nguyên  "
date = 2021
weight = 5
chapter = false
pre = "<b>5. </b>"
+++

Chúng ta sẽ tiến hành các bước sau để xóa các tài nguyên chúng ta đã tạo trong bài thực hành này.

#### Xóa EC2 instance

1. Truy cập [giao diện quản trị dịch vụ CloudFormation](https://ap-southeast-1.console.aws.amazon.com/cloudformation/home?region=ap-southeast-1)

- Click **Stack**.
- Click chọn **Vpc-stack**
- Click **Delete**

![Clean Stack](/images/5.cleanup/5.deletestack.png)

2. Truy cập [giao diện quản trị dịch vụ IAM](https://console.aws.amazon.com/iamv2/home#/home)

- Click **Roles**.
- Tại ô tìm kiếm , điền **myEKSClusterRole**.
- Click chọn **myEKSClusterRole **.
- Click **Delete**, sau đó điền tên role **myEKSClusterRole** và click **Delete** để xóa role.

![Clean](/images/5.cleanup/5.cleanrole.png)

- Tương tự với **myAmazonEKSNodeRole**

3. Click **Users**.

- Click chọn user **manage-eks**.
- Click **Delete**, sau đó điền tên user **manage-eks** và click **Delete** để xóa user.

![Clean](/images/5.cleanup/5.deleteuser.png)

#### Xóa EKS Cluster

1. Truy cập vào [giao diện quản trị dịch vụ EKS](https://ap-southeast-1.console.aws.amazon.com/eks/home?region=ap-southeast-1)

- Click **Eks-cluster**.
- Chọn **Compute** sau đó chọn **NodeGroups** và chọn **Delete** để xóa Node groups
- Sau khi xóa xong **NodeGroups**

- Quay trở lại và xóa **\*Eks-cluster**
