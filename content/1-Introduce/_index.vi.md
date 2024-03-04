---
title: 'Giới thiệu'
date: '`r Sys.Date()`'
weight: 1
chapter: false
pre: ' <b> 1. </b> '
---

**Amazon Elastic Kubernetes Service (Amazon EKS)** là một dịch vụ trên AWS để deploy, quản lý và scale các ứng dụng chạy bằng container sử dụng Kubernetes, đây là dịch vụ container orchestration được quản lý bởi AWS giúp loại bỏ nhu cầu cài đặt, vận hành và duy trì Kubernetes control plane trên AWS

**Jenkins** là một opensource dùng để thực hiện chức năng tích hợp liên tục (gọi là **CI – Continuous Integration**) và xây dựng các tác vụ tự động hóa. Nó quản lý và kiểm soát một số giai đoạn của quá trình triển khai phần mềm bao gồm xây dựng, tài liệu, kiểm tra tự động, đóng gói và phân tích mã tĩnh

**CICD** là viết tắt của Continuous Integration và Continuous Delivery/Deployment, là quá trình kết hợp tự động hoá giúp đẩy nhanh tiến độ phát triển sản phẩm và đưa sản phẩm đến người dùng cuối cùng.

Trong bài lab này, chúng ta sẽ tạo một **Kubernetes Cluster** đơn giản trên **AWS EKS (Elastic Kubernetes Service)**. Sau đó, sẽ triển khai trang ứng dụng trên cluster và sử dụng **Jenkins** để triển khai .

Để xem code được dùng cho bài lab này [tại đây](https://github.com/hoangdat12/eks-workshop.git)

![Introduce](/images/1.introduce/001-introduce.png)
