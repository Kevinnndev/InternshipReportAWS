---
title: "Worklog Tuần 1"
date: "2026-04-17"
weight: 1
chapter: false
pre: " <b> 1.1. </b> "
---

### Trọng tâm tuần này
* Nắm được khái niệm cơ bản về Cloud Computing và các mô hình dịch vụ.
* Hiểu mô hình trách nhiệm chung (Shared Responsibility) của AWS.
* Đăng ký tài khoản AWS và bảo mật ban đầu.

### Công việc đã làm
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 6 | - **Cloud Computing là gì** <br> - Đọc tài liệu về IaaS, PaaS, SaaS <br> - So sánh On-premise và Cloud (chi phí, vận hành, mở rộng) <br> - Tìm hiểu các Region và Availability Zone của AWS <br> - Ghi lại ưu điểm pay-as-you-go | 17/04/2026 | 17/04/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 2 | - **Shared Responsibility Model** <br> - Xác định phần AWS chịu trách nhiệm (hạ tầng vật lý, hypervisor) <br> - Xác định phần khách hàng phải tự quản (OS, firewall, data) <br> - Tìm hiểu compliance programs: SOC 2, ISO 27001, HIPAA <br> - Ghi chú lại bảng phân chia trách nhiệm | 20/04/2026 | 20/04/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 3 | - **Đăng ký tài khoản AWS** <br> - Tạo tài khoản mới với email riêng <br> - Chọn Support Plan (Basic) <br> - Bật MFA cho Root user ngay lập tức <br> - Tạo 1 IAM admin user để tránh dùng Root | 21/04/2026 | 21/04/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 4 | - **Cấu hình bảo mật ban đầu** <br> - Bật CloudTrail ở tất cả regions <br> - Tạo billing alarm (ngưỡng $5) bằng CloudWatch <br> - Cài AWS CLI trên máy và cấu hình access key <br> - Chạy thử `aws sts get-caller-identity` để xác nhận | 22/04/2026 | 22/04/2026 | <https://cloudjourney.awsstudygroup.com/> |

### Điều tôi rút ra được
* Tôi đã phân biệt rõ hơn IaaS, PaaS, SaaS và khi nào nên dùng từng mô hình.
* Tôi hiểu rõ hơn mô hình Shared Responsibility của AWS, đặc biệt là phần trách nhiệm phía người dùng.
* Tôi hoàn tất phần thiết lập ban đầu của tài khoản, gồm bật MFA cho Root user và tạo IAM admin user riêng.
* Tôi cũng cấu hình AWS CLI và đặt billing alarm 5 USD để theo dõi chi phí ngay từ đầu.
