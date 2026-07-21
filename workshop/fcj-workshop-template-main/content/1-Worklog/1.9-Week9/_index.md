---
title: "Week 9 Worklog"
date: "2026-06-12"
weight: 9
chapter: false
pre: " <b> 1.9. </b> "
---

### Focus this week
* Deliver static assets globally with Amazon CloudFront.
* Protect the S3 origin with Origin Access Control.
* Configure cache behavior and HTTPS for the website.

### Work done
| Day | Task | Start Date | Completion Date | Reference Material |
| --- | --- | --- | --- | --- |
| 6 | - **CloudFront overview** <br> - Learn about edge locations, origins, and distributions <br> - Compare cache hit, cache miss, and TTL <br> - Check CloudFront data transfer pricing <br> - Draw the request path from browser to S3 origin | 06/12/2026 | 06/12/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 2 | - **Creating a distribution** <br> - Create a CloudFront distribution with the S3 static bucket as origin <br> - Create Origin Access Control for S3 <br> - Update bucket policy so only CloudFront can read objects <br> - Confirm direct S3 URLs are no longer public | 06/15/2026 | 06/15/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 3 | - **Cache behavior** <br> - Set index.html as the default root object <br> - Configure different cache policies for HTML, CSS, and images <br> - Try an invalidation after uploading a new page <br> - Compare cache-control response headers | 06/16/2026 | 06/16/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 4 | - **HTTPS and custom domain** <br> - Create an ACM certificate in us-east-1 <br> - Attach the certificate to the CloudFront distribution <br> - Create a Route 53 Alias record for the custom domain <br> - Check HTTP to HTTPS redirect in the browser | 06/17/2026 | 06/17/2026 | <https://cloudjourney.awsstudygroup.com/> |

### What I took away
* Created a CloudFront distribution to deliver content from S3.
* S3 origin is protected by Origin Access Control and cannot be accessed publicly.
* Cache behavior separates HTML and static assets, and invalidation works.
* Test website uses a custom domain and HTTPS through an ACM certificate.
