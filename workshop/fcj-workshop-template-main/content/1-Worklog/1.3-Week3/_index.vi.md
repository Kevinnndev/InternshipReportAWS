---
title: "Worklog Tuần 3"
date: "2026-05-01"
weight: 3
chapter: false
pre: " <b> 1.3. </b> "
---

### Trọng tâm tuần này
* Hiểu cách AWS tính phí đối với compute, storage và data transfer.
* Theo dõi AWS Free Tier credits $200 và thiết lập cảnh báo chi phí cho tài khoản lab.
* Thực hành kiểm tra và dọn các tài nguyên không còn dùng.

### Công việc đã làm
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 6 | - **Tìm hiểu giá dịch vụ** <br> - Tra giá On-Demand cho EC2, EBS, S3 và data transfer <br> - So sánh On-Demand với Savings Plans và Spot <br> - Dùng AWS Pricing Calculator ước tính một web app nhỏ <br> - Ghi lại các dịch vụ có thể phát sinh phí ngoài Free Tier | 01/05/2026 | 01/05/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 2 | - **Theo dõi Free Tier credits và AWS Budgets** <br> - Kiểm tra số AWS Free Tier credits $200 còn lại trong Billing console <br> - Tạo cost budget $200 theo tổng credit của tài khoản <br> - Cài email alert tại $20, $50, $100 và $150 <br> - Ghi lại cách dừng hoặc xóa tài nguyên khi credit giảm nhanh | 04/05/2026 | 04/05/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 3 | - **Cost Explorer** <br> - Bật Cost Explorer và nhóm chi phí theo service <br> - So sánh chi phí giữa các region đang dùng <br> - Lọc chi phí EC2 theo instance type <br> - Xuất báo cáo CSV để đối chiếu cuối tuần | 05/05/2026 | 05/05/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 4 | - **Dọn tài nguyên lab** <br> - Liệt kê EC2, EBS, snapshots và Elastic IP trong account <br> - Xóa snapshot và volume không còn dùng <br> - Kiểm tra S3 bucket có version cũ không cần thiết <br> - Lập checklist cleanup trước khi kết thúc mỗi lab | 06/05/2026 | 06/05/2026 | <https://cloudjourney.awsstudygroup.com/> |

### Điều tôi rút ra được
* Dùng Pricing Calculator ước tính được chi phí cho web app nhỏ trước khi triển khai.
* Đã kiểm tra Free Tier credits $200 và cấu hình email alert tại $20, $50, $100, $150.
* Biết dùng Cost Explorer để lọc chi phí theo service, region và instance type.
* Có checklist dọn EC2, EBS, snapshots, Elastic IP, ALB và ECS task sau mỗi buổi lab để tránh hao credit.
