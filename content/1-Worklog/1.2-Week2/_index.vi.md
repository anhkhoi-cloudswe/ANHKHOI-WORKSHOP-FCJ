---
title: "Tuần 2: VPC & Nền tảng EC2 Compute"
date: 2026-01-12
weight: 2
chapter: false
pre: " <b> 1.2. </b> "
---

## Tổng quan
Tuần 2 tập trung vào networking và dịch vụ compute - xương sống của cơ sở hạ tầng AWS. Tuần này bao gồm thiết lập VPC, EC2 instances, và tích hợp IAM roles cho xác thực dịch vụ.

## Danh sách công việc

### Ngày 2: Nền tảng VPC Networking
- Tạo Virtual Private Cloud (VPC) với custom CIDR blocks
- Cấu hình Public và Private Subnets
- Thiết lập Internet Gateway (IGW)
- Cấu hình Route Tables

### Ngày 3: VPC Networking Nâng cao
- Tạo và cấu hình NAT Gateway
- Thiết lập VPC Endpoints cho AWS services
- Hiểu về VPC Peering
- Cấu hình Security Groups và Network ACLs

### Ngày 4: Nền tảng EC2 Instances
- Khởi chạy EC2 instances (t2.micro, t2.small)
- Hiểu về Amazon Machine Images (AMI)
- Cấu hình Elastic Block Store (EBS) volumes
- Quản lý vòng đời instance

### Ngày 5: EC2 Nâng cao & Instance Profiling
- Khởi chạy instances với custom security groups
- Cấu hình Elastic IPs
- Giám sát instance metrics via CloudWatch
- Hiểu về EC2 instance families

### Ngày 6: IAM Roles cho EC2 Services
- Tạo IAM Roles cho EC2 instances
- Gắn Instance Profiles vào EC2
- Cấu hình xác thực dịch vụ
- Kiểm tra quyền truy cập role-based

## Thành tích đạt được
✅ Thiết kế và triển khai VPC architecture an toàn với public/private subnets
✅ Triển khai EC2 instances với cấu hình security group
✅ Thiết lập xác thực EC2 service dựa trên IAM Role
✅ Cấu hình NAT Gateway cho outbound connectivity
✅ Triển khai VPC endpoint access patterns
✅ Xác thực EC2 instance profiling và CloudWatch metrics

## Tài nguyên sử dụng
- AWS VPC Console
- EC2 Dashboard
- AWS IAM Management Console
- CloudWatch Monitoring

## Ghi chú
- VPC là nền tảng của kiến trúc mạng cloud
- Luôn sử dụng IAM Roles thay vì access keys cho EC2
- Security Groups là stateful; NACLs là stateless
- Cô lập workloads bằng subnets và security controls
