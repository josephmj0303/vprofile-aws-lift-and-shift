# Tomcat Auto Scaling Group

## Objective
Ensure application availability and scalability under varying traffic conditions.

---

## Configuration
- Launch Template with user-data
- Min instances: 1
- Max instances: 4
- Desired capacity: 1

---

## Health Checks
- ALB health checks
- Unhealthy instances are automatically replaced

---

## Benefits
- Fault tolerance
- Horizontal scalability
- Zero manual intervention
