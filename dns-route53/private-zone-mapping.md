# Route 53 Private DNS Mapping

## Purpose
To enable secure internal communication between application and backend services using **DNS names instead of IP addresses**.

---

## Private Hosted Zone
A private hosted zone was created in Route 53 and associated with the VPC.

### Example Records

| DNS Name | Target |
|-------|-------|
| db01.internal | MySQL EC2 private IP |
| mc01.internal | Memcache EC2 private IP |
| rmq01.internal | RabbitMQ EC2 private IP |

---

## Benefits
- No hardcoded IPs
- Simplified scaling and replacement
- Cleaner application configuration
- Improved security

---

## Usage
Application configuration files reference DNS names instead of IP addresses for backend connectivity.
