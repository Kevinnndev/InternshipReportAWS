---
title: "Week 1 Worklog"
date: "2026-04-17"
weight: 1
chapter: false
pre: " <b> 1.1. </b> "
---

### Focus this week
* Understand Cloud Computing fundamentals and service models.
* Learn about the AWS Shared Responsibility Model.
* Sign up for an AWS account and secure it from day one.

### Work done
| Day | Task | Start Date | Completion Date | Reference Material |
| --- | --- | --- | --- | --- |
| 6 | - **What is Cloud Computing** <br> - Read about IaaS, PaaS, SaaS <br> - Compare On-premise vs Cloud (cost, operations, scaling) <br> - Look into AWS Regions and Availability Zones <br> - Note down the pay-as-you-go benefits | 04/17/2026 | 04/17/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 2 | - **Shared Responsibility Model** <br> - Identify what AWS handles (physical infra, hypervisor) <br> - Identify what customers manage (OS, firewall, data) <br> - Look at compliance programs: SOC 2, ISO 27001, HIPAA <br> - Write down the responsibility split table | 04/20/2026 | 04/20/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 3 | - **Signing up for AWS** <br> - Create a new account with a dedicated email <br> - Pick the Basic Support Plan <br> - Turn on MFA for Root user right away <br> - Create an IAM admin user so I stop using Root | 04/21/2026 | 04/21/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 4 | - **Initial security setup** <br> - Enable CloudTrail across all regions <br> - Create a billing alarm ($5 threshold) with CloudWatch <br> - Install AWS CLI on my machine and configure access keys <br> - Run `aws sts get-caller-identity` to confirm it works | 04/22/2026 | 04/22/2026 | <https://cloudjourney.awsstudygroup.com/> |

### What I took away
* I can now distinguish IaaS, PaaS, and SaaS and understand when each model is suitable.
* I understood the AWS shared responsibility model more clearly, especially what I need to secure on my side.
* I finished the initial account setup by enabling MFA for the Root user and creating a separate IAM admin user.
* I also configured the AWS CLI and set a 5 USD billing alarm so I could monitor usage from the beginning.
