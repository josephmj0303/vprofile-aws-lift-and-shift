# Security Groups Design

## Principle
Least privilege and tier-based isolation.

---

## Security Group Breakdown

### ALB Security Group
- Inbound: HTTPS (443) from internet
- Outbound: App Security Group

### Application Security Group
- Inbound: 8080 from ALB SG
- Outbound: Backend SGs

### Backend Security Group
- Inbound: MySQL, Memcache, RabbitMQ ports from App SG
- No public access

---

## Result
- Secure traffic flow
- No backend exposure
- Clear network boundaries
