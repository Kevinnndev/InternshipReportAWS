---
title: "Bản đề xuất"
date: 2026-07-17
weight: 2
chapter: false
pre: " <b> 2. </b> "
layout: proposal
---

<div class="proposal-header">
  <div class="proposal-badge">AWS Cloud Project</div>
  <h1>Video Localization Platform</h1>
  <p class="subtitle">Hệ thống Tự động Hóa Dịch Thuật & Lồng Tiếng Video</p>
  <div class="proposal-tags">
    <span class="tag">AWS Cloud</span>
    <span class="tag">Xử lý bất đồng bộ</span>
    <span class="tag">Quy trình video</span>
  </div>
</div>

<div class="proposal-metrics">
  <div class="metric-card">
    <div class="metric-value">5-15 phút</div>
    <div class="metric-label">Thời gian xử lý ước tính</div>
  </div>
  <div class="metric-card">
    <div class="metric-value">$17-30</div>
    <div class="metric-label">Chi phí hàng tháng ước tính</div>
  </div>
  <div class="metric-card">
    <div class="metric-value">2 luồng</div>
    <div class="metric-label">OCR và STT</div>
  </div>
  <div class="metric-card">
    <div class="metric-value">14 tuần</div>
    <div class="metric-label">Thời gian dự kiến</div>
  </div>
</div>

<div class="proposal-content">

## 1. Tổng quan dự án

Đề xuất này trình bày một nền tảng bản địa hóa video nhằm hỗ trợ các bước trích xuất phụ đề, dịch nội dung và lồng tiếng cho video đa ngôn ngữ. Hệ thống được xây dựng trên AWS, kết hợp giao diện web, backend API, worker xử lý nền và dịch vụ lưu trữ để xử lý luồng công việc từ lúc tải video lên đến khi tạo ra kết quả cuối cùng.

Khi người dùng tải video lên, hệ thống sẽ xác định nên xử lý theo hướng OCR hay speech-to-text, sau đó dịch nội dung, tạo giọng đọc khi cần và render file kết quả. Dự án được phát triển theo hướng prototype thực tế, nên trọng tâm là hoàn thiện luồng chức năng chính, kiểm tra khả năng triển khai và theo dõi chi phí vận hành.

### Công nghệ cốt lõi

| Công nghệ | Mô tả |
|-----------|--------|
| AWS Cloud Services | Lưu trữ, cơ sở dữ liệu, thông báo và dịch vụ dịch thuật |
| Celery + Redis | Xử lý tác vụ nền |
| PaddleOCR | Trích xuất phụ đề từ video có chữ nhúng |
| AWS Translate | Dịch vụ dịch chính |
| Google Cloud Translate v2 / Gemini | Phương án dịch dự phòng |
| gTTS / ElevenLabs | Tạo âm thanh cho lồng tiếng |
| FFmpeg | Kiểm tra định dạng và render video |

---

## 2. Bài toán đặt ra

### Những khó khăn hiện tại

| Khó khăn | Tác động |
|----------|----------|
| Trích xuất phụ đề thủ công | Tốn thời gian và lặp lại nhiều thao tác |
| Dịch từng câu | 4-8 giờ cho mỗi video |
| Đồng bộ thời gian | Khó căn chỉnh phụ đề và âm thanh bằng tay |
| Chi phí lồng tiếng | Tăng cao với video dài |
| Xử lý nhiều video cùng lúc | Khó theo dõi và khó mở rộng |

### Giải pháp đề xuất

Hệ thống được đề xuất xử lý toàn bộ luồng công việc từ lúc tải video lên đến khi tạo file đầu ra:

1. **Tải video lên** — Nhận video nguồn từ giao diện web
2. **Chọn OCR hoặc STT** — Dùng PaddleOCR cho video có phụ đề nhúng hoặc Google Cloud Speech-to-Text cho nội dung dựa trên âm thanh
3. **Dịch nội dung** — Ưu tiên AWS Translate, dùng Google Cloud Translate v2 hoặc Google Gemini làm phương án dự phòng khi cần
4. **Tạo âm thanh** — Sinh giọng đọc bằng gTTS hoặc ElevenLabs
5. **Render video** — Ghép phụ đề hoặc âm thanh lồng tiếng vào video bằng FFmpeg
6. **Trả kết quả** — Lưu file đầu ra và cung cấp file để người dùng tải xuống

### Lợi ích kỳ vọng

| Chỉ số | Cách làm thủ công | Hệ thống đề xuất |
|--------|-------------------|------------------|
| Thời gian xử lý | 4-8 giờ/video | Khoảng 5-15 phút/video |
| Chi phí vận hành | Phụ thuộc nhiều vào thao tác thủ công | Khoảng $17-30/tháng ở quy mô phát triển |
| Tính nhất quán nội dung | Phụ thuộc vào người xử lý | Ổn định hơn nhờ cùng một quy trình |
| Xử lý nhiều video | Khó theo dõi khi số lượng tăng | Dễ xếp hàng và theo dõi trạng thái |

---

## 3. Kiến trúc giải pháp

Nền tảng được tổ chức thành bốn phần chính: frontend, backend API, worker xử lý nền và các dịch vụ lưu trữ. Cách chia này giúp tách rõ phần giao diện người dùng, phần xử lý tác vụ và phần quản lý dữ liệu.

![Video Localization Platform Architecture](/images/2-Proposal/aws_demo.jpg)

### Các dịch vụ AWS

| Dịch vụ | Mục đích |
|---------|----------|
| **Amazon S3** | Lưu video đầu vào, video đầu ra và file phụ đề (.srt) |
| **Amazon RDS MySQL** | Lưu thông tin người dùng, metadata video và trạng thái xử lý |
| **Amazon SES** | Gửi email thông báo sau khi xử lý xong |
| **AWS Translate** | Dịch vụ dịch chính |
| **AWS Region** | ap-southeast-1 (Singapore) |

### Các dịch vụ bên thứ ba

| Dịch vụ | Chức năng |
|---------|-----------|
| **PaddleOCR** | Trích xuất phụ đề từ các khung hình video |
| **Google Cloud STT** | Chuyển giọng nói thành văn bản cho video không có phụ đề |
| **Google Cloud Translate v2** | Nhà cung cấp dịch dự phòng |
| **Google Gemini** | Phương án dự phòng cho các trường hợp cần xem lại bản dịch |
| **ElevenLabs** | Tạo giọng đọc tự nhiên |
| **FFmpeg** | Kiểm tra định dạng và render video |

### Thiết kế thành phần

- **Frontend**: React 18 + TypeScript + Vite — tải video, xem trước nội dung và chỉnh sửa phụ đề
- **Backend**: FastAPI — cung cấp API và điều phối yêu cầu xử lý
- **Xử lý nền**: Celery + Redis — chạy các tác vụ OCR, dịch thuật, TTS và render theo kiểu bất đồng bộ
- **Lưu trữ**: Amazon S3 lưu file, Amazon RDS lưu metadata, Redis hỗ trợ queue và cache

---

## 4. Triển khai kỹ thuật

### Các giai đoạn triển khai

| Giai đoạn | Thời gian | Kết quả chính |
|-----------|-----------|---------------|
| **Nền tảng** | 4 tuần | Khởi tạo dự án, hạ tầng và luồng tải video cơ bản |
| **Giai đoạn 1** | 6 tuần | OCR/STT, dịch nội dung và theo dõi tiến độ |
| **Giai đoạn 2** | 4 tuần | TTS, render video và trình chỉnh sửa phụ đề |
| **Hoàn thiện** | 2 tuần | Kiểm thử, tối ưu và tài liệu |

### Công nghệ sử dụng

| Lớp | Công nghệ |
|-----|-----------|
| **Frontend** | React 18, TypeScript, Vite, Zustand, TailwindCSS, Radix UI |
| **Backend** | Python 3.11+, FastAPI, Celery, Redis, SQLAlchemy, Pydantic |
| **OCR/STT** | PaddleOCR, Google Cloud Speech-to-Text API |
| **Dịch thuật** | AWS Translate, Google Cloud Translate v2, Google Gemini API |
| **TTS** | gTTS, ElevenLabs API |
| **Video** | FFmpeg, MoviePy |
| **Hạ tầng** | AWS S3, RDS MySQL, SES, Docker, Redis |

---

## 5. Ước tính ngân sách

### Chi phí AWS hàng tháng ở quy mô phát triển

| Dịch vụ | Mức sử dụng | Chi phí hàng tháng |
|---------|-------------|--------------------|
| Amazon S3 | 50 GB lưu trữ, 10 GB truyền dữ liệu | $1.50 |
| Amazon RDS MySQL | db.t3.micro, 20 GB lưu trữ | $15.00 |
| Amazon SES | 62,000 email miễn phí | $0.00 |
| Data Transfer | 10 GB outbound | $0.90 |
| **Tổng AWS** | | **$17.40** |

### Chi phí API bên thứ ba

| Dịch vụ | Free Tier | Khi vượt mức |
|---------|-----------|--------------|
| Google Cloud STT | 60 phút/tháng | $1.50/15 phút |
| AWS Translate | Tính theo mức dùng | Theo số ký tự dịch |
| Google Cloud Translate v2 | Tính theo mức dùng | Theo số ký tự dịch |
| Google Gemini | 15 request/phút | $0.001/1K ký tự |
| ElevenLabs | 10,000 ký tự/tháng | $5.00/100K ký tự |
| gTTS | Không tính phí | $0.00 |

**Chi phí ước tính hàng tháng**: khoảng $20-30 cho nhu cầu phát triển và kiểm thử.

---

## 6. Đánh giá rủi ro

### Ma trận rủi ro

| Rủi ro | Ảnh hưởng | Xác suất | Hướng xử lý |
|--------|-----------|----------|-------------|
| Dịch vụ dịch bị giới hạn tần suất | Cao | Trung bình | Xếp hàng request và chuyển sang dịch vụ dự phòng khi cần |
| OCR kém chính xác với phụ đề phức tạp | Cao | Thấp | Cho phép rà soát và sửa phụ đề |
| Video không đúng định dạng | Trung bình | Cao | Kiểm tra bằng FFprobe và chuyển đổi trước khi xử lý |
| Worker bị gián đoạn | Trung bình | Thấp | Chạy lại tác vụ sau khi worker phục hồi |
| Chi phí API tăng cao hơn dự kiến | Trung bình | Trung bình | Theo dõi usage và đặt cảnh báo ngân sách |

### Phương án dự phòng

- **Có lỗi ở dịch vụ dịch chính**: chuyển sang nhà cung cấp dự phòng
- **Kết quả OCR chưa tốt**: cho phép chỉnh sửa phụ đề trước khi render cuối cùng
- **Queue bị gián đoạn**: tiếp tục xử lý lại sau khi worker hoạt động trở lại

---

## 7. Kết quả kỳ vọng

### Kết quả kỹ thuật

- Ứng dụng web để tải video và chỉnh sửa phụ đề
- Chức năng trích xuất phụ đề tự động bằng OCR hoặc STT
- Luồng dịch nội dung với AWS Translate và các phương án dự phòng
- Hỗ trợ tạo giọng đọc bằng gTTS hoặc ElevenLabs
- Render video đầu ra với phụ đề hoặc âm thanh lồng tiếng
- Theo dõi tiến độ xử lý
- Gửi email thông báo khi có kết quả

### Định dạng đầu ra

- Video có phụ đề mềm
- Video có phụ đề cứng được chèn trực tiếp vào khung hình
- Video có âm thanh lồng tiếng
- File phụ đề SRT ở ngôn ngữ nguồn và ngôn ngữ đích
- Link tải kết quả sau khi hoàn tất

### Giá trị thực tiễn

- Giảm bớt các thao tác thủ công lặp lại trong xử lý phụ đề
- Hỗ trợ xử lý video đa ngôn ngữ nhanh hơn
- Giúp việc theo dõi và kiểm tra quy trình thuận tiện hơn
- Tạo nền tảng thực tế để tiếp tục triển khai và cải tiến trên AWS

</div>
