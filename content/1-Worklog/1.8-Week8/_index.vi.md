---
title: "Worklog Tuần 8"
date: 2026-02-23
weight: 8
chapter: false
pre: " <b> 1.8. </b> "
---

### Mục tiêu tuần 8:

* Phát triển Ticket Service với order creation và status management.
* Triển khai Wallet Service cho payment processing và balance tracking.
* Thiết kế và xây dựng Saga Pattern (Orchestration) cho distributed transactions.
* Tích hợp với Event và Venue Services để đảm bảo data consistency.
* Triển khai compensating transactions cho failure scenarios.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --------- | ------------ | --------------- | -------------- |
| 2   | - Thiết kế Ticket Service schema: tickets, orders, status enums <br> - Thiết kế Wallet Service schema: wallets, transactions, balance ledger <br> - Lập tài liệu Saga orchestration flow cho ticket purchase transactions <br> - Định nghĩa idempotency keys cho transaction safety | 23/02/2026 | 23/02/2026 | Event Sourcing & Saga Patterns |
| 3   | - **Triển khai Ticket Service:** <br>&emsp; + Tạo ticket order endpoints (POST create, GET status, PUT cancel) <br>&emsp; + Thêm order state machine (pending, confirmed, cancelled) <br>&emsp; + Triển khai seat reservation logic với pessimistic locking <br>&emsp; + Thêm request timeout validation (15-minute hold period) | 24/02/2026 | 24/02/2026 | Distributed Transactions Guide |
| 4   | - **Triển khai Wallet Service:** <br>&emsp; + Tạo wallet management endpoints (GET balance, POST deposit, POST withdraw) <br>&emsp; + Triển khai double-entry bookkeeping cho transactions <br>&emsp; + Thêm transaction ledger với immutable audit trail <br>&emsp; + Triển khai optimistic concurrency control với versioning | 25/02/2026 | 25/02/2026 | Payment System Architecture |
| 5   | - **Triển khai Saga Orchestration:** <br>&emsp; + Tạo Saga Orchestrator như separate service <br>&emsp; + Triển khai ticket purchase saga (Event → Venue → Ticket → Wallet) <br>&emsp; + Thêm compensating transactions cho rollback scenarios <br>&emsp; + Triển khai event-driven communication qua async messages (SQS/SNS) <br>&emsp; + Thêm saga state persistence và recovery logic | 26/02/2026 | 26/02/2026 | Saga Pattern Implementation |
| 6   | - **Testing & Integration:** <br>&emsp; + Integration tests cho complete ticket purchase flow <br>&emsp; + Saga failure và recovery scenario testing <br>&emsp; + Concurrent purchase conflict detection tests <br>&emsp; + Wallet balance consistency verification across saga transitions <br>&emsp; + Load testing: simulate 50+ concurrent ticket purchases | 27/02/2026 | 27/02/2026 | Distributed System Testing |

### Kết quả đạt được tuần 8:

✅ **Ticket Service Development:** Triển khai hệ thống ticket ordering toàn diện với state machine (pending/confirmed/cancelled) và 15-minute seat hold expiration.

✅ **Wallet Service Implementation:** Tạo double-entry bookkeeping transaction system với immutable audit trail và optimistic concurrency control dùng version numbers.

✅ **Saga Pattern Orchestration:** Thiết kế và triển khai thành công Saga Orchestrator xử lý distributed transactions qua 4 microservices với automatic compensation logic.

✅ **Distributed Transaction Safety:** Triển khai idempotency keys và pessimistic locking cho concurrent purchase scenarios, ngăn chặn double-booking và balance inconsistencies.

✅ **Event-Driven Communication:** Tích hợp AWS SQS cho async message processing giữa các services, thay thế synchronous calls để cải thiện resilience và scalability.

✅ **Compensating Transactions:** Triển khai automatic refund logic và seat release mechanisms khi saga steps fail, đảm bảo eventual consistency qua services.

✅ **Transaction Persistence:** Xây dựng saga state management với database persistence và recovery mechanisms để xử lý service restarts và message redelivery scenarios.

✅ **Comprehensive Testing:** Tạo 35+ integration tests bao gồm happy path, failure scenarios, và concurrent purchase conflicts với >85% code coverage.
