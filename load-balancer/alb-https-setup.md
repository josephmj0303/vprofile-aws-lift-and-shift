# Application Load Balancer – HTTPS Setup

## Overview
An **internet-facing Application Load Balancer (ALB)** is used as the entry point to the application.

---

## Listener Configuration
- HTTPS (443) using ACM certificate
- HTTP (80) redirected to HTTPS

---

## Target Group
- Target type: Instance
- Protocol: HTTP
- Port: 8080 (Tomcat)

---

## Security
- ALB Security Group allows inbound HTTPS from the internet
- Outbound traffic allowed only to application security group

---

## Outcome
- Secure HTTPS access
- Load distribution
- Health-based routing
