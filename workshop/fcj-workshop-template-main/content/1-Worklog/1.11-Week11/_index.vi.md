---
title: "Worklog Tuần 11"
date: "2026-06-26"
weight: 11
chapter: false
pre: " <b> 1.11. </b> "
---

### Trọng tâm tuần này
* Đóng gói ứng dụng bằng Docker và quản lý image trên Amazon ECR.
* Triển khai container bằng Amazon ECS Fargate.
* Tích hợp backend OCR-CapCut với S3 và RDS.

### Công việc đã làm
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 6 | - **Docker cho ứng dụng** <br> - Viết Dockerfile cho FastAPI backend <br> - Tạo docker-compose cho API, Celery worker và Redis <br> - Build image, chạy local và kiểm tra API docs <br> - Đưa biến môi trường vào file .env, không commit secrets | 26/06/2026 | 26/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 2 | - **Amazon ECR** <br> - Tạo private repository cho API image <br> - Đăng nhập ECR bằng AWS CLI <br> - Tag và push image lên ECR <br> - Kiểm tra image digest và scan kết quả trong console | 29/06/2026 | 29/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 3 | - **Amazon ECS Fargate** <br> - Tạo ECS cluster dạng Fargate <br> - Viết task definition cho FastAPI container <br> - Cấu hình task role cho phép đọc ghi S3 prefix của dự án <br> - Triển khai service sau Application Load Balancer | 30/06/2026 | 30/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 4 | - **Dự án nhóm OCR-CapCut** <br> - Hoàn thiện module S3 upload, download và presigned URL <br> - Kết nối SQLAlchemy với RDS MySQL và chạy migration <br> - Kết nối Celery pipeline OCR, dịch phụ đề, TTS và render <br> - Test upload video và cập nhật tiến độ xử lý trên frontend | 01/07/2026 | 01/07/2026 | |

### Điều tôi rút ra được
* FastAPI, Celery và Redis chạy được qua Docker Compose.
* API image được push lên private ECR repository.
* Tạo ECS Fargate service và task role truy cập được S3 theo prefix.
* Pipeline OCR-CapCut xử lý được video test từ upload đến tạo file phụ đề.
