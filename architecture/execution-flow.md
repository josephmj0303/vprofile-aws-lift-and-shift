# Execution Flow – AWS Lift & Shift Deployment

This document describes the step-by-step execution flow used to deploy the VProfile application on AWS using a Lift & Shift strategy.

---

## Deployment Steps

1. Login to AWS account
2. Create EC2 key pairs
3. Create security groups for each tier
4. Launch EC2 instances using **user-data (Bash scripts)**
5. Configure Route 53 private hosted zone
6. Build application artifact (WAR file)
7. Upload artifact to Amazon S3
8. Download artifact on Tomcat EC2 instances
9. Configure Application Load Balancer with HTTPS
   - Certificate issued via AWS Certificate Manager
10. Map ALB DNS name to public domain (GoDaddy)
11. Verify application accessibility
12. Configure Auto Scaling Group for Tomcat instances

---

## Key Design Principles

- No application code changes
- Infrastructure automation via user-data
- Private DNS for backend communication
- Secure HTTPS access
- Scalable application tier

---

## Outcome

A production-ready, scalable, and secure AWS deployment that mirrors real-world enterprise cloud migrations.
