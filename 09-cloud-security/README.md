# 09 — Cloud Security

This section connects cloud architecture with security engineering.

## 🟢 Beginner

- Shared responsibility model
- IAM fundamentals
- Least privilege
- Encryption at rest/in transit
- Logging and auditing
- Network segmentation
- Secrets management

## 🟡 Intermediate

### AWS
- IAM Access Analyzer
- Security Hub
- GuardDuty
- Inspector
- Macie
- AWS Config
- CloudTrail
- KMS
- Secrets Manager
- Security Lake

### Kubernetes
- RBAC
- Pod Security Standards
- NetworkPolicy
- Secrets
- Image security

## 🔴 Advanced

- Zero Trust
- Defense in depth
- Multi-account security architecture
- SCPs
- Centralized logging
- Detection engineering
- Event-driven response
- Incident response automation
- Runtime security
- MITRE ATT&CK mapping

## 🧩 Detection and response

```text
Cloud / Kubernetes telemetry
          ↓
Detection
          ↓
Security Hub / SIEM
          ↓
EventBridge
          ↓
Lambda / Automation
          ↓
Containment
          ↓
Investigation
          ↓
Recovery
          ↓
Lessons learned
```

## ⚫ Interview focus

- How do you design least-privilege IAM?
- How would you secure an EKS cluster?
- How do GuardDuty and Security Hub differ?
- How would you respond to compromised AWS credentials?
- How do SCPs differ from IAM policies?
- How do you design centralized security logging?
- How would you implement Zero Trust in a cloud environment?
