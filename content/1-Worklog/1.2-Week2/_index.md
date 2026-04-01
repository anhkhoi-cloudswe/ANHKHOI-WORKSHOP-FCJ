---
title: "Week 2: VPC & EC2 Compute Foundations"
date: 2026-01-12
weight: 2
chapter: false
pre: " <b> 1.2. </b> "
---

## Overview
Week 2 focuses on networking and compute services - the backbone of AWS cloud infrastructure. This week covers VPC setup, EC2 instances, and IAM role integration for service authentication.

## Tasks

### Day 2: VPC Networking Basics
- Create Virtual Private Cloud (VPC) with custom CIDR blocks
- Configure Public and Private Subnets
- Setup Internet Gateway (IGW)
- Configure Route Tables for subnet routing

### Day 3: Advanced VPC Networking
- Create and configure NAT Gateway for private subnet internet access
- Setup VPC Endpoints for AWS services
- Understand VPC Peering concepts
- Configure Security Groups and Network ACLs

### Day 4: EC2 Instance Fundamentals
- Launch EC2 instances (t2.micro, t2.small)
- Understand Amazon Machine Images (AMI)
- Configure Elastic Block Store (EBS) volumes
- Manage instance lifecycle (start, stop, terminate)

### Day 5: EC2 Advanced & Instance Profiling
- Launch instances with custom security groups
- Configure Elastic IPs for persistent public addresses
- Monitor instance metrics via CloudWatch
- Understand EC2 instance families and use cases

### Day 6: IAM Roles for EC2 Services
- Create IAM Roles for EC2 instances
- Attach Instance Profiles to EC2
- Configure service-to-service authentication
- Test role-based access to AWS services (S3, DynamoDB, etc.)

## Achievements
✅ Designed and implemented secure VPC architecture with public/private subnets
✅ Deployed EC2 instances with proper security group configuration
✅ Established IAM Role-based EC2 service authentication
✅ Configured autonomous NAT Gateway for private subnet outbound connectivity
✅ Implemented VPC endpoint access patterns for AWS service integration
✅ Validated EC2 instance profiling and CloudWatch metrics monitoring

## Resources Used
- AWS VPC Console
- EC2 Dashboard
- AWS IAM Management Console
- CloudWatch Monitoring

## Notes
- VPC is the foundation of cloud network architecture
- Always use IAM Roles instead of access keys for EC2 services
- Security Groups are stateful; NACLs are stateless
- Properly isolate workloads using subnets and security controls
