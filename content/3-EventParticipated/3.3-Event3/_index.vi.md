---
title: "Event 3"
date: 2026-03-31
weight: 3
chapter: false
pre: " <b> 4.3. </b> "
---


# Bài thu hoạch "AWS re:Invent 2025 – Kiến trúc hiện đại hóa ứng dụng & GenAI"

### Mục Đích Của Sự Kiện

- Cập nhật các announcement quan trọng từ AWS re:Invent 2025 (Nova models, Trainium3 UltraServers, AI agents, GenAI, modernization, data…).
- Giúp khách tham dự hiểu các best practice về hiện đại hóa ứng dụng, kiến trúc microservices, event‑driven, serverless/container và AI‑driven development.
- Tạo cơ hội networking giữa AWS experts, partners, và cộng đồng cloud/AI tại Việt Nam để hỗ trợ các dự án chuyển đổi số.

### Danh Sách Diễn Giả

- **AWS speakers**: Các Solution Architect và Specialist từ AWS Vietnam chia sẻ về kiến trúc hiện đại, GenAI, và kinh nghiệm triển khai thực tế cho khách hàng tại Việt Nam.
- **Customer speakers/Partners**: Đại diện từ các doanh nghiệp, đối tác AWS ở Việt Nam chia sẻ case study chuyển đổi từ legacy monolith sang microservices, áp dụng event‑driven và AI trên AWS.

### Nội Dung Nổi Bật

#### Nhược điểm của kiến trúc ứng dụng legacy

- Ứng dụng nguyên khối (monolith) khó mở rộng theo từng module, mỗi lần release phải build và deploy cả hệ thống, tăng rủi ro và thời gian down‑time.
- Ràng buộc công nghệ (technology lock‑in), khó áp dụng công nghệ mới như serverless, containers, GenAI, real‑time data vì kiến trúc không tách biệt.
- Độ tin cậy và khả năng chịu lỗi thấp, một lỗi nhỏ có thể ảnh hưởng toàn bộ hệ thống, khó triển khai patterns như blue/green, canary, resilience.

#### Chuyển đổi sang kiến trúc ứng dụng hiện đại – Microservices

- Chia ứng dụng thành các service nhỏ, độc lập, có thể scale và deploy riêng, phù hợp với team nhỏ, triển khai CI/CD nhanh hơn.
- Cho phép chọn công nghệ phù hợp từng service (polyglot), dễ thử nghiệm tính năng mới hoặc tích hợp AI, streaming, event‑driven.
- Trên AWS, microservices thường kết hợp với Amazon ECS/EKS/Lambda, API Gateway, Service Discovery và observability stack (CloudWatch, X‑Ray…).

#### Event‑Driven Architecture

- Sử dụng events để tách loose coupling giữa services, giúp hệ thống linh hoạt, dễ mở rộng thêm consumer mà không ảnh hưởng producer.
- Trên AWS, phổ biến là Amazon EventBridge, Amazon SNS/SQS, Amazon Kinesis cho các use case real‑time analytics, integration giữa nhiều domain service.
- Phù hợp cho các quy trình nghiệp vụ phức tạp (order, payment, notification, audit log…) và xử lý streaming data trong kiến trúc hiện đại.

#### Compute Evolution

- Hành trình từ EC2 truyền thống sang containers (ECS/EKS), serverless (Lambda, Fargate), và các optimized instance cho AI/HPC như Trainium3 UltraServers.
- Mục tiêu là tối ưu chi phí, tự động scale, giảm effort vận hành infra để team tập trung vào logic nghiệp vụ và giá trị cho khách hàng.

#### Amazon Q Developer

- Amazon Q Developer là AI assistant cho developer, tích hợp IDE và AWS console, hỗ trợ sinh code, refactor, tạo test, và gợi ý kiến trúc dựa trên best practice AWS.
- Giúp tăng tốc hiện đại hóa bằng cách phân tích code legacy, đề xuất migration path, và tự động hoá một số tác vụ hạ tầng (infrastructure as code, config).

### Những Gì Học Được

#### Tư Duy Thiết Kế

- **Thiết kế cloud‑native first**: Ưu tiên decoupling, elasticity, fault‑tolerance, automation thay vì chỉ "lift‑and‑shift" từ on‑prem lên cloud.
- **Suy nghĩ theo domain‑driven design**: Tách bounded context rõ ràng trước khi chuyển sang microservices và event‑driven.

#### Kiến Trúc Kỹ Thuật

- **Kiến trúc kết hợp**: Microservices + event‑driven + serverless/containers + managed data services (Aurora, DynamoDB, streaming, vector DB).
- **Áp dụng patterns về resilience**: Circuit breaker, retry, backoff, idempotency; observability end‑to‑end và security by design cho từng service.

#### Chiến Lược Hiện Đại Hóa

- **Bắt đầu bằng đánh giá**: Xác định các domain có giá trị kinh doanh cao để "strangle" dần sang kiến trúc mới.
- **Kết hợp CI/CD và feature flags**: Blue/green deployment để giảm rủi ro khi migrate từng phần hệ thống, thay vì big‑bang rewrite.

### Ứng Dụng Vào Công Việc

- **Áp dụng tư duy decomposition monolith** của công ty/tổ chức thành các domain rõ ràng, từ đó đề xuất kiến trúc microservices hoặc modular monolith.
- **Đề xuất sử dụng các dịch vụ AWS phù hợp** (ví dụ: API Gateway + Lambda cho POC, hoặc ECS/EKS cho hệ thống lớn), kèm thêm event‑driven bằng SQS/EventBridge khi tích hợp nhiều hệ thống.
- **Bắt đầu thử Amazon Q Developer** trong quy trình development để hỗ trợ viết code, test, refactor, và học theo các snippet/best practice nó gợi ý.

### Trải Nghiệm Trong Event

#### Học hỏi từ các diễn giả có chuyên môn cao
- Đánh giá cao cách các speaker AWS và khách hàng chia sẻ real‑world implementation, bài học về failure, scaling challenges, và cost optimization.

#### Trải nghiệm kỹ thuật thực tế
- Được thực hành với các dịch vụ AWS qua lab và workshop: serverless, container orchestration, data services, AI/Bedrock, và Amazon Q Developer demonstrations.

#### Ứng dụng công cụ hiện đại
- Ấn tượng với hệ sinh thái GenAI (Nova models, Bedrock, AI agents) và công cụ Dev‑tool như Amazon Q Developer, AWS CI/CD pipelines, và DevOps automation.

#### Kết nối và trao đổi
- Kết nối với AWS experts, đối tác, cộng đồng VietAWS, sinh viên và engineers từ các công ty khác, trao đổi về các bài toán modernization và giải pháp.

#### Bài học rút ra
- **Thiết kế cho failure**: Xây dựng resilience và observability vào hệ thống từ đầu.
- **Migration phải theo từng bước nhỏ có đo lường**: Tránh big‑bang rewrites; sử dụng gradual migration với feature flags và canary deployments.
- **AI/GenAI là phần mở rộng của kiến trúc, không phải add‑on**: Tích hợp AI một cách có ý thức vào quy trình và thiết kế hệ thống, không phải suy nghĩ thêm sau.

#### Một số hình ảnh khi tham gia sự kiện

**Figure 1: Toàn cảnh venue sự kiện và session khai mạc**
![Event Overview](/images/3-EventParticipated/3.3-Event3/reInvent_RECAP_1.jpg)

**Figure 2: Check-in Session #1**
![Microservices Architecture](/images/3-EventParticipated/3.3-Event3/reInvent_RECAP_2.jpg)

**Figure 3: Check-in Session #2**
![Modernization Strategy](/images/3-EventParticipated/3.3-Event3/reInvent_RECAP_3.jpg)

**Figure 4: Giới thiệu các dịch vụ AWS: Bài phát biểu chính về Học máy/Trí tuệ nhân tạo & Đổi mới #1**
![GenAI Demo](/images/3-EventParticipated/3.3-Event3/reInvent_RECAP_4.jpg)

**Figure 5: Giới thiệu các dịch vụ AWS: Bài phát biểu chính về Học máy/Trí tuệ nhân tạo & Đổi mới #2**
![Networking Session](/images/3-EventParticipated/3.3-Event3/reInvent_RECAP_5.jpg)

**Figure 6: Nụ cười ngày đầu năm – Sẵn sàng cho những thử thách và cột mốc mới tại AWS!**
![AWS Booth](/images/3-EventParticipated/3.3-Event3/reInvent_RECAP_6.jpg)

**Figure 7: Hình chụp đồng đội và kết thúc buổi event**
![Team Picture](/images/3-EventParticipated/3.3-Event3/reInvent_RECAP_7.jpg)

> Tổng thể, sự kiện nhấn mạnh tầm quan trọng của tư duy kiến trúc hiện đại, chiến lược migration thực tế, và vai trò của các dịch vụ AWS trong việc xây dựng các ứng dụng scalable, secure, và có khả năng trí tuệ nhân tạo.
