---
title: "Week 8 Worklog"
date: "2026-06-05"
weight: 8
chapter: false
pre: " <b> 1.8. </b> "
---

### Focus this week
* Use Amazon S3 for static content and uploaded files.
* Configure versioning, encryption, and lifecycle rules.
* Control bucket access with IAM policies and bucket policies.

### Work done
| Day | Task | Start Date | Completion Date | Reference Material |
| --- | --- | --- | --- | --- |
| 6 | - **S3 buckets** <br> - Create a bucket for static assets and another for uploads <br> - Set a naming convention for the dev environment <br> - Upload files using Console, CLI, and sync command <br> - Check object metadata and storage class | 06/05/2026 | 06/05/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 2 | - **Protecting S3 data** <br> - Enable versioning for the upload bucket <br> - Turn on SSE-S3 default encryption <br> - Test restoring a deleted object version <br> - Enable Block Public Access at account level | 06/08/2026 | 06/08/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 3 | - **Access permissions** <br> - Create an IAM policy allowing app role access only to uploads/ prefix <br> - Write a bucket policy that denies requests without HTTPS <br> - Use AWS CLI to test upload with the right role <br> - Create a presigned URL for a test file | 06/09/2026 | 06/09/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 4 | - **Lifecycle and logging** <br> - Create a lifecycle rule moving old files to S3 Standard-IA <br> - Delete incomplete multipart uploads after 7 days <br> - Enable server access logging for the test bucket <br> - Check storage cost in Cost Explorer | 06/10/2026 | 06/10/2026 | <https://cloudjourney.awsstudygroup.com/> |

### What I took away
* Created separate buckets for static assets and uploaded files.
* Versioning, SSE-S3, and Block Public Access are enabled.
* App role has access only to the needed prefix and bucket policy requires HTTPS.
* Lifecycle rule moves old files and removes incomplete multipart uploads.
