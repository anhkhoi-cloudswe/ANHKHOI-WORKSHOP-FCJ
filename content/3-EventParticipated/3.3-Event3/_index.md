---
title: "Event 3"
date: 2025-01-29
weight: 3
chapter: false
pre: " <b> 4.3. </b> "
---


# Summary Report: "AWS re:Invent 2025 – Application Modernization & GenAI Insights"

### Event Objectives

- Updating on important announcements from AWS re:Invent 2025 (Nova models, Trainium3 UltraServers, AI agents, GenAI, modernization, data…).
- Helping attendees understand best practices for application modernization, microservices architecture, event-driven, serverless/container, and AI-driven development.
- Creating networking opportunities between AWS experts, partners, and cloud/AI community in Vietnam to support digital transformation projects.

### Speakers

- **AWS speakers**: Solution Architects and Specialists from AWS Vietnam sharing insights on modern architecture, GenAI, and real-world implementation experience for customers in Vietnam.
- **Customer speakers/Partners**: Representatives from Vietnamese businesses and AWS partners sharing case studies on transitioning from legacy monolith to microservices, applying event-driven architecture and AI on AWS.

### Key Highlights

#### Drawbacks of Legacy Application Architecture

- Monolithic applications are difficult to scale per module; each release requires building and deploying the entire system, increasing risk and downtime.
- Technology lock-in constraints make it difficult to adopt new technologies like serverless, containers, GenAI, and real-time data because architecture is not separated.
- Low reliability and fault tolerance; a small error can affect the entire system, making it difficult to implement patterns like blue/green, canary, and resilience practices.

#### Transitioning to Modern Application Architecture – Microservices

- Breaking applications into small, independent services that can be scaled and deployed separately, suitable for small teams with faster CI/CD deployment.
- Allows choosing appropriate technology for each service (polyglot), making it easier to experiment with new features or integrate AI, streaming, and event-driven patterns.
- On AWS, microservices typically combine Amazon ECS/EKS/Lambda, API Gateway, Service Discovery, and observability stack (CloudWatch, X-Ray…).

#### Event‑Driven Architecture

- Using events to decouple services, allowing systems to be flexible and easily scalable with new consumers without affecting producers.
- On AWS, popular choices are Amazon EventBridge, Amazon SNS/SQS, and Amazon Kinesis for real-time analytics and integration between multiple domain services.
- Suitable for complex business processes (order, payment, notification, audit log…) and streaming data processing in modern architectures.

#### Compute Evolution

- Journey from traditional EC2 to containers (ECS/EKS), serverless (Lambda, Fargate), and optimized instances for AI/HPC like Trainium3 UltraServers.
- Goal is to optimize costs, enable automatic scaling, reduce infrastructure operational effort so teams can focus on business logic and customer value.

#### Amazon Q Developer

- Amazon Q Developer is an AI assistant for developers, integrated with IDE and AWS console, supporting code generation, refactoring, test creation, and architecture recommendations based on AWS best practices.
- Accelerates modernization by analyzing legacy code, suggesting migration paths, and automating infrastructure tasks (infrastructure as code, configuration).

### Key Takeaways

#### Design Mindset

- **Cloud-native first design**: Prioritize decoupling, elasticity, fault-tolerance, automation instead of just "lift-and-shift" from on-prem to cloud.
- **Domain-driven design thinking**: Separate bounded contexts clearly before transitioning to microservices and event-driven architecture.

#### Technical Architecture

- **Hybrid architecture approach**: Microservices + event-driven + serverless/containers + managed data services (Aurora, DynamoDB, streaming, vector DB).
- **Apply resilience patterns**: Circuit breaker, retry, backoff, idempotency; end-to-end observability and security by design for each service.

#### Modernization Strategy

- **Start by assessing legacy applications**: Identify domains with high business value to gradually "strangle" toward new architecture.
- **Combine CI/CD and feature flags**: Blue/green deployment reduces risk when migrating parts of systems instead of big-bang rewrites.

### Applying to Work

- **Apply monolith decomposition thinking** to company/organization systems, identify clear domains, and propose microservices or modular monolith architecture.
- **Recommend appropriate AWS services** (e.g., API Gateway + Lambda for POC, or ECS/EKS for large systems), with event-driven patterns using SQS/EventBridge for multi-system integration.
- **Start using Amazon Q Developer** in development workflow to support code writing, testing, refactoring, and learning from suggested code snippets and best practices.

### Event Experience

#### Learning from highly skilled speakers
- Appreciated how AWS and customer speakers shared real-world implementation, lessons from failures, scaling challenges, and cost optimization strategies.

#### Hands-on technical exposure
- Got practical experience with AWS services through labs and workshops, including serverless, container orchestration, data services, AI/Bedrock, and Amazon Q Developer demonstrations.

#### Leveraging modern tools
- Impressed by the GenAI ecosystem (Nova models, Bedrock, AI agents) and developer tools like Amazon Q Developer, AWS CI/CD pipelines, and DevOps automation.

#### Networking and discussions
- Connected with AWS experts, partners, VietAWS community members, students, and engineers from other companies, exchanging insights on modernization challenges and solutions.

#### Lessons learned
- **Design for failure**: Build resilience and observability into systems from the start.
- **Migration requires small, measured steps**: Avoid big-bang rewrites; use gradual migration with feature flags and canary deployments.
- **AI/GenAI is architecture extension, not add-on**: Integrate AI thoughtfully into business process and system design, not as an afterthought.

#### Some event photos

**Figure 1: Event venue overview and opening session**
![Event Overview](/images/3-EventParticipated/3.3-Event3/reInvent_RECAP_1.jpg)

**Figure 2: Check-in Session #1**
![Microservices Architecture](/images/3-EventParticipated/3.3-Event3/reInvent_RECAP_2.jpg)

**Figure 3: Check-in Session #2**
![Modernization Strategy](/images/3-EventParticipated/3.3-Event3/reInvent_RECAP_3.jpg)

**Figure 4: Showcasing AWS Services: ML/AI & Innovation Keynote #1**
![GenAI Demo](/images/3-EventParticipated/3.3-Event3/reInvent_RECAP_4.jpg)

**Figure 5: Showcasing AWS Services: ML/AI & Innovation Keynote #2**
![Networking Session](/images/3-EventParticipated/3.3-Event3/reInvent_RECAP_5.jpg)

**Figure 6: A New Year's smile – Ready for new challenges and milestones at AWS!**
![AWS Booth](/images/3-EventParticipated/3.3-Event3/reInvent_RECAP_6.jpg)

**Figure 7: Team picture and closing remarks**
![Team Picture](/images/3-EventParticipated/3.3-Event3/reInvent_RECAP_7.jpg)

> Overall, the event reinforced the importance of modern architecture thinking, practical migration strategies, and the role of AWS services in enabling scalable, secure, and intelligent applications.
