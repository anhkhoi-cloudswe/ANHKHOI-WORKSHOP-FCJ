---
title: "Week 8 Worklog"
date: 2026-02-23
weight: 8
chapter: false
pre: " <b> 1.8. </b> "
---

### Week 8 Objectives:

* Develop Ticket Service with order creation and status management.
* Implement Wallet Service for payment processing and balance tracking.
* Design and establish Saga Pattern (Orchestration) for distributed transactions.
* Integrate with Event and Venue Services to ensure data consistency.
* Implement compensating transactions for failure scenarios.

### Tasks to be carried out this week:
| Day | Task | Start Date | Completion Date | Reference Material |
| --- | ---- | ---------- | --------------- | ------------------ |
| 2 (Mon) | - Design Ticket Service schema: tickets, orders, status enums <br> - Design Wallet Service schema: wallets, transactions, balance ledger <br> - Document Saga orchestration flow for ticket purchase transactions <br> - Define idempotency keys for transaction safety | 02/23/2026 | 02/23/2026 | Event Sourcing & Saga Patterns |
| 3 (Tue) | - **Implement Ticket Service:** <br>&emsp; + Create ticket order endpoints (POST create, GET status, PUT cancel) <br>&emsp; + Add order state machine (pending, confirmed, cancelled) <br>&emsp; + Implement seat reservation logic with pessimistic locking <br>&emsp; + Add request timeout validation (15-minute hold period) | 02/24/2026 | 02/24/2026 | Distributed Transactions Guide |
| 4 (Wed) | - **Implement Wallet Service:** <br>&emsp; + Create wallet management endpoints (GET balance, POST deposit, POST withdraw) <br>&emsp; + Implement double-entry bookkeeping for transactions <br>&emsp; + Add transaction ledger with immutable audit trail <br>&emsp; + Implement optimistic concurrency control with versioning | 02/25/2026 | 02/25/2026 | Payment System Architecture |
| 5 (Thu) | - **Implement Saga Orchestration:** <br>&emsp; + Create Saga Orchestrator as separate service <br>&emsp; + Implement ticket purchase saga (Event → Venue → Ticket → Wallet) <br>&emsp; + Add compensating transactions for rollback scenarios <br>&emsp; + Implement event-driven communication via async messages (SQS/SNS) <br>&emsp; + Add saga state persistence and recovery logic | 02/26/2026 | 02/26/2026 | Saga Pattern Implementation |
| 6 (Fri) | - **Testing & Integration:** <br>&emsp; + Integration tests for complete ticket purchase flow <br>&emsp; + Saga failure and recovery scenario testing <br>&emsp; + Concurrent purchase conflict detection tests <br>&emsp; + Wallet balance consistency verification across saga transitions <br>&emsp; + Load testing: simulate 50+ concurrent ticket purchases | 02/27/2026 | 02/27/2026 | Distributed System Testing |

### Week 8 Achievements:

✅ **Ticket Service Development:** Implemented comprehensive ticket ordering system with state machine (pending/confirmed/cancelled) and 15-minute seat hold expiration.

✅ **Wallet Service Implementation:** Created double-entry bookkeeping transaction system with immutable audit trail and optimistic concurrency control using version numbers.

✅ **Saga Pattern Orchestration:** Successfully designed and deployed Saga Orchestrator handling distributed transactions across 4 microservices with automatic compensation logic.

✅ **Distributed Transaction Safety:** Implemented idempotency keys and pessimistic locking for concurrent purchase scenarios, preventing double-booking and balance inconsistencies.

✅ **Event-Driven Communication:** Integrated AWS SQS for async message processing between services, replacing synchronous calls for improved resilience and scalability.

✅ **Compensating Transactions:** Implemented automatic refund logic and seat release mechanisms when saga steps fail, ensuring eventual consistency across services.

✅ **Transaction Persistence:** Built saga state management with database persistence and recovery mechanisms to handle service restarts and message redelivery scenarios.

✅ **Comprehensive Testing:** Created 35+ integration tests covering happy path, failure scenarios, and concurrent purchase conflicts with >85% code coverage.
