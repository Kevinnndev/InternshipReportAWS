---
title: "Week 4 Worklog"
date: "2026-05-08"
weight: 4
chapter: false
pre: " <b> 1.4. </b> "
---

### Focus this week
* Launch EC2 and configure an environment for a web application.
* Learn about AMIs, instance types, key pairs, and user data.
* Access, monitor, and perform basic administration on Amazon Linux.

### Work done
| Day | Task | Start Date | Completion Date | Reference Material |
| --- | --- | --- | --- | --- |
| 6 | - **Launching EC2** <br> - Pick Amazon Linux 2023 AMI and t3.micro <br> - Create an ED25519 key pair and add project tags <br> - Select a Security Group for SSH and HTTP <br> - Check instance state and public IPv4 | 05/08/2026 | 05/08/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 2 | - **User data and web server** <br> - Write user data to install Nginx at boot <br> - Create an HTML landing page for the app <br> - Check Nginx with systemctl and curl <br> - Update the Security Group to open port 80 | 05/11/2026 | 05/11/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 3 | - **Amazon Linux administration** <br> - Connect through SSH and Session Manager <br> - Practice journalctl, top, df, and free <br> - Create a user without using root directly <br> - Update packages and reboot the instance | 05/12/2026 | 05/12/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 4 | - **AMI and EBS** <br> - Create an AMI from the configured web server <br> - Attach another EBS volume and mount it at /data <br> - Configure fstab to remount after reboot <br> - Terminate a test instance and check related snapshots | 05/13/2026 | 05/13/2026 | <https://cloudjourney.awsstudygroup.com/> |

### What I took away
* Launched Amazon Linux EC2 and connected through both SSH and Session Manager.
* User data installs Nginx automatically and the test page is available through HTTP.
* Can check basic Linux logs and resource usage.
* Created an AMI and attached an EBS volume to the web server.
