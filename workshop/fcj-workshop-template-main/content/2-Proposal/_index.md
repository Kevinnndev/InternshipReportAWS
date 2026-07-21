---
title: "Proposal"
date: 2026-07-17
weight: 2
chapter: false
pre: " <b> 2. </b> "
layout: proposal
---

<div class="proposal-header">
  <div class="proposal-badge">AWS Cloud Project</div>
  <h1>Video Localization Platform</h1>
  <p class="subtitle">Automated Video Translation & Dubbing System</p>
  <div class="proposal-tags">
    <span class="tag">AWS Cloud</span>
    <span class="tag">Async Processing</span>
    <span class="tag">Video Workflow</span>
  </div>
</div>

<div class="proposal-metrics">
  <div class="metric-card">
    <div class="metric-value">5-15 minutes</div>
    <div class="metric-label">Estimated processing time</div>
  </div>
  <div class="metric-card">
    <div class="metric-value">$17-30</div>
    <div class="metric-label">Estimated monthly cost</div>
  </div>
  <div class="metric-card">
    <div class="metric-value">2 paths</div>
    <div class="metric-label">OCR and STT processing</div>
  </div>
  <div class="metric-card">
    <div class="metric-value">14 weeks</div>
    <div class="metric-label">Planned timeline</div>
  </div>
</div>

<div class="proposal-content">

## 1. Project Overview

This proposal presents a video localization platform that supports subtitle extraction, translation, and dubbing for multilingual video content. The system is built on AWS and combines a web interface, backend API, background workers, and cloud storage to handle the processing flow from video upload to final output.

When a user uploads a video, the system determines whether the content should go through OCR or speech-to-text, translates the extracted text, generates dubbed audio when needed, and renders the final result. The project is developed as a practical prototype, so the main focus is the core workflow, deployment feasibility, and cost control.

### Core Technologies

| Technology | Description |
|------------|-------------|
| AWS Cloud Services | Storage, database, notification, and translation services |
| Celery + Redis | Background task processing |
| PaddleOCR | Subtitle extraction from videos with embedded text |
| AWS Translate | Primary translation service |
| Google Cloud Translate v2 / Gemini | Fallback translation options |
| gTTS / ElevenLabs | Audio generation for dubbing |
| FFmpeg | Video validation and rendering |

---

## 2. Problem Statement

### Current Challenges

| Challenge | Impact |
|-----------|--------|
| Manual subtitle extraction | Time-consuming and repetitive work |
| Sentence-by-sentence translation | 4-8 hours per video |
| Timing synchronization | Difficult to align subtitles and audio manually |
| Dubbing cost | High cost for longer videos |
| Processing many videos | Hard to track and scale |

### Proposed Solution

The proposed system handles the workflow from video upload to final rendering in one processing flow:

1. **Video upload** — Receive the source video through the web interface
2. **OCR or STT selection** — Use PaddleOCR for videos with embedded subtitles or Google Cloud Speech-to-Text for audio-based content
3. **Translation** — Use AWS Translate as the main service, with Google Cloud Translate v2 or Google Gemini as fallback options when needed
4. **Audio generation** — Create dubbed audio with gTTS or ElevenLabs
5. **Video rendering** — Combine subtitles or dubbed audio into the final output with FFmpeg
6. **Result delivery** — Store outputs and return downloadable files to the user

### Expected Benefits

| Metric | Traditional Workflow | Proposed System |
|--------|----------------------|-----------------|
| Processing time | 4-8 hours/video | Around 5-15 minutes/video |
| Operating cost | Higher manual and service cost | Around $17-30/month in development scale |
| Terminology consistency | Depends on manual review | More stable with one workflow |
| Handling multiple videos | Hard to monitor | Easier to queue and track |

---

## 3. Solution Architecture

The platform is organized into four main parts: frontend, backend API, background workers, and storage services. This structure helps separate user interaction, task processing, and data management.

![Video Localization Platform Architecture](/images/2-Proposal/aws_demo.jpg)

### AWS Services

| Service | Purpose |
|---------|---------|
| **Amazon S3** | Store input videos, output videos, and subtitle files (.srt) |
| **Amazon RDS MySQL** | Store user data, video metadata, and processing status |
| **Amazon SES** | Send notification emails after processing completes |
| **AWS Translate** | Main translation service |
| **AWS Region** | ap-southeast-1 (Singapore) |

### Third-Party Services

| Service | Function |
|---------|----------|
| **PaddleOCR** | Extract subtitles from video frames |
| **Google Cloud STT** | Convert speech to text for videos without subtitles |
| **Google Cloud Translate v2** | Backup translation provider |
| **Google Gemini** | Additional fallback for translation cases that need review |
| **ElevenLabs** | Natural voice generation |
| **FFmpeg** | Validate formats and render videos |

### Component Design

- **Frontend**: React 18 + TypeScript + Vite — upload video, preview content, and edit subtitles
- **Backend**: FastAPI — provide API endpoints and coordinate processing requests
- **Background processing**: Celery + Redis — run OCR, translation, TTS, and rendering tasks asynchronously
- **Storage**: Amazon S3 for files, Amazon RDS for metadata, Redis for queue and caching support

---

## 4. Technical Implementation

### Implementation Phases

| Phase | Duration | Main Output |
|-------|----------|-------------|
| **Foundation** | 4 weeks | Project setup, infrastructure, and basic upload flow |
| **Phase 1** | 6 weeks | OCR/STT processing, translation, and progress tracking |
| **Phase 2** | 4 weeks | TTS, video rendering, and subtitle editor |
| **Finalization** | 2 weeks | Testing, optimization, and documentation |

### Technology Stack

| Layer | Technologies |
|-------|--------------|
| **Frontend** | React 18, TypeScript, Vite, Zustand, TailwindCSS, Radix UI |
| **Backend** | Python 3.11+, FastAPI, Celery, Redis, SQLAlchemy, Pydantic |
| **OCR/STT** | PaddleOCR, Google Cloud Speech-to-Text API |
| **Translation** | AWS Translate, Google Cloud Translate v2, Google Gemini API |
| **TTS** | gTTS, ElevenLabs API |
| **Video** | FFmpeg, MoviePy |
| **Infrastructure** | AWS S3, RDS MySQL, SES, Docker, Redis |

---

## 5. Budget Estimation

### Estimated AWS Monthly Cost (Development Scale)

| Service | Usage | Monthly Cost |
|---------|-------|--------------|
| Amazon S3 | 50 GB storage, 10 GB transfer | $1.50 |
| Amazon RDS MySQL | db.t3.micro, 20 GB storage | $15.00 |
| Amazon SES | 62,000 free emails | $0.00 |
| Data Transfer | 10 GB outbound | $0.90 |
| **Total AWS** | | **$17.40** |

### Third-Party API Costs

| Service | Free Tier | Paid Usage |
|---------|-----------|------------|
| Google Cloud STT | 60 minutes/month | $1.50/15 minutes |
| AWS Translate | Usage-based | Per translated character |
| Google Cloud Translate v2 | Usage-based | Per translated character |
| Google Gemini | 15 requests/minute | $0.001/1K chars |
| ElevenLabs | 10,000 chars/month | $5.00/100K chars |
| gTTS | Unlimited | $0.00 |

**Estimated monthly cost**: around $20-30 for development and testing workload.

---

## 6. Risk Assessment

### Risk Matrix

| Risk | Impact | Probability | Mitigation |
|------|--------|-------------|------------|
| Translation service rate limiting | High | Medium | Queue requests and switch to fallback service when needed |
| Low OCR accuracy on complex subtitles | High | Low | Allow subtitle review and correction |
| Unsupported video format | Medium | High | Validate with FFprobe and transcode before processing |
| Worker interruption | Medium | Low | Retry tasks after worker recovery |
| Higher-than-expected API cost | Medium | Medium | Monitor usage and set budget alerts |

### Contingency Plans

- **Translation issue**: switch from the main provider to a fallback provider
- **OCR output is weak**: allow manual subtitle editing before final rendering
- **Queue interruption**: resume processing after worker recovery

---

## 7. Expected Outcomes

### Technical Deliverables

- A web application for video upload and subtitle editing
- Automatic subtitle extraction using OCR or STT
- Translation flow with AWS Translate and fallback options
- Dubbing support with gTTS or ElevenLabs
- Final video rendering with subtitles or dubbed audio
- Progress tracking for processing jobs
- Email notification when the result is ready

### Output Formats

- Videos with soft subtitles
- Videos with hard subtitles burned into the video
- Videos with dubbed audio
- SRT subtitle files in source and target languages
- Download links for completed results

### Practical Value

- Reduce repetitive manual work in subtitle processing
- Help teams process multilingual videos more quickly
- Keep the workflow easier to monitor and review
- Provide a practical base for deployment and further improvement on AWS

</div>
