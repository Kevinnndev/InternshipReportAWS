---
title: "Worklog Tuần 4"
date: "2026-05-08"
weight: 4
chapter: false
pre: " <b> 1.4. </b> "
---

### Trọng tâm tuần này
* Khởi tạo EC2 và cấu hình môi trường cho ứng dụng web.
* Làm quen với AMI, instance type, key pair và user data.
* Thực hành quản trị cơ bản trên Amazon Linux.

### Công việc đã làm
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 6 | - **Khởi tạo EC2** <br> - Chọn Amazon Linux 2023 AMI và t3.micro <br> - Tạo key pair ED25519, gắn tag theo dự án <br> - Chọn Security Group cho SSH và HTTP <br> - Kiểm tra trạng thái instance và public IPv4 | 08/05/2026 | 08/05/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 2 | - **User data và web server** <br> - Viết user data cài Nginx khi boot <br> - Tạo trang HTML giới thiệu ứng dụng <br> - Kiểm tra Nginx bằng systemctl và curl <br> - Cập nhật Security Group để mở cổng 80 | 11/05/2026 | 11/05/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 3 | - **Quản trị Amazon Linux** <br> - Kết nối bằng SSH và Session Manager <br> - Thực hành journalctl, top, df và free <br> - Tạo user không dùng quyền root trực tiếp <br> - Cập nhật packages và reboot instance | 12/05/2026 | 12/05/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 4 | - **AMI và EBS** <br> - Tạo AMI từ web server đã cấu hình <br> - Gắn thêm EBS volume và mount vào /data <br> - Cấu hình fstab để tự mount sau reboot <br> - Terminate instance test và kiểm tra snapshot liên quan | 13/05/2026 | 13/05/2026 | <https://cloudjourney.awsstudygroup.com/> |

### Điều tôi rút ra được
* Khởi tạo được EC2 Amazon Linux và truy cập bằng SSH lẫn Session Manager.
* User data cài Nginx tự động, trang web test truy cập được qua HTTP.
* Biết kiểm tra log và tài nguyên cơ bản trên Linux.
* Tạo được AMI và gắn EBS volume cho web server.
