---
title: "Worklog Tuần 5"
date: "2026-05-15"
weight: 5
chapter: false
pre: " <b> 1.5. </b> "
---

### Trọng tâm tuần này
* Tìm hiểu Auto Scaling Groups và Launch Templates.
* Cấu hình mở rộng web server dựa trên CPU utilization.
* Thử kiểm tra ứng dụng khi instance được thay thế tự động.

### Công việc đã làm
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 6 | - **Launch Template** <br> - Tạo launch template từ AMI web server tuần trước <br> - Chọn instance type, key pair và Security Group <br> - Đặt user data cập nhật trang web khi boot <br> - Tạo version mới để thử thay đổi cấu hình | 15/05/2026 | 15/05/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 2 | - **Auto Scaling Group** <br> - Tạo Auto Scaling Group từ launch template <br> - Đặt desired capacity 2, minimum 1 và maximum 4 <br> - Chọn subnets cho các instances <br> - Kiểm tra activity history sau khi khởi tạo | 18/05/2026 | 18/05/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 3 | - **Scaling policies** <br> - Tạo target tracking policy giữ CPU trung bình 50% <br> - Tạo CloudWatch alarm cho CPU cao <br> - Dùng stress-ng để tạo tải trên instance test <br> - Theo dõi scale out và scale in trong Activity tab | 19/05/2026 | 19/05/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 4 | - **Health check** <br> - Terminate một instance trong Auto Scaling Group <br> - Theo dõi ASG tạo instance mới thay thế <br> - Kiểm tra grace period và health check type <br> - Ghi lại điểm khác nhau giữa manual và automatic scaling | 20/05/2026 | 20/05/2026 | <https://cloudjourney.awsstudygroup.com/> |

### Điều tôi rút ra được
* Tạo được Launch Template từ AMI web server.
* Auto Scaling Group giữ 2 instances ban đầu và có thể mở rộng đến 4 instances.
* Target tracking policy phản ứng khi CPU tăng trong bài test.
* Instance bị terminate được Auto Scaling Group thay thế tự động.
