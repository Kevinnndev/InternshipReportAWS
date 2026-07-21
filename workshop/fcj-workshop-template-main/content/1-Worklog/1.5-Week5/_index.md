---
title: "Week 5 Worklog"
date: "2026-05-15"
weight: 5
chapter: false
pre: " <b> 1.5. </b> "
---

### Focus this week
* Learn about Auto Scaling Groups and Launch Templates.
* Configure web server scaling based on CPU utilization.
* Test the application when an instance is automatically replaced.

### Work done
| Day | Task | Start Date | Completion Date | Reference Material |
| --- | --- | --- | --- | --- |
| 6 | - **Launch Template** <br> - Create a launch template from last week's web server AMI <br> - Choose an instance type, key pair, and Security Group <br> - Add user data to update the web page at boot <br> - Create a new version to test configuration changes | 05/15/2026 | 05/15/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 2 | - **Auto Scaling Group** <br> - Create an Auto Scaling Group from the launch template <br> - Set desired capacity to 2, minimum to 1, maximum to 4 <br> - Select subnets for the instances <br> - Check activity history after launch | 05/18/2026 | 05/18/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 3 | - **Scaling policies** <br> - Create a target tracking policy for 50% average CPU <br> - Create a CloudWatch alarm for high CPU <br> - Use stress-ng to generate load on a test instance <br> - Watch scale out and scale in in the Activity tab | 05/19/2026 | 05/19/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 4 | - **Health checks** <br> - Terminate one instance in the Auto Scaling Group <br> - Watch the ASG create a replacement instance <br> - Check grace period and health check type settings <br> - Note the difference between manual and automatic scaling | 05/20/2026 | 05/20/2026 | <https://cloudjourney.awsstudygroup.com/> |

### What I took away
* Created a Launch Template from the web server AMI.
* Auto Scaling Group keeps 2 initial instances and can scale to 4.
* Target tracking policy responds when CPU increases during the test.
* A terminated instance is replaced automatically by the Auto Scaling Group.
