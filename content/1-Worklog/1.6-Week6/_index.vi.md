---
title: "Worklog Tuần 6"
date: 2026-02-09
weight: 6
chapter: false
pre: " <b> 1.6. </b> "
---

### Mục tiêu tuần 6:

* Phát triển Authentication Service với JWT token generation và validation.
* Triển khai OAuth2 / API Key authentication mechanisms.
* Tích hợp IAM Roles cho service-to-service authentication và authorization.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --------- | ------------ | --------------- | -------------- |
| 2   | - Thiết kế Auth Service API contract: login, token generation, validation endpoints <br> - Học JWT structure: header, payload, signature <br> - Học token expiration, refresh token patterns | 09/02/2026 | 09/02/2026 | Hướng dẫn JWT Best Practices |
| 3   | - **Triển khai Auth Service Core:** <br>&emsp; + Tạo authentication endpoint (username/password validation) <br>&emsp; + Tạo JWT tokens với custom claims <br>&emsp; + Triển khai token validation middleware | 10/02/2026 | 10/02/2026 | Go JWT Implementation |
| 4   | - Triển khai OAuth2 patterns và API Key generation <br> - Tạo token refresh mechanism <br> - Thêm role-based access control (RBAC) vào Auth Service | 11/02/2026 | 11/02/2026 | OAuth2 & RBAC Patterns |
| 5   | - **Tích hợp IAM Roles:** <br>&emsp; + Tạo AWS IAM role cho Auth Service <br>&emsp; + Cấu hình cross-service JWT verification <br>&emsp; + Kiểm tra service-to-service authentication | 12/02/2026 | 12/02/2026 | AWS IAM Service Roles |
| 6   | - Triển khai logging/audit trails cho auth events <br> - **Testing & Security:** <br>&emsp; + Performance test token generation <br>&emsp; + Security test: invalid signature, expiration | 13/02/2026 | 13/02/2026 | Security Testing Guide |

### Kết quả đạt được tuần 6:

* Thiết kế và triển khai Auth Service với JWT token generation và validation an toàn.
* Triển khai OAuth2 và API Key authentication mechanisms cho flexibility.
* Tạo hệ thống role-based access control (RBAC) cho authorization decisions.
* Tích hợp thành công AWS IAM Roles cho service-to-service communication an toàn.
* Triển khai comprehensive logging và audit trails cho tất cả authentication events.
* Đạt 1000+ tokens/second performance benchmark cho JWT generation.
* Chuẩn bị Auth Service cho integration với các microservices còn lại trong Tuần 7-10.
