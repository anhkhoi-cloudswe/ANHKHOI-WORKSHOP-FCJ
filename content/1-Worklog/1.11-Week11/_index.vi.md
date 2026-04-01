---
title: "Worklog Tuần 11"
date: 2026-03-16
weight: 11
chapter: false
pre: " <b> 1.11. </b> "
---

### Mục tiêu tuần 11:

* Thực hiện Smoke Testing toàn hệ thống qua tất cả microservices và API endpoints.
* Triển khai Time Travel Testing sử dụng SYSTEM_TIME_OVERRIDE environment variable.
* Xác nhận check-in/check-out flow với simulated time progression.
* Xác nhận hành vi hệ thống trong quá trình chuyển trạng thái sự kiện.
* Lập tài liệu test scenarios và tạo automated test suite.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --------- | ------------ | --------------- | -------------- |
| 2   | - Thiết kế Smoke Test scenarios bao quát tất cả services <br> - Lập kế hoạch Time Travel Testing: SYSTEM_TIME_OVERRIDE environment variable implementation <br> - Xác định critical paths: event creation → ticket purchase → check-in → check-out <br> - Định nghĩa test data setup: test events với specific date/time windows | 16/03/2026 | 16/03/2026 | Smoke Testing & Time Simulation |
| 3   | - **Smoke Testing Phase 1:** <br>&emsp; + Test Event Service endpoints: create, list, update, delete <br>&emsp; + Xác nhận Venue Service capacity management và availability checks <br>&emsp; + Test Auth Service JWT token generation và validation <br>&emsp; + Xác nhận Wallet Service balance operations <br>&emsp; + Xác nhận ticket ordering system basic flow | 17/03/2026 | 17/03/2026 | API Endpoint Testing |
| 4   | - **Smoke Testing Phase 2:** <br>&emsp; + Test Saga orchestration: complete ticket purchase flow <br>&emsp; + Xác nhận Notification Service: order confirmation email delivery <br>&emsp; + Test PDF E-ticket generation và attachment quality <br>&emsp; + Xác nhận API responses: status codes (200, 201, 400, 404, 500) <br>&emsp; + Kiểm tra error message consistency và error codes | 18/03/2026 | 18/03/2026 | Integration Testing |
| 5   | - **Time Travel Testing Implementation:** <br>&emsp; + Triển khai SYSTEM_TIME_OVERRIDE trong tất cả services (đọc từ env variable) <br>&emsp; + Test event start → check-in allowed → event end → check-out allowed (15 min sau end) <br>&emsp; + Simulate events trong different states: upcoming, ongoing, completed <br>&emsp; + Xác nhận check-in validation: accept chỉ during event window <br>&emsp; + Xác nhận time-based transitions trong Saga orchestration | 19/03/2026 | 19/03/2026 | Time Simulation Testing |
| 6   | - **System Integration & Regression Testing:** <br>&emsp; + Chạy complete end-to-end test với time travel: Day 1 (purchase) → Day 2 (check-in) → Day 3 (check-out) <br>&emsp; + Xác nhận wallet consistency qua time jumps <br>&emsp; + Test concurrent operations under time acceleration <br>&emsp; + Lập tài liệu tất cả test cases (acceptance criteria, expected results) <br>&emsp; + Tạo automated test suite (Postman collection / pytest scripts) <br>&emsp; + Generate test report với coverage metrics | 20/03/2026 | 20/03/2026 | End-to-End Testing |

### Kết quả đạt được tuần 11:

✅ **Comprehensive Smoke Testing:** Xác nhận tất cả 6 microservices qua 40+ endpoint combinations với pass/fail verification.

✅ **Time Travel Implementation:** Triển khai SYSTEM_TIME_OVERRIDE environment variable handling trong tất cả services cho non-wall-clock time simulation.

✅ **Time-based Workflow Validation:** Thành công simulate multi-day event lifecycle: ticket purchase (Day 1) → check-in during event (Day 2) → check-out post-event (Day 3 với 15-min grace).

✅ **Check-in/Check-out Logic Verification:** Xác nhận time-window constraints: check-in chỉ allowed [event_start, event_end], check-out allowed [event_end, event_end + 15min].

✅ **Saga State Consistency:** Xác nhận distributed transaction state vẫn consistent qua time jumps với proper journal entries.

✅ **Error Scenario Coverage:** Test boundary conditions: too-early check-in, too-late check-out, concurrent operations during time transitions.

✅ **Automated Test Suite:** Tạo 35+ test cases với Postman collections và Python pytest scripts đạt 90% API coverage.

✅ **Performance Under Time Stress:** Xác nhận system stability khi accelerating time by minutes/hours, với database query performance <100ms.
