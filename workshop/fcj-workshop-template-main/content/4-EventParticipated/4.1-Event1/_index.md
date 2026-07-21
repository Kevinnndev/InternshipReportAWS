---
title: "Event 1"
date: 2026-05-23
weight: 1
chapter: false
pre: " <b> 4.1. </b> "
---

# Reflection Report: AWS Vietnam Community Day 2026

### Event information

**AWS Vietnam Community Day 2026** was a community event about AWS, Cloud Computing, and Generative AI. The event included sharing sessions from people working in different roles, such as Platform Engineer, Solution Architect, DevOps Engineer, Business Systems Analyst, and AWS Community Builder.

What interested me most was how the speakers connected cloud and AI knowledge with real use cases. The event did not only talk about AWS services, but also included stories about product building, hackathon experience, AI system design, and risks when working with LLMs.

### Speakers

- **Tinh Truong** - Platform Engineer, GoTymeX  
  Topic: *Context Is Everything*

- **Pham Ng Hai Anh** - AWS Community Builder, G-AsiaPacific Vietnam  
  Topic: *Friendly AI Assistant with Amazon Quick*

- **Nguyen Tuan Thinh** - DevOps Engineer, First Cloud AI Journey  
  Topic: *From Edge to Origin: CloudFront as Your Foundation*

- **Team VIB**  
  Topic: *36 Hours with LotusHacks - Building UTMorpho from Idea to Reality*

- **Duc Dao** - Solution Architect, Cloud Kinetics  
  Topic: *Deep Dive Talk: How LLM Actually Works?*

- **Vy Lam** - Senior Business Systems Analyst, VPBank  
  Topic: *Enterprise-Grade Multi-Agent System: The Case of Startup Credit Scoring*

### What I learned from the sessions

#### Context Is Everything

The session by **Tinh Truong** helped me understand the role of context when working with Generative AI. Before this session, I often thought that a longer prompt would usually give a better result. After the session, I understood that context needs to be focused, clear, and related to the problem.

Some points I noted:

- Poor AI answers are not always caused by weak models, but often by unclear input context.
- More context does not always mean better context.
- When building AI applications, developers need to think about memory, retrieval, and how the system stores useful information.
- The idea of a “Second AI Brain” shows how AI can help store, retrieve, and process personal or organizational knowledge.

This lesson can be applied directly when I use AI to study AWS, read documentation, or debug errors. If I provide logs, goals, environment details, and actual results more clearly, the answer is usually more useful.

#### Friendly AI Assistant with Amazon Quick

The session by **Pham Ng Hai Anh** introduced how Amazon Quick Suite can support business users in tasks such as summarizing information, creating meeting notes, sending emails, and automating repetitive workflows.

The point I found important is that an enterprise AI assistant should not only answer questions. It also needs to connect with data, perform actions, and have guardrails to control the result. This is different from a normal chatbot because enterprise environments require stronger security, permission control, and governance.

#### From Edge to Origin: CloudFront as Your Foundation

The session by **Nguyen Tuan Thinh** helped me look at Amazon CloudFront beyond the basic idea of a CDN. CloudFront can support security, performance, reliability, and cost control for web systems.

The main points I noted were:

- Edge caching can reduce load on the origin and improve response time.
- AWS WAF and DDoS protection add another security layer for applications.
- HTTP/3 and QUIC can improve connection performance.
- Signed URLs, mTLS, origin failover, and stale cache are useful when designing production systems.
- Pricing should be considered early because cloud systems can create unexpected costs if they are not designed carefully.

This session was closely related to what I learned in FCAJ about CloudFront, S3, Route 53, and HTTPS.

#### 36 Hours with LotusHacks - Building UTMorpho from Idea to Reality

**Team VIB** shared their experience building UTMorpho in 36 hours during LotusHacks. UTMorpho is an AI tool that helps generate user interfaces and allows users to edit them directly on a canvas.

What I liked about this session was that the idea came from a real frustration during product development. The team then turned that problem into a hackathon project. This made me realize that a project idea does not always need to be large at the beginning. It is more important to identify the problem clearly, divide work quickly, and keep testing the result.

Some lessons I took away:

- Team coordination is very important during a hackathon.
- AI can act like a teammate that helps with ideas and speeds up development.
- Token cost and design consistency matter when building AI products.
- A demo should focus on the main flow instead of trying to include too many features.

#### Deep Dive Talk: How LLM Actually Works?

The session by **Duc Dao** explained how LLMs generate text token by token. This helped me understand why the same prompt may still produce different results, even when the temperature is low.

Important points included:

- LLMs predict the next token based on probability.
- Temperature affects randomness during token selection.
- Temperature 0 does not guarantee the exact same result every time.
- Small differences can come from GPU floating-point calculation or inference batching.
- When building LLM-based applications, developers need to accept a certain level of variance.

This is important because it reminds me not to design an AI system as if it always returns a fixed result. If stability is required, the system needs output validation, constraints, and review steps.

#### Enterprise-Grade Multi-Agent System

The session by **Vy Lam** discussed a multi-agent system for startup credit scoring. Instead of using only one agent, the system separates the work into multiple specialized agents that look at different aspects of a startup.

The agents mentioned were:

- Financial Analyst Agent
- Market Analyst Agent
- Team Evaluator Agent
- Risk Assessor Agent
- Compliance Agent

This design makes the system easier to audit, clearer in responsibility, and more suitable for enterprise problems because decisions are not based on only one factor. I found this to be a clear example of why multi-agent systems are useful for complex tasks.

### Main takeaways

After attending the event, I learned several important points:

- When using Generative AI, context and problem framing have a strong impact on output quality.
- CloudFront can play an important role in security, performance, and reliability.
- LLMs are not fully deterministic, so AI applications need validation and output control.
- Multi-agent architecture is suitable for problems that require analysis from different perspectives.
- A useful AI product should start from a real problem, not only from the technology itself.

### Connection with FCAJ learning

The event helped me connect back to the topics I learned in FCAJ, such as CloudFront, S3, IAM, security, and system design. Before the event, I mainly understood CloudFront as a content delivery service. After the event, I understood that in real systems, CloudFront is also related to access control, failover, security, and cost management.

With my interest in backend and cloud, this event gave me more motivation to study AWS, Generative AI, and system architecture more deeply. It also reminded me that knowing how to use a service is not enough. I also need to understand why the service is chosen and how it affects real operations.

### Personal reflection

I found **AWS Vietnam Community Day 2026** useful because the content was diverse and practical. The speakers did not only explain concepts but also shared examples, experience, and problems they had faced when building products or deploying systems.

After the event, I had a clearer view of the trend of combining Cloud Computing and Generative AI. It also helped me shape my learning direction toward backend development, cloud deployment, AI assistants, and scalable systems.

### Event photos

![Event 1 participation photo](/images/4-EventParticipated/event1.jpg)