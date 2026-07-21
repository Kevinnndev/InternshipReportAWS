---
title: "Week 6 Worklog"
date: "2026-05-22"
weight: 6
chapter: false
pre: " <b> 1.6. </b> "
---

### Focus this week
* Learn the parts and behavior of an Application Load Balancer.
* Distribute traffic to EC2 instances in the Auto Scaling Group.
* Configure health checks and test application fault tolerance.

### Work done
| Day | Task | Start Date | Completion Date | Reference Material |
| --- | --- | --- | --- | --- |
| 6 | - **Elastic Load Balancing overview** <br> - Compare ALB, NLB, and Gateway Load Balancer <br> - Learn about listeners, rules, target groups, and health checks <br> - Draw the request path from client to EC2 <br> - Check pricing by Load Balancer Capacity Units | 05/22/2026 | 05/22/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 2 | - **Creating an Application Load Balancer** <br> - Create an internet-facing ALB for the web app <br> - Create an HTTP listener on port 80 <br> - Create an instance target group <br> - Register EC2 instances in the target group | 05/25/2026 | 05/25/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 3 | - **Health checks and rules** <br> - Configure the /health health check path <br> - Add a health check page in Nginx <br> - Adjust healthy threshold and timeout <br> - Try redirecting HTTP to HTTPS with a listener rule | 05/26/2026 | 05/26/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 4 | - **Integrating ASG** <br> - Attach the target group to the Auto Scaling Group <br> - Test request distribution with repeated curl calls <br> - Stop Nginx on one target to check unhealthy status <br> - Watch ALB send traffic only to healthy targets | 05/27/2026 | 05/27/2026 | <https://cloudjourney.awsstudygroup.com/> |

### What I took away
* Can distinguish ALB, NLB, and the use case for each one.
* ALB distributes requests to EC2 instances in the target group.
* The /health check works and detects a failed target.
* Auto Scaling Group registers new instances with the ALB target group.
