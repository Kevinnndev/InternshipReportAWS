---
title: "Week 7 Worklog"
date: "2026-05-29"
weight: 7
chapter: false
pre: " <b> 1.7. </b> "
---

### Focus this week
* Learn DNS and how Amazon Route 53 resolves domain names.
* Create a hosted zone and basic DNS records.
* Connect a domain name to the Application Load Balancer.

### Work done
| Day | Task | Start Date | Completion Date | Reference Material |
| --- | --- | --- | --- | --- |
| 6 | - **DNS and Route 53 overview** <br> - Review DNS resolver, nameserver, and TTL <br> - Learn public hosted zones and private hosted zones <br> - Distinguish A, AAAA, CNAME, MX, and TXT records <br> - Use nslookup to inspect records for a website | 05/29/2026 | 05/29/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 2 | - **Hosted zones and records** <br> - Create a public hosted zone for a test domain <br> - Check the four Route 53 nameservers <br> - Create test A and CNAME records <br> - Adjust TTL and check propagation | 06/01/2026 | 06/01/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 3 | - **Route 53 Alias** <br> - Create an Alias A record pointing to Application Load Balancer <br> - Check the app through DNS instead of the ALB DNS name <br> - Create an HTTP health check for the /health endpoint <br> - View health check status in the Route 53 console | 06/02/2026 | 06/02/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 4 | - **Routing policies** <br> - Compare simple, weighted, latency, and failover routing <br> - Try weighted routing with two test records <br> - Note when failover routing is useful <br> - Save the DNS records used by the web app | 06/03/2026 | 06/03/2026 | <https://cloudjourney.awsstudygroup.com/> |

### What I took away
* Understand how DNS resolves requests and the record types used most often.
* Created a hosted zone with A, CNAME, and Alias records.
* Test domain points to the Application Load Balancer.
* Route 53 HTTP health check works with the /health endpoint.
