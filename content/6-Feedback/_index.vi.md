---
title: "Chia sẻ, đóng góp ý kiến"
date: 2026-03-31
weight: 6
chapter: false
pre: " <b> 6. </b> "
---

### Đánh giá chung

**1. Môi trường làm việc**  
Điều ấn tượng nhất với mình là một môi trường cực kỳ năng động khi phát triển kiến trúc microservices. Lúc đầu, khi phải kết nối backend Go, frontend React, database MySQL, và message queue RabbitMQ, mình thật sự bị choáng ngợp bởi độ phức tạp của hệ thống phân tán. Tuy nhiên, một cộng đồng hỗ trợ nhiệt tình và sự hướng dẫn kỷ luật của các mentor đã giúp mình vượt qua. Một gợi ý cho các bạn: mình rất mong muốn có thêm các buổi **Peer Code Review** có tổ chức, nơi mà các bạn thực tập sinh có thể học hỏi các mẫu code tối ưu và tư duy kiến trúc từ nhau—điều này sẽ giúp gia tăng quá trình truyền đạt kiến thức.

**2. Sự hỗ trợ của mentor / team admin**  
Mình thật sự rất trân trọng cách hướng dẫn của các mentor. Thay vì chỉ sửa lỗi, các anh chị đã dạy mình cách tư duy có hệ thống về vấn đề—phân tích log để tìm ra race condition, hiểu rõ ý tưởng pessimistic locking, và đưa ra quyết định thiết kế database hợp lý. Hướng dẫn của các mentor về cách dùng `SELECT FOR UPDATE` để triệt tiêu vấn đề concurrency đặc biệt là sáng tỏ. Team admin cũng xứng đáng được khen ngợi vì phối hợp kịp thời và tài liệu rõ ràng.

**3. Sự phù hợp giữa công việc và chuyên ngành học**  
Ngành học của mình là **Kỹ thuật Phần mềm tại ĐH FPT**, và thực tập này hoàn toàn khớp với chuyên ngành. Xây dựng một hệ thống chuẩn sản xuất với đầy đủ luồng—từ xác thức người dùng, xử lý thanh toán cho đến check-in QR—đã giúp mình hiểu sâu các nguyên lý SE như thiết kế hệ thống, phân tích trade-off, và chiến lược kiểm thử. Kinh nghiệm thực tế này là nền tảng vô cùng quý giá cho đồ án tốt nghiệp sắp tới cũng như cho sự nghiệp xây dựng các backend system quy mô lớn.

**4. Cơ hội học hỏi & phát triển kỹ năng**  
13 tuần là một cuộc marathon đòi hỏi kỷ luật và lập kế hoạch chặt chẽ. Bên cạnh kỹ năng kỹ thuật, mình đã phát triển **Kỹ năng Đưa Ra Quyết Định Kỹ Thuật**—một năng lực quan trọng phân biệt junior developer với senior engineer. Ví dụ tiêu biểu: mình lúc đầu muốn dùng WebSocket cho real-time updates nhưng sau đó chuyển sang giải pháp Cache Busting & Delay Refetch khi gặp vấn đề ổn định. Quyết định đó dạy mình cân bằng các ambition về tính năng với độ tin cậy của hệ thống. Ngoài ra, mình cũng rèn luyện được khả năng đọc tài liệu kỹ thuật và tự debug thông qua log một cách độc lập.

**5. Văn hóa & tinh thần đồng đội**  
Tinh thần hợp tác rất rõ rệt xuyên suốt thực tập. Hễ ai gặp bug phức tạp và post lên Slack, những người khác sẽ nhanh chóng tham gia để brainstorm. Tư duy giải quyết vấn đề tập thể này đẩy nhanh quá trình học hỏi và tạo ra cảm giác sở hữu chung cho dự án.


### Một số chia sẻ thêm

- **Điều khiến mình hài lòng nhất:** Sự chuyển mình từ một developer chỉ biết viết các đoạn code cô lập thành một người có khả năng thiết kế hệ thống phân tán (Distributed System) chạy ổn định trên Docker với nhiều microservices. Nhìn thấy toàn bộ pipeline sản xuất hoạt động mượt mà—các giao dịch thanh toán được xử lý an toàn, các lần check-in được ghi nhận tức thì—thực sự vô cùng bứt phá.
- **Lời khuyên cho khóa sau:** Hãy chấp nhận độ phức tạp thay vì sợ nó. Đọc log như đọc tiểu thuyết; chúng sẽ nói cho bạn biết chính xác có gì sai. Đừng cấu tạo công nghệ mới nếu nó làm ảnh hưởng đến ổn định hệ thống. Độ tin cậy của hệ thống quan trọng hơn sự tinh xảo của nó.

### Lời kết

Thực tập này không chỉ trao cho mình kiến thức kỹ thuật mà còn trao cho mình sự tự tin trong khả năng thiết kế các hệ thống thực tế. Mình chân thành cảm ơn tất cả các mentor, team lead, và những thực tập sinh khác đã hỗ trợ mình trong suốt 13 tuần này. Nếu có cơ hội, mình sẽ rất nhiệt tình truyền đạt lại kiến thức và những giá trị mà kinh nghiệm này đã cho mình cho thế hệ sau.