---
title: "Week 7 Worklog"
date: 2026-02-16
weight: 7
chapter: false
pre: " <b> 1.7. </b> "
---

### Week 7 Objectives:

* Develop Event Service with CRUD operations and business logic.
* Implement Venue Service with capacity management and booking logic.
* Integrate both services with database and Auth Service validation.

### Tasks to be carried out this week:
| Day | Task | Start Date | Completion Date | Reference Material |
| --- | ---- | ---------- | --------------- | ------------------ |
| 2 (Mon) | - Design Event Service schema: events table, bookings, status tracking <br> - Design Venue Service schema: venues, capacities, availability <br> - Plan service API contracts and database relationships | 02/16/2026 | 02/16/2026 | Database Design Patterns |
| 3 (Tue) | - **Implement Event Service:** <br>&emsp; + Create events endpoints (GET all, GET by ID, POST create, PUT update, DELETE) <br>&emsp; + Add event filtering and pagination <br>&emsp; + Implement event status management (draft, published, ended) | 02/17/2026 | 02/17/2026 | Go CRUD API Patterns |
| 4 (Wed) | - Implement Venue Service CRUD operations <br> - Add venue capacity management and validation <br> - Implement availability check logic before booking | 02/18/2026 | 02/18/2026 | Go Database Integration |
| 5 (Thu) | - **Integrate with Auth Service:** <br>&emsp; + Add JWT middleware to both services <br>&emsp; + Implement authorization checks (only organizers can modify events) <br>&emsp; + Add audit logging for business operations | 02/19/2026 | 02/19/2026 | Service Integration Patterns |
| 6 (Fri) | - **Testing & Optimization:** <br>&emsp; + Integration tests between Event & Venue Services <br>&emsp; + Database query optimization (indexing) <br>&emsp; + Load testing with 100 concurrent requests | 02/20/2026 | 02/20/2026 | Testing & Optimization Guide |

### Week 7 Achievements:

* Designed and implemented Event Service with complete CRUD operations and event lifecycle management.
* Developed Venue Service with capacity tracking and real-time availability checking.
* Integrated JWT authentication into both services with proper authorization enforcement.
* Implemented database indexes for optimal query performance on event and venue lookups.
* Created comprehensive unit and integration tests achieving >80% code coverage.
* Successfully handled 100+ concurrent requests with sub-100ms response times.
* Prepared both services for Ticket Service integration in Week 8.
