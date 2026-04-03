---
title: "Tự đánh giá"
date: 2026-03-31
weight: 5
chapter: false
pre: " <b> 5. </b> "
---

Nhìn lại hành trình 13 tuần phát triển hệ thống **FPT Event Management** từ ngày **05/01/2026** đến **05/04/2026** đã mang lại cho mình một kinh nghiệm học tập sâu sắc. Thực tập này đã đẩy mình vượt ra ngoài những kỹ năng backend cơ bản để thiết kế và triển khai kiến trúc microservices chuẩn sản phẩm sử dụng **Go, React, MySQL, RabbitMQ, và Docker**.

Thông qua quá trình triển khai trực tiếp các tính năng cốt lõi—từ xây dựng hệ thống thanh toán vững chắc với cơ chế Double-Lock cho đến giải quyết hoàn toàn lỗi race condition bằng kỹ thuật Pessimistic Locking (SELECT FOR UPDATE)—mình đã phát triển một sự hiểu biết sâu sắc hơn về các cân nhắc trong thiết kế hệ thống. Quan trọng hơn, mình học được cách ra quyết định thực tế: khi triển khai WebSocket gặp vấn đề ổn định, mình đã nhanh chóng chuyển hướng sang giải pháp Cache Busting & Delay Refetch đạt được trải nghiệm người dùng tốt hơn mà vẫn giữ được độ tin cậy.

Beyond technical execution, the collaborative environment and mentorship have reinforced the importance of proactive problem-solving, rigorous documentation study, and effective teamwork in delivering quality software.

Để có cái nhìn khách quan nhất về sự trưởng thành của mình với tư cách là một Backend Engineer, mình xin đưa ra một số tự đánh giá chi tiết theo các tiêu chí sau:

| STT | Tiêu chí                            | Mô tả                                                                                            | Tốt | Khá | Trung bình |
| --- | ----------------------------------- | ------------------------------------------------------------------------------------------------ | :---: | :---: | :----------: |
| 1   | **Kiến thức và kỹ năng Backend** | Thành thạo Go, tối ưu hóa truy vấn MySQL, thiết kế microservices vững chắc với RabbitMQ | ✅   | ☐   | ☐          |
| 2   | **Tư duy giải quyết vấn đề**                | Nhanh chóp bắt nhịp các mô hình concurrency, chiến lược locking database, và đưa ra quyết định kiến trúc thông minh | ✅   | ☐   | ☐          |
| 3   | **Tính chủ động**                        | Tự mình debug lỗi race condition và các vấn đề ổn định, nghiên cứu giải pháp mà không chờ hướng dẫn | ✅   | ☐   | ☐          |
| 4   | **Chất lượng code và trách nhiệm**           | Commit code được kiểm thử kỹ lưỡng, thực hiện code review đầy đủ, và hoàn thành deadline sprintĐúng | ✅   | ☐   | ☐          |
| 5   | **Kỷ luật kỹ thuật**                         | Tuân thủ SOLID principles, áp dụng design patterns, và tuân theo các quy ước dự án | ✅   | ☐   | ☐          |
| 6   | **Tính cầu tiến**                   | Hành động dựa trên nhận xét từ code review, lặp đi lặp lại các quyết định kiến trúc, tìm tòi kiến thức ngoài vùng thoải mái | ✅   | ☐   | ☐          |
| 7   | **Kỹ năng truyền đạt kỹ thuật**                       | Giải thích rõ ràng các quyết định thiết kế hệ thống, tài liệu hóa logic phức tạp, trình bày các cân nhắc cho nhóm | ☐   | ✅   | ☐          |
| 8   | **Hợp tác nhóm**                    | Hỗ trợ đồng nghiệp qua code review, pair debugging, và chia sẻ kiến thức | ✅   | ☐   | ☐          |
| 9   | **Chuẩn mực chuyên nghiệp**            | Giữ code sạch, tuân thủ hướng dẫn kiến trúc, phản hồi nhanh chóng các yêu cầu review | ✅   | ☐   | ☐          |
| 10  | **Tư duy hệ thống**        | Phân tích các bottleneck hiệu suất thông qua log và metrics, thiết kế giải pháp có khả năng mở rộng | ☐   | ✅   | ☐          |
| 11  | **Đóng góp dự án**                   | Triển khai hệ thống Event Management sản phẩm có các tính năng quan trọng (xử lý thanh toán, hệ thống check-in) | ✅   | ☐   | ☐          |
| 12  | **Tổng thể**                        | Tự hào về sự trưởng thành kỹ thuật và chất lượng phần mềm được triển khai với tư cách Backend Engineer | ✅   | ☐   | ☐          |

### Những điểm cần tiếp tục hoàn thiện

- **Kiến thức về hạ tầng Cloud**: Cần nâng cao kiến thức về AWS ALB (Application Load Balancer) và cấu hình reverse proxy Nginx để có thể triển khai WebSocket một cách ổn định hơn trong các dự án tương lai.
- **Cân bằng giữa tốc độ phát triển và Unit Test**: Tăng cường độ phủ sóng test cho các luồng quan trọng về bảo mật (xác thực thanh toán, kiểm chứng check-in) mà không làm giảm tốc độ phát triển.
- **Kỹ năng diễn giải kỹ thuật**: Rèn luyện khả năng giải thích những khái niệm phức tạp như race condition và pessimistic locking một cách đơn giản và dễ hiểu cho những người không có nền tảng kỹ thuật sâu.