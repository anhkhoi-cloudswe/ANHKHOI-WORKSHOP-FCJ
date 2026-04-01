---
title: "Week 12 Worklog"
date: 2026-03-23
weight: 12
chapter: false
pre: " <b> 1.12. </b> "
---

### Week 12 Objectives:

* Fix Timezone Bug: migrate from local time to Wall-Clock Time (RFC 3339) strategy.
* Implement check-out grace period logic (allow check-out X minutes after event end).
* Optimize Docker images and implement security hardening.
* Resolve database query performance issues and apply missing indexes.
* Conduct security audit and patch vulnerabilities.

### Tasks to be carried out this week:
| Day | Task | Start Date | Completion Date | Reference Material |
| --- | ---- | ---------- | --------------- | ------------------ |
| 2 (Mon) | - Analyze Timezone Bug root cause: inconsistent DateTime handling across services <br> - Design RFC 3339 migration: UTC timestamps, timezone-aware comparisons <br> - Plan check-out grace period: event_end ± 15 minutes permitted window <br> - Audit all time-sensitive operations: comparisons, formatting, storage <br> - Plan database optimization: identify N+1 queries, plan indexes | 03/23/2026 | 03/23/2026 | Timezone & Performance Audit |
| 3 (Tue) | - **Timezone Bug Fix:** <br>&emsp; + Migrate all DateTime fields to RFC 3339 UTC format in database <br>&emsp; + Update service code: parse incoming times → UTC conversion <br>&emsp; + Fix time comparisons: use RFC 3339 string comparison or Unix timestamps <br>&emsp; + Implement timezone-aware output formatting for API responses <br>&emsp; + Test with multiple timezones (UTC, UTC+7, UTC-8) | 03/24/2026 | 03/24/2026 | DateTime Handling |
| 4 (Wed) | - **Check-out Grace Period Implementation:** <br>&emsp; + Update Ticket Service: check-out validation logic allows [event_end - buffer, event_end + 15min] <br>&emsp; + Add grace period configuration (default 15 minutes, configurable via env var) <br>&emsp; + Implement check-out UI prompt: "Event ends at X. Check-out allowed until Y." <br>&emsp; + Test edge cases: exactly at event_end, 1 second before, 1 minute after window <br>&emsp; + Database migration for grace period metadata | 03/25/2026 | 03/25/2026 | Business Logic Optimization |
| 5 (Thu) | - **Docker Image Optimization & Security:** <br>&emsp; + Multi-stage builds: reduce final image size from ~200MB to <50MB <br>&emsp; + Base image scan: use distroless or alpine for smaller footprint <br>&emsp; + Remove development dependencies from production image <br>&emsp; + Implement vulnerability scanning: Trivy/Snyk analysis <br>&emsp; + Apply security patches: update base images, Go modules <br>&emsp; + Add security headers and input validation in all endpoints | 03/26/2026 | 03/26/2026 | Docker & Security Hardening |
| 6 (Fri) | - **Database Performance & Final Testing:** <br>&emsp; + Identify and optimize N+1 queries: implement batch queries, joins <br>&emsp; + Add database indexes: event_id, user_id, created_at, status <br>&emsp; + Performance test: verify query execution time <100ms after optimization <br>&emsp; + Run full regression suite: verify all fixes don't break existing features <br>&emsp; + Generate security audit report: vulnerabilities found/fixed, recommendations <br>&emsp; + Performance benchmarking: checkout flow throughput capacity | 03/27/2026 | 03/27/2026 | Database Optimization & Testing |

### Week 12 Achievements:

✅ **Timezone Bug Resolution:** Migrated from local DateTime to RFC 3339 UTC strategy, fixing timezone inconsistencies across 6 services with comprehensive test coverage.

✅ **Wall-Clock Time Implementation:** All timestamps now stored/transmitted in RFC 3339 format with proper UTC normalization, eliminating daylight saving time issues.

✅ **Check-out Grace Period:** Implemented 15-minute post-event check-out window with configurable buffer, properly validated across Event → Ticket → Notification flow.

✅ **Docker Image Optimization:** Reduced production image size from ~200MB to ~45MB using multi-stage builds and distroless base, improving deployment speed by 60%.

✅ **Security Hardening:** Applied vulnerability patches, implemented security headers (HSTS, CSP), added input validation on all API endpoints, passed Trivy scan with 0 critical issues.

✅ **Database Performance:** Optimized 8 N+1 queries, added strategic indexes on event_id/user_id/status, reduced average query latency from 500ms to <80ms.

✅ **Query Optimization:** Verified checkout flow throughput: 500+ concurrent requests with <200ms p99 latency after database indexing.

✅ **Regression Testing:** Executed full test suite (45 integration tests, 120 unit tests) confirming all timezone and logic fixes maintain backward compatibility 100%.
