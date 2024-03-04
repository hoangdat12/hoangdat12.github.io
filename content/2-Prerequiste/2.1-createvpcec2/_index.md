---
title: 'Prepre VPC and EC2'
date: '`r Sys.Date()`'
weight: 1
chapter: false
pre: ' <b> 2.1 </b> '
---

In this step, we need to create a VPC with 2 subnet public / private, Afterward, we will create a Linux EC2 Instance in the public subnet

The overall architecture after completing this step will look like this

![VPC](/images/2.prerequisite/001-vpcoverview.png)
To create a VPC, we can use **CloudFormation**

1. Create **Key pairs**
   - Go to the [AWS EC2 Console](https://ap-southeast-1.console.aws.amazon.com/ec2/home?region=ap-southeast-1#Home:)
   - Select **Key pairs**
   - Select **Create key pair**

![Key pair](/images/2.prerequisite/2.1-createkeypair.png)

- In **Create key pair** step
- Enter `jenkins-key`
- Select **RSA**
- Select **.pem**
- Click **Create**

![Complete](/images/2.prerequisite/2.1-complete.png)

2. Go to the [giao diện quản trị của dịch vụ CloudFormation](https://ap-southeast-1.console.aws.amazon.com/cloudformation/home?region=ap-southeast-1#/).

- Download the configuration file for CloudFormation [here](/vpcConfig.yaml)

3. Create Stack.
   - Select **Create Stack**

![Create Stack](/images/2.prerequisite/2.1-createstack.png)

4. Select **Upload a template file**, select **vpcConfig.yaml** and then select **Next**.

![Upload config file](/images/2.prerequisite/2.1-configStack.png)

5. Enter **Vpc-stack** and select **Next**.

![Stack detail](/images/2.prerequisite/2.1-stackdetail.png)

6. In **Configure stack options** page, remain the default and select **Next**.

![Stack config options](/images/2.prerequisite/2.1-configDetault.png)

7. In **Review** page, check the information and select **Submit**.

![Stack review](/images/2.prerequisite/2.1-stackreview.png)

8. Create success

![Stakc success](/images/2.prerequisite/2.1-createSuccess.png)
