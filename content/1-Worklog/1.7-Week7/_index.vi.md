---
title: "Worklog Tuần 7"
date: 2026-02-16
weight: 7
chapter: false
pre: " <b> 1.7. </b> "
---

### Mục tiêu tuần 7:

* Phát triển Event Service với CRUD operations và business logic.
* Triển khai Venue Service với capacity management và booking logic.
* Tích hợp cả hai services với database và Auth Service validation.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --------- | ------------ | --------------- | -------------- |
| 2   | - Thiết kế Event Service schema: events table, bookings, status tracking <br> - Thiết kế Venue Service schema: venues, capacities, availability <br> - Lập kế hoạch API contracts và database relationships | 16/02/2026 | 16/02/2026 | Database Design Patterns |
| 3   | - **Triển khai Event Service:** <br>&emsp; + Tạo endpoints cho events (GET all, GET by ID, POST, PUT, DELETE) <br>&emsp; + Thêm event filtering và pagination <br>&emsp; + Triển khai event status management | 17/02/2026 | 17/02/2026 | Go CRUD API Patterns |
| 4   | - Triển khai Venue Service CRUD operations <br> - Thêm venue capacity management và validation <br> - Triển khai availability check logic trước booking | 18/02/2026 | 18/02/2026 | Go Database Integration |
| 5   | - **Tích hợp với Auth Service:** <br>&emsp; + Thêm JWT middleware vào cả hai services <br>&emsp; + Triển khai authorization checks <br>&emsp; + Thêm audit logging cho business operations | 19/02/2026 | 19/02/2026 | Service Integration Patterns |
| 6   | - **Testing & Optimization:** <br>&emsp; + Integration tests giữa Event & Venue Services <br>&emsp; + Database query optimization (indexing) <br>&emsp; + Load testing với 100 concurrent requests | 20/02/2026 | 20/02/2026 | Testing & Optimization Guide |

### Kết quả đạt được tuần 7:

* Thiết kế và triển khai Event Service với complete CRUD operations và event lifecycle management.
* Phát triển Venue Service với capacity tracking và real-time availability checking.
* Tích hợp JWT authentication vào cả hai services với proper authorization enforcement.
* Triển khai database indexes cho optimal query performance trên event và venue lookups.
* Tạo comprehensive unit và integration tests đạt >80% code coverage.
* Xử lý thành công 100+ concurrent requests với sub-100ms response times.
* Chuẩn bị cả hai services cho Ticket Service integration trong Tuần 8.
