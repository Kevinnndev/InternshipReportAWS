---
title: "Worklog Tuần 7"
date: "2026-05-29"
weight: 7
chapter: false
pre: " <b> 1.7. </b> "
---

### Trọng tâm tuần này
* Tìm hiểu DNS và cách Amazon Route 53 phân giải tên miền.
* Tạo hosted zone và các bản ghi DNS cơ bản.
* Kết nối tên miền với Application Load Balancer.

### Công việc đã làm
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 6 | - **Tổng quan DNS và Route 53** <br> - Ôn lại DNS resolver, nameserver và TTL <br> - Tìm hiểu public hosted zone, private hosted zone <br> - Phân biệt A, AAAA, CNAME, MX, TXT records <br> - Dùng nslookup kiểm tra bản ghi của một website | 29/05/2026 | 29/05/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 2 | - **Hosted zone và records** <br> - Tạo public hosted zone cho tên miền test <br> - Kiểm tra 4 nameservers được Route 53 cung cấp <br> - Tạo A record và CNAME record thử nghiệm <br> - Điều chỉnh TTL rồi kiểm tra propagation | 01/06/2026 | 01/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 3 | - **Route 53 Alias** <br> - Tạo Alias A record trỏ đến Application Load Balancer <br> - Kiểm tra app qua DNS thay vì ALB DNS name <br> - Tạo health check HTTP cho endpoint /health <br> - Xem trạng thái health check trong Route 53 console | 02/06/2026 | 02/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 4 | - **Routing policies** <br> - So sánh simple, weighted, latency và failover routing <br> - Thử weighted routing với hai record test <br> - Ghi chú khi nào cần failover routing <br> - Lưu danh sách DNS records đang dùng cho web app | 03/06/2026 | 03/06/2026 | <https://cloudjourney.awsstudygroup.com/> |

### Điều tôi rút ra được
* Hiểu cách DNS phân giải request và các loại record thường dùng.
* Tạo được hosted zone cùng A record, CNAME record và Alias record.
* Tên miền test trỏ được đến Application Load Balancer.
* Health check HTTP trong Route 53 hoạt động với endpoint /health.
