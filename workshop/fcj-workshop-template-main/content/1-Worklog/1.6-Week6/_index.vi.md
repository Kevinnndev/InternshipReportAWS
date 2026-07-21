---
title: "Worklog Tuần 6"
date: "2026-05-22"
weight: 6
chapter: false
pre: " <b> 1.6. </b> "
---

### Trọng tâm tuần này
* Tìm hiểu các thành phần và cơ chế hoạt động của Application Load Balancer.
* Phân phối traffic đến các EC2 instances trong Auto Scaling Group.
* Cấu hình health check và kiểm tra khả năng chịu lỗi của ứng dụng.

### Công việc đã làm
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 6 | - **Tổng quan Elastic Load Balancing** <br> - So sánh ALB, NLB và Gateway Load Balancer <br> - Tìm hiểu listener, rule, target group và health check <br> - Vẽ sơ đồ request đi từ client đến EC2 <br> - Kiểm tra pricing theo Load Balancer Capacity Units | 22/05/2026 | 22/05/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 2 | - **Tạo Application Load Balancer** <br> - Tạo internet-facing ALB cho web app <br> - Tạo listener HTTP port 80 <br> - Tạo target group loại instance <br> - Đăng ký các EC2 instances vào target group | 25/05/2026 | 25/05/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 3 | - **Health check và rules** <br> - Cấu hình health check path /health <br> - Thêm trang health check trên Nginx <br> - Điều chỉnh healthy threshold và timeout <br> - Thử redirect HTTP sang HTTPS bằng listener rule | 26/05/2026 | 26/05/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 4 | - **Tích hợp ASG** <br> - Gắn target group vào Auto Scaling Group <br> - Test phân phối request bằng curl nhiều lần <br> - Dừng Nginx trên một target để kiểm tra unhealthy status <br> - Theo dõi ALB chỉ gửi request đến target healthy | 27/05/2026 | 27/05/2026 | <https://cloudjourney.awsstudygroup.com/> |

### Điều tôi rút ra được
* Phân biệt được ALB, NLB và trường hợp dùng từng loại.
* ALB phân phối request đến các EC2 trong target group.
* Health check path /health hoạt động và phát hiện target lỗi.
* Auto Scaling Group tự đăng ký instance mới vào ALB target group.
