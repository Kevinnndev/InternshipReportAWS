---
title: "Worklog Tuần 10"
date: "2026-06-19"
weight: 10
chapter: false
pre: " <b> 1.10. </b> "
---

### Trọng tâm tuần này
* Triển khai Amazon RDS MySQL và tìm hiểu Aurora.
* Kết nối ứng dụng với database theo cách bảo mật.
* Bắt đầu dự án nhóm OCR-CapCut.

### Công việc đã làm
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 6 | - **Amazon RDS và Aurora** <br> - So sánh RDS MySQL với Aurora MySQL <br> - Tạo RDS MySQL 8.0 instance db.t3.micro <br> - Cấu hình database name, DB parameter group và backup window <br> - Kết nối thử bằng MySQL client | 19/06/2026 | 19/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 2 | - **Bảo mật database** <br> - Cấu hình Security Group chỉ nhận MySQL từ app server <br> - Bật encryption at rest và automated backup 7 ngày <br> - Lưu database URL trong environment variables <br> - Kiểm tra kết nối từ EC2 và chặn kết nối từ IP bên ngoài | 22/06/2026 | 22/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 3 | - **RDS vận hành** <br> - Tạo read replica để tìm hiểu luồng đọc <br> - Chụp manual snapshot và thử restore DB instance <br> - Xem CloudWatch metrics: CPU, connections, storage <br> - Ghi chú khác nhau giữa backup, snapshot và replica | 23/06/2026 | 23/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 4 | - **Dự án nhóm OCR-CapCut** <br> - Thống nhất phạm vi: upload video, OCR phụ đề, dịch, TTS và render <br> - Vẽ kiến trúc FastAPI, Celery, Redis, S3 và RDS MySQL <br> - Tạo database schema cho users, videos, srt và video_tts <br> - Phân công phần backend, frontend và xử lý video | 24/06/2026 | 24/06/2026 | |

### Điều tôi rút ra được
* Tạo được RDS MySQL và kết nối từ ứng dụng test.
* Database chỉ cho phép traffic MySQL từ Security Group của app server.
* Đã thử snapshot, restore và theo dõi metrics cơ bản của RDS.
* Nhóm chốt phạm vi và kiến trúc dự án OCR-CapCut.
