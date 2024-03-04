---
title: 'Create IAM User'
date: '`r Sys.Date()`'
weight: 1
chapter: false
pre: ' <b> 2.2.1 </b> '
---

1. Go to the [AWS IAM Console](https://ap-southeast-1.console.aws.amazon.com/iam/home#/home).

   - Select **User**.
   - Click **Add users**

2. In **Add user** step

   - Enter **User name**
   - Select **Provide user access to the AWS Management Console**
   - Select **I want to create an IAM user**
   - Select **Custom password**
   - Enter **Password**

![Create IAM User](/images/2.prerequisite/2.2.1-createiamuser.png)

3. Attach Policy

   - Select **Attach policies directly**
   - Search **AdministratorAccess** policy
   - Click **Next**

![Attach Policy](/images/2.prerequisite/2.2.1-attachpolicy.png)

4. In **Review and create** step

   - Click **Create user**

5. In **Retrieve password** step
   - Click **Download .csv file**
   - Click **Return to users list**

![Retrieve password](/images/2.prerequisite/2.2.1-downloadcsv.png)

6. Create **access key**

   - Select **user** was created
   - Select **Security**
   - Click **Create access key**

![Create access key](/images/2.prerequisite/2.2.1-createaccessky.png)

7. Config **access key**

   - Select **Command Line Interface (CLI)**
   - Click **I understand the above recommendation and want to proceed to create an access key.**
   - Select **Next**

![Config access key](/images/2.prerequisite/2.2.1-configaccesskey.png)

8. Compele creating **access key**

   - At step **Set description tag** -> Select **Create access key**
   - At step **Retrieve access keys** -> Select **Download .csv file** and Click **Done**
