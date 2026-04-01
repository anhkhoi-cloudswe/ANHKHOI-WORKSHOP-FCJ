---
title: "Worklog Tuần 12"
date: 2026-03-23
weight: 12
chapter: false
pre: " <b> 1.12. </b> "
---

### Mục tiêu tuần 12:

* Fix Timezone Bug: chuyển từ local time sang Wall-Clock Time (RFC 3339) strategy.
* Triển khai check-out grace period logic (cho phép check-out X phút sau event end).
* Tối ưu Docker images và triển khai security hardening.
* Giải quyết database query performance issues và apply missing indexes.
* Thực hiện security audit và patch vulnerabilities.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --------- | ------------ | --------------- | -------------- |
| 2   | - Phân tích Timezone Bug root cause: inconsistent DateTime handling qua services <br> - Thiết kế RFC 3339 migration: UTC timestamps, timezone-aware comparisons <br> - Lập kế hoạch check-out grace period: event_end ± 15 minutes permitted window <br> - Audit tất cả time-sensitive operations: comparisons, formatting, storage <br> - Lập kế hoạch database optimization: identify N+1 queries, plan indexes | 23/03/2026 | 23/03/2026 | Timezone & Performance Audit |
| 3   | - **Timezone Bug Fix:** <br>&emsp; + Chuyển tất cả DateTime fields sang RFC 3339 UTC format trong database <br>&emsp; + Cập nhật service code: parse incoming times → UTC conversion <br>&emsp; + Fix time comparisons: dùng RFC 3339 string comparison hoặc Unix timestamps <br>&emsp; + Triển khai timezone-aware output formatting cho API responses <br>&emsp; + Test với multiple timezones (UTC, UTC+7, UTC-8) | 24/03/2026 | 24/03/2026 | DateTime Handling |
| 4   | - **Check-out Grace Period Implementation:** <br>&emsp; + Cập nhật Ticket Service: check-out validation logic allows [event_end - buffer, event_end + 15min] <br>&emsp; + Thêm grace period configuration (default 15 minutes, configurable via env var) <br>&emsp; + Triển khai check-out UI prompt: "Event ends at X. Check-out allowed until Y." <br>&emsp; + Test edge cases: exactly at event_end, 1 second trước, 1 phút sau window <br>&emsp; + Database migration cho grace period metadata | 25/03/2026 | 25/03/2026 | Business Logic Optimization |
| 5   | - **Docker Image Optimization & Security:** <br>&emsp; + Multi-stage builds: giảm final image size từ ~200MB xuống <50MB <br>&emsp; + Base image scan: dùng distroless hoặc alpine cho smaller footprint <br>&emsp; + Remove development dependencies từ production image <br>&emsp; + Triển khai vulnerability scanning: Trivy/Snyk analysis <br>&emsp; + Apply security patches: cập nhật base images, Go modules <br>&emsp; + Thêm security headers và input validation trong tất cả endpoints | 26/03/2026 | 26/03/2026 | Docker & Security Hardening |
| 6   | - **Database Performance & Final Testing:** <br>&emsp; + Xác định và optimize N+1 queries: implement batch queries, joins <br>&emsp; + Thêm database indexes: event_id, user_id, created_at, status <br>&emsp; + Performance test: xác nhận query execution time <100ms sau optimization <br>&emsp; + Chạy full regression suite: xác nhận tất cả fixes không break existing features <br>&emsp; + Generate security audit report: vulnerabilities found/fixed, recommendations <br>&emsp; + Performance benchmarking: checkout flow throughput capacity | 27/03/2026 | 27/03/2026 | Database Optimization & Testing |

### Kết quả đạt được tuần 12:

✅ **Timezone Bug Resolution:** Chuyển từ local DateTime sang RFC 3339 UTC strategy, fix timezone inconsistencies qua 6 services với comprehensive test coverage.

✅ **Wall-Clock Time Implementation:** Tất cả timestamps giờ stored/transmitted trong RFC 3339 format với proper UTC normalization, loại bỏ daylight saving time issues.

✅ **Check-out Grace Period:** Triển khai 15-minute post-event check-out window với configurable buffer, properly validated qua Event → Ticket → Notification flow.

✅ **Docker Image Optimization:** Giảm production image size từ ~200MB xuống ~45MB dùng multi-stage builds và distroless base, improve deployment speed 60%.

✅ **Security Hardening:** Apply vulnerability patches, implement security headers (HSTS, CSP), thêm input validation trên tất cả API endpoints, pass Trivy scan với 0 critical issues.

✅ **Database Performance:** Optimize 8 N+1 queries, thêm strategic indexes trên event_id/user_id/status, giảm average query latency từ 500ms xuống <80ms.

✅ **Query Optimization:** Xác nhận checkout flow throughput: 500+ concurrent requests với <200ms p99 latency sau database indexing.

✅ **Regression Testing:** Thực thi full test suite (45 integration tests, 120 unit tests) xác nhận tất cả timezone và logic fixes maintain backward compatibility 100%.
