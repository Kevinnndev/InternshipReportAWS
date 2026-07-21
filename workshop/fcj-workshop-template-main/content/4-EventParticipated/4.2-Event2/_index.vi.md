---
title: "Event 2"
date: 2026-06-27
weight: 2
chapter: false
pre: " <b> 4.2. </b> "
---

# Bài thu hoạch: Cloud, AI Agent và Amazon Q trên AWS

### Thông tin sự kiện

Sự kiện **Cloud, AI Agent và Amazon Q trên AWS** tập trung vào cách AI Agent được ứng dụng trong các hệ thống thực tế trên AWS. Nội dung sự kiện trải rộng từ định hướng nghề nghiệp cloud, Voice Agent, DevOps AI Agent, Amazon Q trong quản trị nhân sự đến bảo mật kết nối bằng Private Connection.

Điểm tôi thấy khác biệt ở sự kiện này là có nhiều phần demo cụ thể. Thay vì chỉ nói về khái niệm AI Agent, các diễn giả cho thấy AI có thể tham gia vào những công việc khá gần với môi trường doanh nghiệp như hỗ trợ khách hàng bằng giọng nói, phân tích incident, xử lý CV hoặc bảo vệ luồng kết nối với hệ thống nội bộ.

### Danh sách diễn giả

- **Steve Trần** - Founder của Cloud Thinker  
  Chủ đề: *Con đường sự nghiệp với Cloud và giới thiệu Cloud Thinker*

- **Hiếu Nghị** - Renova Cloud  
  Chủ đề: *Xây dựng trợ lý giọng nói bằng AI*

- **Kiệt** - AWS Study Group  
  Chủ đề: *Voice Agent và ứng dụng AI trên AWS*

- **Trung Nguyễn** - Founder & CEO của R AI  
  Chủ đề: *Triển khai Voice AI cho tiếng Việt*

- **Bảo** - Cloud Kinetic  
  Chủ đề: *Tìm hiểu về AWS DevOps AI Agent*

- **Nguyên Nguyễn** - Cloud Engineer, Cloud Kinetic  
  Chủ đề: *DevOps AI Agent và xử lý incident trên AWS*

- **Trường** - Solution Architect, Noventic  
  Chủ đề: *Ứng dụng Amazon Q trong quản trị nhân sự*

- **Minh Anh** - Solution Architect, Noventic  
  Chủ đề: *Amazon Q và tự động hóa quy trình HR*

- **Toàn Nguyễn** - AWS Security Builder  
  Chủ đề: *Thiết lập bảo mật cho Amazon Q với Private Connection*

### Nội dung tôi ghi nhận được

#### Con đường sự nghiệp với Cloud và Cloud Thinker

Phần mở đầu của anh **Steve Trần** nói nhiều về hành trình học cloud và phát triển sự nghiệp. Điều tôi nhớ nhất là việc học cloud không phải lúc nào cũng đi thẳng. Diễn giả chia sẻ cả những lần gặp khó khăn, thi chứng chỉ chưa đạt, chuyển hướng công nghệ và sau đó tiếp tục phát triển trong lĩnh vực AWS.

Từ phần này, tôi rút ra rằng cloud là một lĩnh vực cần học lâu dài. Ngoài việc biết dùng dịch vụ, người học cần hiểu hệ thống, biết xử lý vấn đề và biết cập nhật công nghệ mới. Trong bối cảnh AI phát triển nhanh, kỹ sư cloud hoặc backend cũng cần biết cách dùng AI để hỗ trợ công việc, nhưng vẫn phải giữ nền tảng kỹ thuật vững.

Diễn giả cũng giới thiệu **Agentic Platform** của Cloud Thinker, hướng đến các bài toán như xử lý sự cố, review code, tối ưu chi phí cloud theo FinOps và kiểm thử bảo mật. Phần so sánh giữa Single Agent và Multi-Agent giúp tôi hiểu rằng không phải bài toán nào cũng nên dùng một agent duy nhất. Với những việc phức tạp, chia nhỏ vai trò cho nhiều agent có thể giúp hệ thống dễ kiểm soát hơn.

#### Xây dựng trợ lý giọng nói bằng AI

Các phần chia sẻ của **Hiếu Nghị**, **Kiệt** và **Trung Nguyễn** giúp tôi hiểu rõ hơn về kiến trúc Voice Agent. Một hệ thống Voice AI thường gồm ba phần chính: Speech-to-Text để chuyển giọng nói thành văn bản, LLM để xử lý nội dung và Text-to-Speech để tạo câu trả lời bằng giọng nói.

Trong phần demo, Voice Agent được dùng để trả lời thông tin về sản phẩm Apple như MacBook Pro. Demo này giúp tôi hình dung được cách AI có thể hỗ trợ chăm sóc khách hàng hoặc tư vấn sản phẩm. Tuy nhiên, khi triển khai cho tiếng Việt, hệ thống sẽ gặp thêm nhiều vấn đề như độ trễ, giọng vùng miền, cách xưng hô và việc xử lý khi người dùng ngắt lời.

Một điểm tôi thấy quan trọng là mô hình **Human-in-the-loop**. AI có thể hỗ trợ rất nhiều, nhưng khi câu trả lời chưa chắc chắn hoặc khách hàng không hài lòng, hệ thống vẫn cần chuyển cho con người xử lý. Điều này làm tôi hiểu rằng AI trong sản phẩm thật nên được thiết kế để phối hợp với con người, không nên hoạt động hoàn toàn độc lập.

#### AWS DevOps AI Agent và xử lý incident

Phần của **Bảo** và **Nguyên Nguyễn** nói về cách AI Agent hỗ trợ DevOps khi hệ thống gặp sự cố. Trước đây, tôi hình dung DevOps phải tự xem log, metric, dashboard và cảnh báo để tìm nguyên nhân. Qua session này, tôi hiểu thêm rằng AI Agent có thể giúp gom ngữ cảnh, phân tích dữ liệu vận hành và đề xuất hướng xử lý nhanh hơn.

Các điểm chính của DevOps AI Agent gồm:

- Context Learning để hiểu ngữ cảnh hệ thống.
- Control để con người vẫn quyết định bước cuối.
- Integration để kết nối với các công cụ vận hành.
- Collaboration để hỗ trợ làm việc qua Slack, ServiceNow hoặc nền tảng nội bộ.
- Cost-effective để tối ưu chi phí theo thời gian chạy thực tế.

Trong phần demo, diễn giả mô phỏng tình huống ứng dụng thương mại điện tử chạy trên AWS ECS bị chậm do một dạng tấn công từ chối dịch vụ. DevOps AI Agent đã phân tích thông tin và đưa ra hướng xử lý trong thời gian ngắn. Bài học tôi rút ra là AI Agent chỉ hữu ích khi hệ thống có observability tốt. Nếu không có log, metric và thông tin giám sát đầy đủ, AI cũng khó tìm được nguyên nhân chính xác.

#### Amazon Q trong quản trị nhân sự

Phần của **Trường** và **Minh Anh** trình bày cách dùng Amazon Q trong quy trình nhân sự. Bộ phận HR thường phải xử lý nhiều công việc lặp lại như viết mô tả công việc, đọc CV, đánh giá ứng viên và tổng hợp báo cáo. Amazon Q có thể hỗ trợ các bước này bằng cách kết nối với dữ liệu nội bộ và thực hiện một số action theo quy trình.

Trong demo, Amazon Q được dùng để tạo mô tả công việc cho vị trí Junior Cloud Engineer, quét thư mục CV, phân tích kỹ năng ứng viên, chấm điểm và xuất báo cáo HTML. Tôi thấy ví dụ này khá thực tế vì AI không chỉ trả lời câu hỏi mà còn tham gia vào một workflow cụ thể.

Tuy nhiên, phần này cũng cho thấy dữ liệu nhân sự là dữ liệu nhạy cảm. Khi dùng AI trong doanh nghiệp, không thể chỉ quan tâm đến tính tiện lợi mà phải xem xét quyền truy cập, bảo mật dữ liệu và việc kiểm soát kết quả đầu ra.

#### Thiết lập bảo mật cho Amazon Q với Private Connection

Phần của **Toàn Nguyễn** tập trung vào bảo mật khi Amazon Q kết nối với MCP Server hoặc hệ thống bên thứ ba. Nếu dữ liệu đi qua Internet công cộng, hệ thống có thể gặp rủi ro như rò rỉ dữ liệu, tấn công trung gian hoặc bị khai thác ở tầng mạng.

Giải pháp được trình bày là đưa luồng kết nối vào mạng riêng thông qua **Private Connection**. Kiến trúc này có thể dùng các thành phần như VPC Connection, Interface Endpoint, Route 53 Resolver, Application Load Balancer và TLS để giảm việc dữ liệu đi qua Internet công cộng.

Phần này giúp tôi hiểu rằng bảo mật cho hệ thống AI không chỉ nằm ở prompt, model hay ứng dụng. Khi triển khai trong doanh nghiệp, kiến trúc mạng, DNS, endpoint, mã hóa và phân quyền cũng rất quan trọng. Dù cách triển khai này có thể phát sinh thêm chi phí, nó phù hợp với các hệ thống xử lý dữ liệu nội bộ hoặc dữ liệu khách hàng.

### Bài học sau sự kiện

Sau sự kiện, tôi ghi nhận được một số bài học chính:

- AI Agent có thể hỗ trợ nhiều mảng khác nhau như chăm sóc khách hàng, DevOps, HR và security.
- Khi xây dựng Voice Agent cho tiếng Việt, cần chú ý đến độ trễ, giọng vùng miền, cách xưng hô và trải nghiệm hội thoại.
- DevOps AI Agent cần hệ thống có log, metric và monitoring tốt để phân tích sự cố chính xác.
- Amazon Q có thể hỗ trợ tự động hóa trong doanh nghiệp, nhưng phải đi kèm kiểm soát dữ liệu và phân quyền.
- Private Connection là một hướng quan trọng khi kết nối AI với hệ thống nội bộ.
- AI nên hỗ trợ con người ra quyết định, không nên thay thế hoàn toàn con người trong các bước quan trọng.

### Liên hệ với quá trình học FCAJ

Sự kiện này liên quan khá nhiều đến những nội dung tôi đã học trong FCAJ như ECS, VPC, Load Balancer, IAM, bảo mật và triển khai ứng dụng trên AWS. Trước đây tôi học các dịch vụ này chủ yếu qua lab riêng lẻ. Sau sự kiện, tôi hiểu hơn cách chúng có thể kết hợp trong các hệ thống AI thực tế.

Đặc biệt, phần DevOps AI Agent làm tôi chú ý hơn đến logging và monitoring. Khi làm backend hoặc triển khai ứng dụng, nếu chỉ chạy được chức năng chính thì chưa đủ. Hệ thống cần có khả năng quan sát để khi lỗi xảy ra, người vận hành có thể hiểu được nguyên nhân và xử lý nhanh hơn.

### Cảm nhận cá nhân

Tôi thấy sự kiện **Cloud, AI Agent và Amazon Q trên AWS** rất hữu ích vì có nhiều demo gần với công việc thực tế. Các nội dung như Voice Agent, DevOps AI Agent, Amazon Q cho HR và Private Connection giúp tôi hiểu rõ hơn cách AI đang được đưa vào doanh nghiệp.

Sau sự kiện, tôi nhận ra rằng để theo hướng backend và cloud, tôi không chỉ cần học lập trình API mà còn cần hiểu thêm về cloud deployment, observability, security và cách AI Agent được tích hợp vào hệ thống. Đây là những phần tôi muốn tiếp tục tìm hiểu sau chương trình FCAJ.

### Hình ảnh tham gia

![Hình ảnh tham gia sự kiện 2](/images/4-EventParticipated/event2.jpg)