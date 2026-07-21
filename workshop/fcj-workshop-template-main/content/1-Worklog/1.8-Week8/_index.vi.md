---
title: "Worklog Tuần 8"
date: "2026-06-05"
weight: 8
chapter: false
pre: " <b> 1.8. </b> "
---

### Trọng tâm tuần này
* Sử dụng Amazon S3 để lưu nội dung tĩnh và file upload.
* Cấu hình versioning, encryption và lifecycle rules.
* Kiểm soát truy cập bucket bằng IAM policy và bucket policy.

### Công việc đã làm
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 6 | - **S3 buckets** <br> - Tạo bucket cho static assets và bucket cho file upload <br> - Đặt naming convention theo môi trường dev <br> - Upload file bằng Console, CLI và sync command <br> - Kiểm tra object metadata và storage class | 05/06/2026 | 05/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 2 | - **Bảo vệ dữ liệu trên S3** <br> - Bật versioning cho bucket upload <br> - Bật default encryption SSE-S3 <br> - Test khôi phục object version đã xóa <br> - Bật Block Public Access ở account level | 08/06/2026 | 08/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 3 | - **Phân quyền truy cập** <br> - Tạo IAM policy chỉ cho phép app role truy cập prefix uploads/ <br> - Viết bucket policy chặn request không dùng HTTPS <br> - Dùng AWS CLI test upload bằng role phù hợp <br> - Tạo presigned URL cho một file test | 09/06/2026 | 09/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 4 | - **Lifecycle và logging** <br> - Tạo lifecycle rule chuyển file cũ sang S3 Standard-IA <br> - Xóa incomplete multipart uploads sau 7 ngày <br> - Bật server access logging cho bucket test <br> - Kiểm tra chi phí storage trong Cost Explorer | 10/06/2026 | 10/06/2026 | <https://cloudjourney.awsstudygroup.com/> |

### Điều tôi rút ra được
* Tạo tách riêng bucket chứa static assets và bucket chứa file upload.
* Versioning, SSE-S3 và Block Public Access đã được bật.
* App role chỉ có quyền trong prefix cần thiết, bucket policy bắt buộc HTTPS.
* Lifecycle rule tự chuyển file cũ và dọn multipart upload chưa hoàn tất.
