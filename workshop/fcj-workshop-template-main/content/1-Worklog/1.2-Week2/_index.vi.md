---
title: "Worklog Tuần 2"
date: "2026-04-24"
weight: 2
chapter: false
pre: " <b> 1.2. </b> "
---

### Trọng tâm tuần này
* Hiểu cấu trúc IAM: Users, Groups, Roles, Policies.
* Viết được IAM Policy tuỳ chỉnh và áp dụng Permission Boundaries.
* Bật MFA cho các tài khoản quan trọng và cấu hình password policy.

### Công việc đã làm
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 6 | - **Cấu trúc IAM** <br> - Tạo IAM Group cho developers và admins <br> - Gắn managed policies (ReadOnlyAccess, PowerUserAccess) <br> - Tạo 2 IAM Users và đưa vào group <br> - Kiểm tra quyền bằng Policy Simulator | 24/04/2026 | 24/04/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 2 | - **Viết custom policies** <br> - Viết JSON policy cho phép chỉ EC2 và S3 tại region ap-southeast-1 <br> - Thêm điều kiện IP để giới hạn truy cập từ mạng công ty <br> - Test bằng CLI với --dry-run <br> - Lưu policy vào repo để tái sử dụng | 27/04/2026 | 27/04/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 3 | - **IAM Roles** <br> - Tạo EC2 Instance Role với quyền truy cập S3 <br> - Gắn role vào 1 EC2 instance đang chạy <br> - Test gọi S3 từ trong EC2 mà không cần access key <br> - Ghi chú sự khác biệt giữa Role và User | 28/04/2026 | 28/04/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 4 | - **MFA và password policy** <br> - Bật virtual MFA cho tất cả IAM users <br> - Đặt password policy: tối thiểu 12 ký tự, phải có số + ký tự đặc biệt <br> - Tạo credential report và kiểm tra user nào chưa bật MFA <br> - Xóa access key không dùng | 29/04/2026 | 29/04/2026 | <https://cloudjourney.awsstudygroup.com/> |

### Điều tôi rút ra được
* Dựng được cấu trúc IAM gọn gàng: 2 groups, managed policies, 2 users.
* Viết xong custom policy có điều kiện IP và region, test bằng --dry-run ok.
* EC2 Instance Role gọi S3 không cần key - bảo mật hơn nhiều so với dùng access key.
* MFA bật hết, password policy 12 ký tự, xóa được 1 access key cũ không ai dùng.
