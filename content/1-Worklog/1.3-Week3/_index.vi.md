---
title: "Tuần 3: Storage, Database & DNS"
date: 2026-01-19
weight: 3
chapter: false
pre: " <b> 1.3. </b> "
---

## Tổng quan
Tuần 3 bao gồm ba dịch vụ AWS quan trọng cho quản lý dữ liệu: S3 cho lưu trữ object và hosting trang web tĩnh, RDS cho cơ sở dữ liệu quan hệ, và Route 53 cho quản lý DNS.

## Danh sách công việc

### Ngày 2: Nền tảng S3 & Static Web Hosting
- Tạo S3 buckets với naming conventions
- Cấu hình bucket policies và access control
- Kích hoạt Static Website Hosting trên S3
- Upload và tổ chức static content

### Ngày 3: Cấu hình S3 Nâng cao
- Cấu hình CORS
- Thiết lập CloudFront distribution với S3 origin
- Triển khai S3 versioning và lifecycle policies
- Cấu hình S3 encryption

### Ngày 4: Nền tảng RDS Database
- Tạo RDS instances (MySQL, PostgreSQL)
- Hiểu về DB subnet groups
- Cấu hình Multi-AZ deployment
- Thiết lập automated backups

### Ngày 5: RDS Nâng cao & Quản lý Database
- Tạo read replicas
- Cấu hình database security groups
- Hiểu về connection pooling
- Triển khai database monitoring

### Ngày 6: Route 53 DNS & Domain Management
- Đăng ký domain trong Route 53
- Tạo hosted zone và DNS records
- Thiết lập health checks
- Cấu hình alias records
- Triển khai routing policies

## Thành tích đạt được
✅ Triển khai thành công trang web tĩnh trên S3 với CloudFront distribution
✅ Thiết lập cơ sở hạ tầng RDS có tính khả dụng cao với Multi-AZ
✅ Triển khai cơ sở hạ tầng DNS sử dụng Route 53
✅ Cấu hình S3 lifecycle policies cho tối ưu hóa chi phí
✅ Kích hoạt end-to-end encryption cho dữ liệu
✅ Tạo chiến lược automated backup cho database resilience

## Tài nguyên sử dụng
- AWS S3 Console
- RDS Database Console
- Route 53 Hosted Zones
- CloudFront Distribution Manager
- AWS Certificate Manager (ACM)

## Ghi chú
- Tên S3 bucket phải là duy nhất trên toàn AWS
- Multi-AZ RDS cung cấp synchronous replication
- Route 53 hỗ trợ nhiều routing policies
- Luôn triển khai lifecycle policies cho S3
- Database backups nên được giữ theo yêu cầu compliance
