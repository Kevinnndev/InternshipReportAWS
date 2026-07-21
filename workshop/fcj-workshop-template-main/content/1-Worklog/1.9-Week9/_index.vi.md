---
title: "Worklog Tuần 9"
date: "2026-06-12"
weight: 9
chapter: false
pre: " <b> 1.9. </b> "
---

### Trọng tâm tuần này
* Phân phối static assets toàn cầu bằng Amazon CloudFront.
* Bảo vệ S3 origin bằng Origin Access Control.
* Cấu hình cache behavior và HTTPS cho website.

### Công việc đã làm
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 6 | - **Tổng quan CloudFront** <br> - Tìm hiểu edge locations, origin và distribution <br> - So sánh cache hit, cache miss và TTL <br> - Kiểm tra pricing data transfer của CloudFront <br> - Vẽ luồng request từ browser đến S3 origin | 12/06/2026 | 12/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 2 | - **Tạo distribution** <br> - Tạo CloudFront distribution với S3 static bucket làm origin <br> - Tạo Origin Access Control cho S3 <br> - Cập nhật bucket policy chỉ cho CloudFront đọc objects <br> - Kiểm tra direct S3 URL không còn public | 15/06/2026 | 15/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 3 | - **Cache behavior** <br> - Cấu hình default root object là index.html <br> - Đặt cache policy khác nhau cho HTML, CSS và ảnh <br> - Thử invalidation sau khi upload trang mới <br> - So sánh response headers cache-control | 16/06/2026 | 16/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 4 | - **HTTPS và custom domain** <br> - Tạo ACM certificate ở region us-east-1 <br> - Gắn certificate vào CloudFront distribution <br> - Tạo Route 53 Alias record cho custom domain <br> - Kiểm tra redirect HTTP sang HTTPS trên trình duyệt | 17/06/2026 | 17/06/2026 | <https://cloudjourney.awsstudygroup.com/> |

### Điều tôi rút ra được
* Tạo CloudFront distribution phân phối nội dung từ S3.
* S3 origin được bảo vệ bằng Origin Access Control, không còn truy cập public trực tiếp.
* Cache behavior tách riêng cho HTML và static assets, invalidation chạy được.
* Website test dùng custom domain và HTTPS qua ACM certificate.
