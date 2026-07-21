---
title: "Event 1"
date: 2026-05-23
weight: 1
chapter: false
pre: " <b> 4.1. </b> "
---

# Bài thu hoạch: AWS Vietnam Community Day 2026

### Thông tin sự kiện

**AWS Vietnam Community Day 2026** là sự kiện cộng đồng về AWS, Cloud Computing và Generative AI. Sự kiện có nhiều phiên chia sẻ từ các anh chị đang làm trong ngành, gồm Platform Engineer, Solution Architect, DevOps Engineer, Business Systems Analyst và AWS Community Builder.

Điều tôi quan tâm nhất ở sự kiện này là cách các diễn giả liên hệ kiến thức cloud và AI với các bài toán thực tế. Nội dung không chỉ nói về dịch vụ AWS, mà còn có các câu chuyện về cách xây dựng sản phẩm, cách làm việc trong hackathon, cách thiết kế hệ thống AI và cách nhìn nhận rủi ro khi dùng LLM.

### Danh sách diễn giả

- **Tinh Truong** - Platform Engineer, GoTymeX  
  Chủ đề: *Context Is Everything*

- **Pham Ng Hai Anh** - AWS Community Builder, G-AsiaPacific Vietnam  
  Chủ đề: *Friendly AI Assistant with Amazon Quick*

- **Nguyen Tuan Thinh** - DevOps Engineer, First Cloud AI Journey  
  Chủ đề: *From Edge to Origin: CloudFront as Your Foundation*

- **Team VIB**  
  Chủ đề: *36 Hours with LotusHacks - Building UTMorpho from Idea to Reality*

- **Duc Dao** - Solution Architect, Cloud Kinetics  
  Chủ đề: *Deep Dive Talk: How LLM Actually Works?*

- **Vy Lam** - Senior Business Systems Analyst, VPBank  
  Chủ đề: *Enterprise-Grade Multi-Agent System: The Case of Startup Credit Scoring*

### Nội dung tôi ghi nhận được

#### Context Is Everything

Phần chia sẻ của anh **Tinh Truong** giúp tôi hiểu rõ hơn vai trò của context khi làm việc với Generative AI. Trước đây tôi thường nghĩ chỉ cần viết prompt đủ dài thì kết quả sẽ tốt hơn. Sau session này, tôi hiểu rằng context cần đúng trọng tâm, có mục tiêu rõ và phải cung cấp thông tin liên quan đến bài toán.

Một vài điểm tôi ghi chú lại:

- AI trả lời chưa tốt nhiều khi không phải do model yếu, mà do context đầu vào chưa rõ.
- Context nhiều không đồng nghĩa với context tốt.
- Khi xây dựng ứng dụng AI, cần nghĩ đến memory, retrieval và cách hệ thống lưu lại thông tin có ích.
- Ý tưởng “Second AI Brain” cho thấy AI có thể hỗ trợ lưu trữ, tìm lại và xử lý tri thức cá nhân hoặc tổ chức.

Nội dung này có thể áp dụng trực tiếp khi tôi dùng AI để học AWS, đọc tài liệu hoặc debug lỗi. Nếu đặt câu hỏi rõ hơn và cung cấp log, mục tiêu, môi trường chạy, kết quả nhận được thì câu trả lời sẽ hữu ích hơn.

#### Friendly AI Assistant with Amazon Quick

Phần của anh **Pham Ng Hai Anh** giới thiệu cách Amazon Quick Suite có thể hỗ trợ người dùng doanh nghiệp trong các công việc như tổng hợp thông tin, tạo ghi chú cuộc họp, gửi email hoặc tự động hóa một số quy trình lặp lại.

Điểm tôi thấy đáng chú ý là AI assistant trong doanh nghiệp không chỉ cần trả lời câu hỏi, mà còn phải kết nối được với dữ liệu, có action để thực hiện tác vụ và có guardrails để kiểm soát kết quả. Điều này khác với việc dùng chatbot thông thường vì môi trường doanh nghiệp cần bảo mật, phân quyền và khả năng kiểm soát tốt hơn.

#### From Edge to Origin: CloudFront as Your Foundation

Session của anh **Nguyen Tuan Thinh** giúp tôi nhìn Amazon CloudFront rộng hơn so với khái niệm CDN ban đầu. CloudFront không chỉ dùng để cache nội dung tĩnh, mà còn hỗ trợ bảo mật, hiệu năng, độ tin cậy và tối ưu chi phí cho hệ thống web.

Các ý chính tôi ghi nhận:

- Edge caching giúp giảm tải cho origin và cải thiện tốc độ phản hồi.
- AWS WAF và DDoS protection giúp tăng lớp bảo vệ cho ứng dụng.
- HTTP/3 và QUIC có thể cải thiện hiệu năng kết nối.
- Signed URLs, mTLS, origin failover và stale cache là các tính năng hữu ích khi thiết kế hệ thống production.
- Việc hiểu pricing cũng quan trọng vì hệ thống cloud có thể phát sinh chi phí nếu thiết kế chưa hợp lý.

Phần này liên quan khá nhiều đến nội dung tôi đã học trong FCAJ về CloudFront, S3, Route 53 và HTTPS.

#### 36 Hours with LotusHacks - Building UTMorpho from Idea to Reality

**Team VIB** chia sẻ quá trình xây dựng UTMorpho trong 36 giờ tại LotusHacks. Đây là một công cụ AI hỗ trợ tạo giao diện và cho phép chỉnh sửa trực tiếp trên canvas.

Điều tôi thích ở phần này là câu chuyện bắt đầu từ một khó khăn thật khi làm sản phẩm, sau đó nhóm biến khó khăn đó thành ý tưởng hackathon. Qua đó tôi thấy khi làm sản phẩm, ý tưởng không nhất thiết phải quá lớn ngay từ đầu. Quan trọng hơn là phải xác định đúng vấn đề, chia việc nhanh và liên tục kiểm tra kết quả.

Một số bài học tôi rút ra:

- Hackathon cần sự phối hợp tốt giữa các thành viên.
- AI có thể đóng vai trò như một teammate để hỗ trợ tạo ý tưởng và tăng tốc phát triển.
- Khi xây dựng sản phẩm AI, cần chú ý chi phí token và tính nhất quán của giao diện.
- Demo cần tập trung vào luồng chính thay vì cố làm quá nhiều tính năng.

#### Deep Dive Talk: How LLM Actually Works?

Phần của anh **Duc Dao** giải thích cách LLM sinh văn bản theo từng token. Nội dung này giúp tôi hiểu vì sao cùng một prompt nhưng kết quả đôi khi vẫn khác nhau, kể cả khi temperature được đặt thấp.

Các điểm quan trọng:

- LLM dự đoán token tiếp theo dựa trên xác suất.
- Temperature ảnh hưởng đến mức độ ngẫu nhiên trong quá trình chọn token.
- Temperature 0 không có nghĩa là kết quả luôn giống nhau tuyệt đối.
- Sự khác nhau nhỏ có thể đến từ floating-point calculation trên GPU hoặc inference batching.
- Khi xây dựng ứng dụng dùng LLM, developer cần chấp nhận một mức độ variance nhất định.

Điểm này khá quan trọng vì nó nhắc tôi không nên thiết kế hệ thống AI như một hàm luôn trả về kết quả cố định. Nếu cần độ ổn định cao, hệ thống phải có kiểm tra, ràng buộc output và bước review.

#### Enterprise-Grade Multi-Agent System

Phần chia sẻ của chị **Vy Lam** nói về hệ thống multi-agent cho bài toán chấm điểm tín dụng startup. Thay vì dùng một agent duy nhất, hệ thống tách thành nhiều agent chuyên xử lý từng góc nhìn khác nhau.

Các agent được nhắc đến gồm:

- Financial Analyst Agent
- Market Analyst Agent
- Team Evaluator Agent
- Risk Assessor Agent
- Compliance Agent

Cách thiết kế này giúp hệ thống dễ audit hơn, rõ trách nhiệm hơn và phù hợp với bài toán enterprise vì quyết định không chỉ dựa trên một tiêu chí. Tôi thấy đây là một ví dụ dễ hiểu về lý do vì sao multi-agent system cần thiết trong các bài toán phức tạp.

### Bài học sau sự kiện

Sau khi tham gia sự kiện, tôi rút ra một số bài học chính:

- Khi dùng Generative AI, context và cách đặt vấn đề ảnh hưởng lớn đến chất lượng kết quả.
- CloudFront có thể đóng vai trò quan trọng trong bảo mật, hiệu năng và độ tin cậy của hệ thống.
- LLM không hoàn toàn deterministic, nên ứng dụng AI cần có cơ chế kiểm tra và kiểm soát output.
- Multi-agent architecture phù hợp với các bài toán cần phân tích từ nhiều góc độ.
- Một sản phẩm AI tốt nên bắt đầu từ vấn đề thực tế, không chỉ từ công nghệ.

### Liên hệ với quá trình học FCAJ

Nội dung sự kiện giúp tôi liên hệ lại với các phần đã học trong chương trình FCAJ như CloudFront, S3, IAM, bảo mật và thiết kế hệ thống. Trước đó tôi chỉ hiểu CloudFront chủ yếu là dịch vụ phân phối nội dung. Sau sự kiện, tôi hiểu thêm rằng khi xây dựng hệ thống thật, CloudFront còn liên quan đến bảo mật, kiểm soát truy cập, failover và chi phí.

Với định hướng backend và cloud, sự kiện này giúp tôi có thêm động lực học sâu hơn về AWS, Generative AI và kiến trúc hệ thống. Tôi cũng nhận ra rằng ngoài việc biết dùng dịch vụ, cần hiểu lý do chọn dịch vụ đó và ảnh hưởng của nó đến vận hành thực tế.

### Cảm nhận cá nhân

Tôi thấy **AWS Vietnam Community Day 2026** là một sự kiện hữu ích vì nội dung khá đa dạng và gần với thực tế. Các diễn giả không chỉ trình bày khái niệm mà còn chia sẻ ví dụ, kinh nghiệm và vấn đề gặp phải khi làm sản phẩm hoặc triển khai hệ thống.

Sau sự kiện, tôi có cái nhìn rõ hơn về xu hướng kết hợp giữa Cloud Computing và Generative AI. Đây cũng là phần giúp tôi định hướng rõ hơn trong việc học backend, cloud deployment, AI assistant và các hệ thống có khả năng mở rộng.

### Hình ảnh tham gia

![Hình ảnh tham gia sự kiện 1](/images/4-EventParticipated/event1.jpg)