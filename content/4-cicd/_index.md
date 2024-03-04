---
title: 'Implement Jenkins CICD'
date: '`r Sys.Date()`'
weight: 4
chapter: false
pre: ' <b> 4 </b> '
---

### Overview

{{% notice info %}}

You need create 3 images and push to Docker hub with name `${DOCKER_USERNAME}/api-gateway`, `${DOCKER_USERNAME}/user-api` và `${DOCKER_USERNAME}/auth-gateway`
{{% /notice %}}

{{% notice info %}}
You can download code [here](https://github.com/hoangdat12/eks-workshop.git)
{{% /notice %}}

- In this step, we will implement a Jenkins CICD pipeline
- The overall architecture of this step will look like this

![Basic CICD](/images/4.cicd/Workshop-CICDPipeline.drawio.png)

### Content

- [Configure Jenkins Browser](configjenkins/)
- [Create Jenkins Pipeline](createpipeline/)
- [Test CICD](testcicd/)
