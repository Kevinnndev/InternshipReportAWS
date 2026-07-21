---
title: "Week 10 Worklog"
date: "2026-06-19"
weight: 10
chapter: false
pre: " <b> 1.10. </b> "
---

### Focus this week
* Deploy Amazon RDS MySQL and learn about Aurora.
* Connect an application to the database securely.
* Start the OCR-CapCut team project.

### Work done
| Day | Task | Start Date | Completion Date | Reference Material |
| --- | --- | --- | --- | --- |
| 6 | - **Amazon RDS and Aurora** <br> - Compare RDS MySQL with Aurora MySQL <br> - Create an RDS MySQL 8.0 db.t3.micro instance <br> - Configure database name, DB parameter group, and backup window <br> - Test connection with MySQL client | 06/19/2026 | 06/19/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 2 | - **Database security** <br> - Configure Security Group to allow MySQL only from app server <br> - Enable encryption at rest and 7-day automated backup <br> - Store database URL in environment variables <br> - Test access from EC2 and block connections from outside IPs | 06/22/2026 | 06/22/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 3 | - **Operating RDS** <br> - Create a read replica to learn the read path <br> - Take a manual snapshot and restore a DB instance <br> - Check CloudWatch CPU, connections, and storage metrics <br> - Note the difference between backup, snapshot, and replica | 06/23/2026 | 06/23/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 4 | - **OCR-CapCut team project** <br> - Agree on scope: video upload, subtitle OCR, translation, TTS, and render <br> - Draw FastAPI, Celery, Redis, S3, and RDS MySQL architecture <br> - Create database schema for users, videos, srt, and video_tts <br> - Divide backend, frontend, and video processing tasks | 06/24/2026 | 06/24/2026 | |

### What I took away
* Created RDS MySQL and connected from a test application.
* Database allows MySQL traffic only from the app server Security Group.
* Tested snapshots, restore, and basic RDS metrics.
* Team agreed on the scope and architecture for OCR-CapCut.
