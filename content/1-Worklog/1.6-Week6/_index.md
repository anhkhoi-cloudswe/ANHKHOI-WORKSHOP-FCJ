---
title: "Week 6 Worklog"
date: 2026-02-09
weight: 6
chapter: false
pre: " <b> 1.6. </b> "
---

### Week 6 Objectives:

* Develop Authentication Service with JWT token generation and validation.
* Implement OAuth2 / API Key authentication mechanisms.
* Integrate IAM Roles for service-to-service authentication and authorization.

### Tasks to be carried out this week:
| Day | Task | Start Date | Completion Date | Reference Material |
| --- | ---- | ---------- | --------------- | ------------------ |
| 2 (Mon) | - Design Auth Service API contract: login, token generation, validation endpoints <br> - Learn JWT structure: header, payload, signature <br> - Study token expiration, refresh token patterns | 02/09/2026 | 02/09/2026 | JWT Best Practices Guide |
| 3 (Tue) | - **Implement Auth Service Core:** <br>&emsp; + Create user authentication endpoint (username/password validation) <br>&emsp; + Generate JWT tokens with custom claims <br>&emsp; + Implement token validation middleware | 02/10/2026 | 02/10/2026 | Go JWT Implementation |
| 4 (Wed) | - Implement OAuth2 patterns and API Key generation <br> - Create token refresh mechanism to extend session duration <br> - Add role-based access control (RBAC) to Auth Service | 02/11/2026 | 02/11/2026 | OAuth2 & RBAC Patterns |
| 5 (Thu) | - **Integrate IAM Roles:** <br>&emsp; + Create AWS IAM role for Auth Service <br>&emsp; + Configure cross-service JWT verification <br>&emsp; + Test service-to-service authentication flow | 02/12/2026 | 02/12/2026 | AWS IAM Service Roles |
| 6 (Fri) | - Implement logging/audit trails for auth events <br> - **Testing & Security:** <br>&emsp; + Performance test token generation (1000 req/sec) <br>&emsp; + Security test: invalid signature detection, token expiration | 02/13/2026 | 02/13/2026 | Security Testing Guide |

### Week 6 Achievements:

* Designed and implemented Auth Service with secure JWT token generation and validation.
* Implemented OAuth2 and API Key authentication mechanisms for flexibility.
* Created role-based access control (RBAC) system for authorization decisions.
* Successfully integrated AWS IAM Roles for secure service-to-service communication.
* Implemented comprehensive logging and audit trails for all authentication events.
* Achieved 1000+ tokens/second performance benchmark for JWT generation.
* Prepared Auth Service for integration with remaining microservices in Weeks 7-10.
