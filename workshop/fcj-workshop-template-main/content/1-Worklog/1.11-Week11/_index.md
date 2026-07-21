---
title: "Week 11 Worklog"
date: "2026-06-26"
weight: 11
chapter: false
pre: " <b> 1.11. </b> "
---

### Focus this week
* Package the application with Docker and manage images in Amazon ECR.
* Deploy containers with Amazon ECS Fargate.
* Integrate the OCR-CapCut backend with S3 and RDS.

### Work done
| Day | Task | Start Date | Completion Date | Reference Material |
| --- | --- | --- | --- | --- |
| 6 | - **Docker for the application** <br> - Write a Dockerfile for the FastAPI backend <br> - Create docker-compose for API, Celery worker, and Redis <br> - Build image, run locally, and check API docs <br> - Put environment variables in .env and do not commit secrets | 06/26/2026 | 06/26/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 2 | - **Amazon ECR** <br> - Create a private repository for API image <br> - Sign in to ECR with AWS CLI <br> - Tag and push the image to ECR <br> - Check image digest and scan results in console | 06/29/2026 | 06/29/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 3 | - **Amazon ECS Fargate** <br> - Create a Fargate ECS cluster <br> - Write task definition for the FastAPI container <br> - Configure task role to read and write project S3 prefix <br> - Deploy service behind Application Load Balancer | 06/30/2026 | 06/30/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 4 | - **OCR-CapCut team project** <br> - Finish S3 upload, download, and presigned URL module <br> - Connect SQLAlchemy to RDS MySQL and run migrations <br> - Connect Celery pipeline for OCR, subtitle translation, TTS, and render <br> - Test video upload and processing progress on the frontend | 07/01/2026 | 07/01/2026 | |

### What I took away
* FastAPI, Celery, and Redis run through Docker Compose.
* API image was pushed to a private ECR repository.
* Created an ECS Fargate service and task role can access the needed S3 prefix.
* OCR-CapCut pipeline processes a test video from upload to subtitle output.
