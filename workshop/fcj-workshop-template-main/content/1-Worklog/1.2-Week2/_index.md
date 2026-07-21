---
title: "Week 2 Worklog"
date: "2026-04-24"
weight: 2
chapter: false
pre: " <b> 1.2. </b> "
---

### Focus this week
* Understand IAM structure: Users, Groups, Roles, Policies.
* Write custom IAM Policies and apply Permission Boundaries.
* Enable MFA for critical accounts and set up password policy.

### Work done
| Day | Task | Start Date | Completion Date | Reference Material |
| --- | --- | --- | --- | --- |
| 6 | - **IAM Structure** <br> - Create IAM Groups for developers and admins <br> - Attach managed policies (ReadOnlyAccess, PowerUserAccess) <br> - Create 2 IAM Users and add them to groups <br> - Check permissions with Policy Simulator | 04/24/2026 | 04/24/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 2 | - **Writing custom policies** <br> - Write a JSON policy allowing only EC2 and S3 in ap-southeast-1 <br> - Add IP condition to restrict access from company network <br> - Test with CLI using --dry-run <br> - Save the policy to a repo for reuse | 04/27/2026 | 04/27/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 3 | - **IAM Roles** <br> - Create an EC2 Instance Role with S3 access <br> - Attach the role to a running EC2 instance <br> - Test calling S3 from inside EC2 without access keys <br> - Write down the difference between Roles and Users | 04/28/2026 | 04/28/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 4 | - **MFA and password policy** <br> - Enable virtual MFA for all IAM users <br> - Set password policy: minimum 12 chars, require numbers + special chars <br> - Generate credential report and check which users don't have MFA <br> - Delete unused access keys | 04/29/2026 | 04/29/2026 | <https://cloudjourney.awsstudygroup.com/> |

### What I took away
* Built a clean IAM structure: 2 groups, managed policies, 2 users.
* Wrote a custom policy with IP and region conditions, tested with --dry-run.
* EC2 Instance Role calls S3 without keys - way more secure than using access keys.
* MFA enabled everywhere, 12-char password policy, deleted one old unused access key.
