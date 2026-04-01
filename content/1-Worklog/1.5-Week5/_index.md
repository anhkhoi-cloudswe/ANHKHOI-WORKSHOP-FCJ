---
title: "Week 5 Worklog"
date: 2026-02-02
weight: 5
chapter: false
pre: " <b> 1.5. </b> "
---

## Overview
Week 5 marks the beginning of the FPT Event Management System development phase. This week focuses on designing the microservices architecture, technology stack selection (Go, Docker), and infrastructure setup on AWS.

## Tasks

### Day 2: Microservices Architecture Design
- Define domain boundaries and service boundaries
- Design service-to-service communication patterns (gRPC, REST APIs)
- Plan data consistency strategies (eventual consistency, saga pattern)
- Document service dependencies and deployment topology

### Day 3: Technology Stack & Development Environment
- Select Go as the primary backend language
- Setup local development environment (Go SDK, tooling)
- Configure Docker for containerization
- Setup Docker Compose for multi-service orchestration locally

### Day 4: Infrastructure Design on AWS
- Design container orchestration strategy (ECS Fargate vs EKS)
- Plan VPC architecture for microservices deployment
- Design inter-service communication (Security groups, VPC Endpoints)
- Plan database per service strategy

### Day 5: AWS Infrastructure Setup
- Setup VPC with appropriate subnets for container services
- Configure security groups for service-to-service communication
- Create ECR repositories for each microservice
- Setup CloudWatch log groups for centralized logging

### Day 6: CI/CD Pipeline Foundation
- Setup GitHub repository structure for microservices
- Plan CI/CD workflow using GitHub Actions
- Define build, test, and deployment stages
- Create infrastructure as code templates (CloudFormation/Terraform)

## Achievements
✅ Designed comprehensive microservices architecture adhering to domain-driven design principles  
✅ Established Go-based backend technology stack with Docker containerization  
✅ Configured AWS VPC infrastructure optimized for containerized microservices deployment  
✅ Created ECR repositories and automated image management pipeline  
✅ Implemented centralized logging using CloudWatch log groups  
✅ Established foundation for CI/CD automation using Infrastructure as Code  

## Resources Used
- AWS Architecture Best Practices
- Docker and Docker Compose
- Go Programming Language SDK
- GitHub Repository Management
- AWS CloudFormation / Terraform

## Notes
- Microservices architecture requires careful service boundary definition
- Each service should have its own database following CQRS patterns when needed
- Service discovery is critical in distributed systems
- Implement proper circuit breaker patterns for resilience
- Plan for cross-cutting concerns (logging, tracing, metrics) from the start
| 5 (Thu) | - **Implement Service Communication:** <br>&emsp; + Configure inter-service REST API calls <br>&emsp; + Implement circuit breaker pattern for resilience <br>&emsp; + Set up service discovery mechanism | 02/05/2026 | 02/05/2026 | Service Communication Guide |
| 6 (Fri) | - **Infrastructure Setup:** <br>&emsp; + Set up RDS database cluster for persistence <br>&emsp; + Configure VPC networking for service-to-service communication <br>&emsp; + Implement logging and monitoring foundation with CloudWatch | 02/06/2026 | 02/06/2026 | AWS Infrastructure Setup |

### Week 5 Achievements:

* Designed comprehensive Microservices Architecture for FPT Event Management System with six core services.
* Established clear service boundaries, API contracts, and data ownership patterns.
* Created Docker environment with Docker Compose for local development and testing.
* Implemented base Go service templates with proper project structure and configuration management.
* Set up inter-service communication patterns with resilience mechanisms (circuit breaker, timeout policies).
* Configured AWS infrastructure foundation: VPC, RDS clusters, and CloudWatch monitoring.
* Prepared foundation for Weeks 6-10 service-by-service development and integration.
