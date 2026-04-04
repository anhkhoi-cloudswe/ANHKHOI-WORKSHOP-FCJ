---
title: "Event 4"
date: 2026-04-04
weight: 4
chapter: false
pre: " <b> 4.4. </b> "
---

## 1. Elixir as a Unified Solution for Highly Concurrent & Fault-Tolerant DevOps Infrastructure

### Event Objectives

- Introduction to **Elixir** and **functional programming** on **BEAM VM**.
- Understanding how **Elixir** achieves high **fault-tolerance** through **OTP** and **process supervision**.
- Applying **Elixir** to **DevOps pipelines** as a unified toolset.

### Speaker

- **Nguyen Ta Minh Triet** — R&D Member at ITea Lab, SAP Developer Intern at Bosch GSV
  - Swinburne 3rd-year Computer Science/Software Development student
  - Published 2 conference papers on Elixir (CCIOT 2025, SCI 2026)
  - FCJ member and ITea Lab contributor

### Key Highlights

- **BEAM VM** — the same foundation as Erlang with Ruby-like syntax.
- **BEAM Process**: lightweight processes with no shared memory, supporting millions of concurrent processes.
- **"Let It Crash" philosophy** — supervisors automatically restart failed processes instead of using try/catch.
- **Hot Code Upgrades** — upgrade systems without downtime.
- **Unified toolset** — one language for testing, deployment, and monitoring.
- **Real-world case study**: migration from AWS Lambda to Elixir reduced costs from **$30K/month → $397/month**.

### Key Takeaways

- **Design Mindset**: functional & immutable architecture.
- **Technical Architecture**: process-based concurrency with robust supervision trees.
- **Modernization Strategy**: replacing serverless with BEAM for cost optimization and fault tolerance.
- **High concurrency capability**: demonstrated with 2M+ WebSocket connections per server.

### Applying to Work

- Apply **"Let It Crash"** philosophy to simplify error handling in distributed systems.
- Consider **BEAM/Elixir** for services requiring high concurrency (IoT, WebSocket, real-time streaming).
- Optimize cloud costs by migrating from serverless to **Elixir** for suitable workloads.

### Event Experience

- Live demo of **Elixir IoT Edge Server** running in Docker.
- Hands-on experience with **concurrency** and **OTP supervision trees**.
- Real-world performance benchmarks: **2M WebSocket connections** per single server.
- Learning from a speaker with published papers on Elixir architecture.

---

## 2. Architecting for the Cloud with Kubernetes

### Event Objectives

- Understand challenges of running containers manually at scale.
- Master **Kubernetes** architecture and core components.
- Learn how to start learning and practicing Kubernetes in local environments.

### Speaker

- **Bao Huynh** — Junior Cloud Native Developer at Endava Vietnam, Founder of ITea Lab
  - Swinburne alumni
  - Former Cloud DevOps Engineer at NAB Innovation Centre Vietnam

### Key Highlights

- **Container Orchestration**: automate deployment, scaling, self-healing across clusters.
- **Kubernetes Architecture**: Control Plane (etcd, api-server, scheduler) + Worker Nodes.
- **Core objects**: Pod, ReplicaSet, Deployment, ConfigMap, Secret, Jobs, Services.
- **Manifest YAML + kubectl basics**: writing and applying configurations.
- **EKS** (Amazon Elastic Kubernetes Service): running Kubernetes on AWS with minimal setup and tight AWS integration.
- **Helm Charts & K9s**: package manager and terminal UI for Kubernetes management.

### Key Takeaways

- **Design Mindset**: declarative configuration and infrastructure.
- **Technical Architecture**: cluster, node, pod hierarchy for scalable application design.
- **Modernization Strategy**: transitioning from Docker Compose → Kubernetes for production workloads.
- **Standardized deployment patterns**: blue-green, canary, and rolling updates.

### Applying to Work

- Use **Minikube/K3D** for practicing Kubernetes on personal laptops.
- Write **Deployment + Service manifests** for current projects.
- Adopt **Helm** for standardizing deployments across dev/staging/prod environments.
- Normalize **CI/CD and deployment patterns** with Kubernetes best practices.

### Event Experience

- Live demo of a **Kubernetes cluster** using Minikube/K3D.
- Hands-on **kubectl commands** for real-world scenarios.
- Networking discussions comparing EKS vs self-hosted Kubernetes.
- Recommended learning resources: **LFS158**, **kubernetes.io**, **Kelsey Hightower** tutorials.

---

## 3. Infrastructure as Code with Terraform on AWS

### Event Objectives

- Understand why **ClickOps** is unsuitable for production environments.
- Compare **IaC tools**: CloudFormation, CDK, Terraform.
- Master **Terraform** workflow and core concepts on AWS.

### Speaker

- **Thinh Nguyễn** (Khanh Phuc Thinh Nguyen) — FCAJ Cloud Engineer Trainee, ITea Lab Operations Team
  - Swinburne 3rd-year Computer Science student
  - FCAJ member 2025
  - Operations Team contributor at ITea Lab

### Key Highlights

- **ClickOps vs IaC**: manual cloud console operations are slow, error-prone, and difficult to collaborate on → **IaC** solves these through automation and reproducibility.
- **AWS CloudFormation**: YAML/JSON templates, Stack management, Drift Detection.
- **AWS CDK**: Infrastructure as code using real programming languages (Python, TypeScript, etc.), with 3 levels of Constructs (L1/L2/L3).
- **Terraform**: multi-cloud support (AWS/Azure/GCP), HCL syntax, state management with tfstate files.
- **Terraform workflow**: init → validate → plan → apply → destroy.
- **Choosing an IaC tool**: depends on single/multi-cloud requirements, team background, and ecosystem.

### Key Takeaways

- **Design Mindset**: "infrastructure as code" — version-controlled, reviewable, reproducible.
- **Technical Architecture**: provider → resource → state model for infrastructure management.
- **Modernization Strategy**: gradual migration from ClickOps → IaC.
- **Infrastructure reproducibility**: easily clone environments for dev/staging/prod consistency.

### Applying to Work

- Write **Terraform scripts** to provision dev environments instead of manual console clicks.
- Use **CDK L2/L3 Constructs** to deploy AWS resources with built-in best practices.
- Enable **Drift Detection** in CloudFormation to identify untracked infrastructure changes.
- Version-control all infrastructure code for audit trails and easy rollback.

### Event Experience

- Live demo creating **S3 buckets** using 3-level **CDK Constructs**.
- Hands-on **Terraform commands** demonstration.
- Direct comparison: **CloudFormation vs CDK vs Terraform** in real scenarios.
- Discussion of alternatives: **OpenTofu**, **Pulumi**, and other IaC tools.

---

## Overall Event Takeaways

### Key Themes

- **Modern DevOps Architecture**: from monolithic VMs → containers → orchestrated Kubernetes → serverless alternatives, optimizing cost and operational burden.
- **Event-Driven Systems**: reduce coupling and enable high throughput through message queues and event buses.
- **Cloud-Native Design Mindset**: stateless design, horizontal scaling, resilience, and observability from day one.
- **Cost Optimization**: demonstrated with real cases (Elixir reducing $30K/month to $397/month).

### Emerging Tools & Practices

- **Amazon Q Developer**: AWS AI assistant supporting code writing, cloud resource creation, and architecture suggestions.
- **Unified DevOps Toolsets**: Kubernetes ecosystem, IaC frameworks (Terraform/CDK), and functional languages (Elixir) converging on common patterns.

### Applying to Modernization Strategy

- Gradually migrate monolithic applications to microservices on Kubernetes.
- Automate infrastructure using IaC (Terraform/CloudFormation/CDK) for consistency and auditability.
- Adopt event-driven architectures to reduce system coupling.
- Consider **Elixir** for high-concurrency, fault-tolerant workloads.
- Leverage **AI assistants** (Amazon Q Developer) to accelerate DevOps and development productivity.
