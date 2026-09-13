# 13 — Hands-on Projects

Reading documentation is useful. Deploying something and then discovering why it broke is more educational.

## 🟢 Beginner projects

1. Linux server deployment
2. Git branching workflow
3. Dockerize a Flask application
4. GitHub Actions CI pipeline
5. Static website deployment
6. AWS EC2 deployment
7. Terraform VPC

Each project should include:

- Architecture
- Prerequisites
- Implementation
- Security checklist
- Troubleshooting
- Cost considerations
- Cleanup instructions
- Interview questions

## 🟡 Intermediate projects

1. Three-tier AWS application
2. Docker + CI/CD platform
3. Kubernetes application deployment
4. Terraform + AWS environment
5. Argo CD GitOps deployment
6. Prometheus + Grafana observability
7. Kubernetes policy enforcement
8. Secure container supply chain

## 🔴 Advanced projects

### 1. Production-style EKS platform

```text
Terraform/OpenTofu
      ↓
AWS VPC + IAM
      ↓
EKS
      ↓
Helm
      ↓
Argo CD
      ↓
Application
      ↓
Observability + Security
```

### 2. Secure DevSecOps supply chain

```text
GitHub
 ↓
SAST + SCA + Secrets
 ↓
IaC Security
 ↓
Build
 ↓
Container Scan
 ↓
SBOM
 ↓
Signing + Provenance
 ↓
Policy Verification
 ↓
Deployment
```

### 3. Cloud-native security platform

Combine:

- EKS
- Cilium
- Tetragon
- Kyverno
- GuardDuty
- Security Hub
- EventBridge
- Lambda
- centralized observability

### 4. Internal Developer Platform

Build a golden path using:

- Backstage
- GitHub
- CI/CD
- Terraform/OpenTofu
- GitOps
- Kubernetes
- policy enforcement
- observability

## 🏆 Capstone rule

A project is portfolio-ready when you can explain:

**Architecture → implementation → security → failure modes → monitoring → cost → trade-offs → recovery.**
