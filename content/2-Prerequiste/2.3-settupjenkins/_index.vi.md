---
title: 'Chuẩn bị Jenkins Server'
date: '`r Sys.Date()`'
weight: 3
chapter: false
pre: ' <b> 2.3 </b> '
---

### Overview

- **kubectl** là một công cụ command-line phổ biến được sử dụng để quản lý Kubernetes container. **kubectl** giúp những người quản trị hệ thống và các lập trình viên tương tác với những tài nguyên và thực hiện quản lý vận hành môi trường bên trong Kubernetes

- **Jenkins** là máy chủ tự động mã nguồn mở được sử dụng phổ biến để xây dựng, triển khai và tự động hóa dự án. Nó hỗ trợ quá trình CICD bằng việc tự động hóa các giai đoạn xây dựng, kiểm thử và triển khai của vòng đời phát triển phần mềmn

- **Docker** là một platform mã nguồn mở được thiết kế để đơn giản quá trình phát triển, triển khai và kiểm thử phần mềm. **Docker** đóng gói phần mềm trong một đơn vị tiêu chuẩn gọi là containers chứa tất cả những thứ cần để chạy ứng dụng bao gồm thư viện, công cực và code

- **Git** là một hệ thống quản lý phiên bản phần mềm phổ biến được thiết kế để theo dõi các thay đổi trong mã nguồn của dự án phần mềm. Git rộng rãi sử dụng để duy trì tính nhất quán và quản lý phiên bản của mã nguồn trong các dự án phần mềm.

- In this step:
  - Chúng ta sẽ cài đặt kubectl để tương tác với EKS
  - Chúng ta sẽ tải Jenkins và cấu hình cơ bản để truy cập vào Jenkins thông qua web browser
  - Chúng ta sẽ cài đặt Docker để tạo và update image để EKS sử dụng, tải Git để pull code

### Content

- [Cài đặt kubectl](2.3.1-installkubectl/)
- [Cài đặt Jenkins](2.3.2-installjenkin/)
- [Cài đặt Docker và Git](2.3.3-installdocker/)
