---
title: "Week 3: Storage, Database & DNS"
date: 2026-01-19
weight: 3
chapter: false
pre: " <b> 1.3. </b> "
---

## Overview
Week 3 covers three critical AWS services for data management and website hosting: S3 for object storage and static web hosting, RDS for relational databases, and Route 53 for DNS management.

## Tasks

### Day 2: S3 Fundamentals & Static Web Hosting
- Create S3 buckets with proper naming conventions
- Configure bucket policies and access control
- Enable Static Website Hosting on S3
- Upload and organize static content (HTML, CSS, JS)

### Day 3: S3 Advanced Configuration
- Configure CORS (Cross-Origin Resource Sharing)
- Setup CloudFront distribution with S3 origin
- Implement S3 versioning and lifecycle policies
- Configure S3 encryption and access logging

### Day 4: RDS Database Basics
- Create RDS instances (MySQL, PostgreSQL)
- Understand DB subnet groups and parameter groups
- Configure Multi-AZ deployment for high availability
- Setup automated backups and retention policies

### Day 5: RDS Advanced & Database Management
- Create read replicas for scaling read operations
- Configure database security groups and encryption
- Understand connection pooling and performance tuning
- Implement database monitoring via CloudWatch

### Day 6: Route 53 DNS & Domain Management
- Register or import domain in Route 53
- Create hosted zone and configure DNS records (A, CNAME, MX)
- Setup health checks for failover routing
- Configure alias records pointing to AWS resources
- Implement routing policies (Simple, Weighted, Latency-based)

## Achievements
✅ Successfully deployed static website on S3 with cloudfront distribution
✅ Established highly available RDS infrastructure with Multi-AZ configuration
✅ Implemented DNS infrastructure using Route 53 with health checks
✅ Configured S3 lifecycle policies for cost optimization
✅ Enabled end-to-end encryption for data at rest and in transit
✅ Created automated backup strategy for database resilience

## Resources Used
- AWS S3 Console
- RDS Database Console
- Route 53 Hosted Zones
- CloudFront Distribution Manager
- AWS Certificate Manager (ACM)

## Notes
- S3 bucket names must be globally unique across AWS
- Multi-AZ RDS provides synchronous replication for data consistency
- Route 53 supports various routing policies for different use cases
- Always implement lifecycle policies to optimize S3 storage costs
- Database backups should be retained according to compliance requirements
