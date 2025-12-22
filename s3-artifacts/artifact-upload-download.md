# Application Artifact Management using S3

## Overview
Amazon S3 is used to store application build artifacts.

---

## Workflow
1. Build application locally or via CI
2. Upload WAR file to S3 bucket
3. Tomcat EC2 instances download artifact during boot using user-data
4. Application deployed automatically

---

## Advantages
- Centralized artifact storage
- Easy rollback
- Decoupled build and deployment
