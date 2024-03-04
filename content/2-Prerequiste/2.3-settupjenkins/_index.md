---
title: 'Set up Jenkins'
date: '`r Sys.Date()`'
weight: 3
chapter: false
pre: ' <b> 2.3 </b> '
---

### Overview

- **kubectl** is a popular command-line tool used to manage Kubernetes container. **kubectl** allows system administrators and developers to interact with resources and perform management operations in a Kubernetes environment.

- **Jenkins** is a open-source automation server commonly used for building, deploying and automating project. It facilitates continuous integration and continuous dilivery (CICD) by automating the building, testing and deployment phrases of the software development lifecycle.

- **Docker** is a open-source platform designed to simplify the process of developing, deploying and testing application. Docker packages software into standardized units called containers that contains everything the software need to run includings library, system tools, code runtime

- **Git** is a widely used Version Control System designed to track changes in the source code of software projects.

- In this step:
  - We will install kubectl to interact with the EKS cluster
  - We will install Jenkins and set up basic configurations to access Jenkins through a web browser.
  - We will install Docker to create and update images for EKS usage and install Git to pull code

### Content

- [Install kubectl](2.3.1-installkubectl/)
- [Install Jenkins](2.3.2-installjenkin/)
- [Install Docker and Git](2.3.3-installdocker/)
