---
title: "Event 1"
date: 2026-03-31
weight: 1
chapter: false
pre: " <b> 4.1. </b> "
---

{{% notice warning %}}
⚠️ **Lưu ý:** Các thông tin dưới đây chỉ nhằm mục đích tham khảo, vui lòng **không sao chép nguyên văn** cho bài báo cáo của bạn kể cả warning này.
{{% /notice %}}

# Bài thu hoạch “GenAI-powered Cloud-Mastery 2026 workshop”

#### Một số hình ảnh khi tham gia sự kiện
 * Một số ảnh từ buổi workshop:
 
 ![Workshop photo 1](/images/4-EventParticipated/4.1-Event1/photo-1.jpg)
 ![Workshop photo 2](/images/4-EventParticipated/4.1-Event1/photo-2.jpg)
 ![Workshop photo 3](/images/4-EventParticipated/4.1-Event1/photo-3.jpg)
> Tổng thể, sự kiện không chỉ cung cấp kiến thức kỹ thuật mà còn giúp tôi thay đổi cách tư duy về thiết kế ứng dụng, hiện đại hóa hệ thống và phối hợp hiệu quả hơn giữa các team.

---

## 1. Building AI Agent with Strands (Banh Cam Vinh)

### Mục tiêu sự kiện

 - Giới thiệu khái niệm nền tảng về **LLM** và giới hạn của **LLM** khi hoạt động độc lập.
 - Trình bày vì sao cần thiết kế **AI Agent** (**multi-step reasoning**, **tool integration**, **autonomous behaviour**).
 - Giới thiệu **Strands Agents**: workflow, loại **tools**, chuẩn mở và cách **Strands** giảm "glue code".

 - Giới hạn của **standalone LLM**: chỉ trả lời chat, thiếu trạng thái dài hạn, không kết nối API/DB, khó xử lý quy trình nhiều bước.
 - Kết nối **LLM** với thế giới thật qua **tools**: **API**, **database**, external services để biến **LLM** thành agent có khả năng hành động.
 - Định nghĩa **AI Agent**: **LLM** làm "bộ não" nhưng cần khả năng **lập kế hoạch**, **gọi tools**, đọc kết quả và lặp lại đến khi hoàn thành task.
 - **Strands Agents** cung cấp workflow chuẩn, bộ công cụ và chuẩn provider open-standard, giúp định nghĩa **tool** và **agentic loop** nhanh và an toàn hơn.
 - "Generic prompts → Generic outputs"; cần cấu trúc prompt gồm: **Role**, **Instruction**, **Context**, **Input Data**, **Output Format**, **Examples**, **Constraints**.
 - Ví dụ cụ thể: cách viết prompt cho bài tóm tắt hoặc tự giới thiệu để có kết quả rõ ràng, tiết kiệm token.
 - Kỹ thuật nâng cao: **Chain-of-Thought (CoT)**, **Self-Consistency**, **Tree-of-Thoughts (ToT)**, **Retrieval-Augmented Generation (RAG)**, **Role Prompting**.
 - Demo **Proptimizer**: extension tối ưu prompt tự động, kiến trúc dùng **CloudFront**, **S3**, **Cognito**, **API Gateway**, **Lambda**.
### Nội dung nổi bật
 - Để **LLM** thực sự "làm việc", cần thiết kế **agent** chứ không chỉ tối ưu prompt.
 - **Tool calling** và **agentic loop** là lõi: **LLM** lập kế hoạch → chọn **tool** → gọi **tool** → phân tích kết quả → lặp.
 - **Strands** giảm đáng kể công sức viết "glue code" khi xây hệ thống **agent-based**.
- Định nghĩa AI Agent: LLM làm "bộ não" nhưng cần khả năng lập kế hoạch, gọi tools, đọc kết quả và lặp lại đến khi hoàn thành task.
- Strands Agents cung cấp workflow chuẩn, bộ công cụ và chuẩn provider open-standard, giúp định nghĩa tool và agentic loop nhanh và an toàn hơn.

### Bài học rút ra

- Để LLM thực sự "làm việc", cần thiết kế agent chứ không chỉ tối ưu prompt.
- Tool calling và agentic loop là lõi: LLM lập kế hoạch → chọn tool → gọi tool → phân tích kết quả → lặp.
- Strands giảm đáng kể công sức viết "glue code" khi xây hệ thống agent-based.

### Ứng dụng

- Xây chatbot nội bộ (FAQ, IT support, CS): cho phép bot gọi API ticket/HR/CRM thay vì chỉ trả lời text.
- Xử lý workflow nhiều bước (onboarding, đăng ký dịch vụ): dùng agent để orchestration các action tự động.
- Map API/service nội bộ thành tools, để agent điều phối thay vì viết logic thủ công.

### Trải nghiệm

- Nội dung lý thuyết nhưng rất thực tiễn, phù hợp cho người đã có nền tảng LLM và muốn triển khai hệ thống agent trong thực tế.

---

## 2. Automated Prompt Engineering: Enhancing LLM Output Quality (Nguyen Tuan Thinh)

### Mục tiêu sự kiện

 - Giải thích tầm quan trọng của **prompt engineering** để tối ưu chất lượng output và chi phí token.
 - Hệ thống hóa các thành phần của prompt "xịn" và giới thiệu kỹ thuật nâng cao (**CoT**, **RAG**, **ToT**, ...).
 - Demo **Proptimizer** (extension) và kiến trúc hạ tầng trên **AWS**.

### Diễn giả

- Nguyen Tuan Thinh – DevOps Engineer, First Cloud AI Journey.

### Nội dung nổi bật

- "Generic prompts → Generic outputs"; cần cấu trúc prompt gồm: Role, Instruction, Context, Input Data, Output Format, Examples, Constraints.
- Ví dụ cụ thể: cách viết prompt cho bài tóm tắt hoặc tự giới thiệu để có kết quả rõ ràng, tiết kiệm token.
- Kỹ thuật nâng cao: Chain-of-Thought (CoT), Self-Consistency, Tree-of-Thoughts (ToT), Retrieval-Augmented Generation (RAG), Role Prompting.
- Demo Proptimizer: extension tối ưu prompt tự động, kiến trúc dùng CloudFront, S3, Cognito, API Gateway, Lambda.

### Bài học rút ra

- Prompt engineering là kỹ năng cốt lõi: coi prompt như specification (role, task, context, format, examples, constraints).
- Tối ưu prompt giúp giảm chi phí token và tăng độ ổn định/độ chính xác của model.
- Kỹ thuật CoT/RAG/ToT giúp cải thiện reasoning, không chỉ dựa vào một câu trả lời đơn thuần.

### Ứng dụng

- Khi xây các tác vụ AI (code, tóm tắt, phân tích), dùng khung prompt chuẩn để đạt kết quả đáng tin cậy.
- Chuẩn hóa template prompt + logging cho sản phẩm production để tối ưu dần dựa trên dữ liệu thực.
- Tham khảo kiến trúc Proptimizer nếu muốn build tool hỗ trợ người dùng tối ưu prompt trên web.

### Trải nghiệm

- Slide thực dụng, nhiều ví dụ cụ thể, dễ áp dụng cho cả người mới lẫn người đã dùng AI nhiều.

---

## 3. AIoT Project: Locker Management (Aiden Dinh)

### Mục tiêu sự kiện

- Trình bày một dự án AIoT thực tế: hệ thống quản lý locker tích hợp sensor, RFID và AI để tự động hoá mượn/trả đồ.
- Chia sẻ kiến trúc hardware + cloud (AWS), flow dữ liệu, và demo hoạt động.

### Diễn giả

- Aiden Dinh – Katalon Operation Engineer, "AI-Powered Projects – AIoT Project: Locker Management".

### Nội dung nổi bật

- Bài toán: tự động hoá quy trình mượn đồ cho club/nhóm, giảm phụ thuộc manager.
 - Kiến trúc: **Arduino** (edge) + **Raspberry Pi** (controller, **MQTT**) + sensors (reed switch, **RFID**) + camera.
 - Cloud: **AWS IoT Core (MQTT)**, **S3** (lưu ảnh), **DynamoDB** (thông tin thành viên), **Lambda** (**Rekognition**), **Amplify** (monitoring UI).
 - Flow: **RFID** và sensor tạo event → ảnh chụp → **Lambda** gọi **Rekognition** so sánh với collection → ghi giao dịch vào **DB**.

### Bài học rút ra

- Kết hợp sensing, connectivity và AI giải quyết bài toán quản lý vật lý hiệu quả.
- Rekognition + RFID giúp log mượn đồ minh bạch: ai, lúc nào, mượn món gì.
- AWS IoT Core và các dịch vụ serverless giúp mở rộng hệ thống cho nhiều locker/địa điểm.

### Ứng dụng

- Áp dụng cho quản lý kho thiết bị lab, smart cabinet trong công ty, hệ thống mượn/trả tự động.
- Mô hình này là case study tốt cho đồ án IoT/Cloud hoặc portfolio cá nhân.

### Trải nghiệm

- Buổi trình bày mang tính showcase: từ problem → mission → kiến trúc → cost → demo, rất phù hợp để lấy cảm hứng làm đồ án.

