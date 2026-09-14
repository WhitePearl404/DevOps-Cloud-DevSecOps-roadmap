# AWS Deep Dive

AWS should be learned as an architecture system, not as a list of service names.

## 💡 Learning model

For every AWS service ask:

1. What problem does it solve?
2. What is the request/data path?
3. What permissions does it need?
4. What happens when it fails?
5. How is it monitored?
6. How does it scale?
7. What does it cost?
8. How can it be misconfigured?

## 🟢 Core path

### Identity

- IAM users and roles
- policies and policy evaluation
- STS and temporary credentials
- least privilege
- workload identity
- IAM Access Analyzer

### Networking

- VPC
- CIDR and subnets
- route tables
- Internet Gateway
- NAT Gateway
- security groups
- network ACLs
- VPC endpoints
- Transit Gateway
- Route 53

### Compute

- EC2
- Auto Scaling
- ECS
- EKS
- Lambda

### Storage

- S3
- EBS
- EFS
- lifecycle and backup concepts

### Databases

- RDS
- Aurora concepts
- DynamoDB concepts
- caching concepts

### Edge and application delivery

- Application Load Balancer
- Network Load Balancer
- CloudFront
- WAF

## 🟡 Architecture skills

Build these patterns:

1. Single-AZ application
2. Multi-AZ three-tier application
3. Private application tier with managed database
4. Containerized application on ECS
5. Containerized application on EKS
6. Multi-account workload isolation
7. Centralized logging and security findings

## 🛡️ Security path

```text
Identity
  ↓
Least privilege
  ↓
Network segmentation
  ↓
Encryption
  ↓
Secrets management
  ↓
Audit logging
  ↓
Threat detection
  ↓
Centralized findings
  ↓
Automated response
```

Study together:

- IAM
- KMS
- Secrets Manager
- CloudTrail
- Config
- GuardDuty
- Security Hub
- Inspector
- Macie
- Security Lake
- EventBridge

## 🚨 Failure thinking

For each architecture intentionally ask:

- What if an AZ fails?
- What if the load balancer is unhealthy?
- What if credentials leak?
- What if the database becomes unavailable?
- What if an administrator makes a dangerous change?
- What if logs are deleted or inaccessible?
- What if a workload becomes publicly reachable?

## ⚫ Interview exercise

Design a production web platform with:

- public edge
- private application tier
- private database
- multi-AZ availability
- least-privilege IAM
- encrypted data
- centralized audit logs
- threat detection
- automated deployment
- backup and recovery

Explain the request path, failure domains, security boundaries and trade-offs.
