---
title: "Event 2"
date: 2026-06-27
weight: 2
chapter: false
pre: " <b> 4.2. </b> "
---

# Reflection Report: Cloud, AI Agent, and Amazon Q on AWS

### Event information

The **Cloud, AI Agent, and Amazon Q on AWS** event focused on how AI Agents can be applied in real systems on AWS. The event covered several topics, including cloud career development, Voice Agents, DevOps AI Agents, Amazon Q in human resource management, and Private Connection design for better security.

What made this event useful for me was that many sessions included practical demos. Instead of only explaining the concept of AI Agents, the speakers showed how AI can support tasks that are close to enterprise environments, such as voice customer support, incident analysis, CV processing, and secure connection to internal systems.

### Speakers

- **Steve Trần** - Founder of Cloud Thinker  
  Topic: *Career Path with Cloud and Introduction to Cloud Thinker*

- **Hiếu Nghị** - Renova Cloud  
  Topic: *Building an AI Voice Assistant*

- **Kiệt** - AWS Study Group  
  Topic: *Voice Agent and AI Applications on AWS*

- **Trung Nguyễn** - Founder & CEO of R AI  
  Topic: *Deploying Voice AI for the Vietnamese Language*

- **Bảo** - Cloud Kinetic  
  Topic: *Introduction to AWS DevOps AI Agent*

- **Nguyên Nguyễn** - Cloud Engineer, Cloud Kinetic  
  Topic: *DevOps AI Agent and Incident Handling on AWS*

- **Trường** - Solution Architect, Noventic  
  Topic: *Applying Amazon Q in Human Resource Management*

- **Minh Anh** - Solution Architect, Noventic  
  Topic: *Amazon Q and HR Workflow Automation*

- **Toàn Nguyễn** - AWS Security Builder  
  Topic: *Securing Amazon Q with Private Connection*

### What I learned from the sessions

#### Career path with Cloud and Cloud Thinker

The opening session by **Steve Trần** focused on the cloud learning journey and career development. The point I remembered most was that learning cloud is not always a straight path. The speaker shared difficulties, failed certification attempts, technology changes, and how he continued developing in the AWS field.

From this session, I learned that cloud is a long-term learning path. Besides knowing how to use services, learners need to understand systems, solve problems, and keep up with new technologies. In the AI era, cloud and backend engineers also need to know how to use AI to support their work while still keeping a strong technical foundation.

The speaker also introduced Cloud Thinker’s **Agentic Platform**, which focuses on use cases such as incident handling, code review, cloud cost optimization with FinOps, and security testing. The comparison between Single Agent and Multi-Agent architecture helped me understand that not every problem should be handled by one agent. For complex workflows, separating roles into multiple agents can make the system easier to control.

#### Building an AI Voice Assistant

The sessions by **Hiếu Nghị**, **Kiệt**, and **Trung Nguyễn** helped me understand the architecture of a Voice Agent more clearly. A typical Voice AI system includes three main parts: Speech-to-Text to convert voice into text, an LLM to process the content, and Text-to-Speech to generate voice output.

In the demo, the Voice Agent was used to answer questions about Apple products such as the MacBook Pro. This demo helped me imagine how AI can support customer service or product consultation. However, when deploying Voice AI for Vietnamese, there are additional challenges such as latency, regional accents, forms of address, and handling user interruptions.

One important point was the **Human-in-the-loop** model. AI can provide a lot of support, but when the answer is uncertain or the customer is not satisfied, the system still needs to transfer the case to a human. This helped me understand that AI in real products should be designed to work with humans, not operate completely on its own.

#### AWS DevOps AI Agent and incident handling

The sessions by **Bảo** and **Nguyên Nguyễn** discussed how AI Agents can support DevOps when systems have incidents. Before this event, I imagined that DevOps engineers had to manually check logs, metrics, dashboards, and alerts to find the root cause. Through this session, I understood that an AI Agent can help collect context, analyze operational data, and suggest mitigation steps faster.

The main ideas of DevOps AI Agent included:

- Context Learning to understand the system context.
- Control so humans still make the final decision.
- Integration with operations tools.
- Collaboration through Slack, ServiceNow, or internal platforms.
- Cost-effective operation based on actual runtime.

In the demo, the speakers simulated a situation where an e-commerce application running on AWS ECS became slow because of a denial-of-service style attack. The DevOps AI Agent analyzed the information and suggested a mitigation plan in a short time. The lesson I learned is that an AI Agent is only useful when the system has good observability. Without enough logs, metrics, and monitoring information, AI also has difficulty finding the correct cause.

#### Amazon Q in human resource management

The sessions by **Trường** and **Minh Anh** showed how Amazon Q can be used in human resource workflows. HR teams often handle repetitive tasks such as writing job descriptions, reading CVs, evaluating candidates, and preparing reports. Amazon Q can support these steps by connecting to internal data and performing actions as part of a workflow.

In the demo, Amazon Q was used to create a job description for a Junior Cloud Engineer position, scan a folder of CVs, analyze candidate skills, score candidates, and export an HTML report. I found this example practical because AI was not only answering questions but also participating in a real workflow.

However, this session also showed that HR data is sensitive. When using AI in enterprises, convenience is not enough. Access permission, data protection, and output control must also be considered carefully.

#### Securing Amazon Q with Private Connection

The session by **Toàn Nguyễn** focused on security when Amazon Q connects with MCP Servers or third-party systems. If data travels through the public Internet, the system may face risks such as data leakage, man-in-the-middle attacks, or network-level threats.

The proposed solution was to move the connection flow into a private network through **Private Connection**. This architecture can use components such as VPC Connection, Interface Endpoint, Route 53 Resolver, Application Load Balancer, and TLS to reduce public Internet exposure.

This session helped me understand that security for AI systems is not only about prompts, models, or application logic. In enterprise deployment, network architecture, DNS, endpoints, encryption, and access control are also important. Although this approach can add operational cost, it is suitable for systems that process internal or customer data.

### Main takeaways

After the event, I noted several key lessons:

- AI Agents can support many areas, such as customer service, DevOps, HR, and security.
- When building Voice Agents for Vietnamese, latency, regional accents, forms of address, and conversation experience need careful design.
- DevOps AI Agents require systems with good logs, metrics, and monitoring to analyze incidents accurately.
- Amazon Q can support enterprise automation, but it must come with data control and access permissions.
- Private Connection is important when connecting AI to internal systems.
- AI should support human decision-making, not completely replace humans in important steps.

### Connection with FCAJ learning

This event was closely related to what I learned in FCAJ, such as ECS, VPC, Load Balancer, IAM, security, and AWS application deployment. Before the event, I mainly learned these services through separate labs. After the event, I understood better how they can be combined in real AI systems.

The DevOps AI Agent session made me pay more attention to logging and monitoring. When building a backend or deploying an application, having the main function work is not enough. The system also needs observability so that when errors happen, operators can understand the cause and respond faster.

### Personal reflection

I found the **Cloud, AI Agent, and Amazon Q on AWS** event very useful because many demos were close to real work. Topics such as Voice Agent, DevOps AI Agent, Amazon Q for HR, and Private Connection helped me understand how AI is being introduced into enterprise systems.

After the event, I realized that to follow the backend and cloud direction, I should not only learn API programming. I also need to understand cloud deployment, observability, security, and how AI Agents are integrated into systems. These are the areas I want to continue learning after the FCAJ program.

### Event photos

![Event 2 participation photo](/images/4-EventParticipated/event2.jpg)