---
title: "Worklog Tuần 5"
date: 2026-02-02
weight: 5
chapter: false
pre: " <b> 1.5. </b> "
---

## Tổng quan
Tuần 5 đánh dấu khởi đầu giai đoạn phát triển Hệ thống Quản lý Sự kiện FPT. Tuần này tập trung vào thiết kế kiến trúc microservices, lựa chọn công nghệ (Go, Docker), và cài đặt cơ sở hạ tầng trên AWS.

## Danh sách công việc

### Ngày 2: Thiết kế Kiến trúc Microservices
- Xác định domain boundaries và service boundaries
- Thiết kế service-to-service communication patterns
- Lập kế hoạch data consistency strategies
- Ghi chép service dependencies

### Ngày 3: Technology Stack & Development Environment
- Lựa chọn Go làm ngôn ngữ backend chính
- Cài đặt local development environment
- Cấu hình Docker cho containerization
- Thiết lập Docker Compose

### Ngày 4: Thiết kế Infrastructure trên AWS
- Thiết kế container orchestration strategy
- Lập kế hoạch VPC architecture
- Thiết kế inter-service communication
- Lập kế hoạch database per service

### Ngày 5: Cài đặt AWS Infrastructure
- Cài đặt VPC với appropriate subnets
- Cấu hình security groups
- Tạo ECR repositories
- Thiết lập CloudWatch log groups

### Ngày 6: Nền tảng CI/CD Pipeline
- Cài đặt GitHub repository structure
- Lập kế hoạch CI/CD workflow
- Xác định build, test, deployment stages
- Tạo infrastructure as code templates

## Thành tích đạt được
✅ Thiết kế comprehensive microservices architecture với domain-driven design principles  
✅ Thiết lập backend technology stack dựa trên Go với Docker containerization  
✅ Cấu hình AWS VPC infrastructure cho microservices deployment  
✅ Tạo ECR repositories với automated image management pipeline  
✅ Triển khai centralized logging sử dụng CloudWatch log groups  
✅ Thiết lập nền tảng cho CI/CD automation sử dụng Infrastructure as Code  

## Tài nguyên sử dụng
- AWS Architecture Best Practices
- Docker và Docker Compose
- Go Programming Language SDK
- GitHub Repository Management
- AWS CloudFormation / Terraform

## Ghi chú
- Microservices architecture yêu cầu service boundary definition cẩn thận
- Mỗi service nên có database riêng (CQRS patterns)
- Service discovery rất quan trọng trong distributed systems
- Triển khai circuit breaker patterns cho resilience
- Lập kế hoạch cho cross-cutting concerns từ đầu
| 5   | - **Triển khai Service Communication:** <br>&emsp; + Cấu hình inter-service REST API calls <br>&emsp; + Triển khai circuit breaker pattern <br>&emsp; + Thiết lập service discovery mechanism | 05/02/2026 | 05/02/2026 | Service Communication Guide |
| 6   | - **Infrastructure Setup:** <br>&emsp; + Thiết lập RDS database cluster <br>&emsp; + Cấu hình VPC cho service-to-service communication <br>&emsp; + Triển khai logging & monitoring với CloudWatch | 06/02/2026 | 06/02/2026 | AWS Infrastructure Setup |

### Kết quả đạt được tuần 5:

* Thiết kế Microservices Architecture toàn diện cho FPT Event Management System với 6 core services.
* Xác lập clear service boundaries, API contracts, data ownership patterns.
* Tạo Docker environment với Docker Compose cho local development và testing.
* Triển khai base Go service templates với proper project structure và configuration management.
* Thiết lập inter-service communication patterns với resilience mechanisms (circuit breaker, timeout).
* Cấu hình AWS infrastructure foundation: VPC, RDS clusters, CloudWatch monitoring.
* Chuẩn bị nền tảng cho Tuần 6-10 service-by-service development và integration.
