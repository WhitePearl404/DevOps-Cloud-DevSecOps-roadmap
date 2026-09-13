# 11 — Platform Engineering

Platform engineering focuses on providing reusable, self-service capabilities that let development teams deliver software safely without rebuilding infrastructure patterns from scratch.

## 🟢 Beginner

- What platform engineering solves
- Developer experience
- Internal Developer Platform (IDP)
- Self-service
- Golden paths
- Platform vs DevOps

## 🟡 Intermediate

- Backstage
- Service catalogs
- Templates
- GitOps integration
- Infrastructure provisioning
- Environment automation
- Observability integration
- Policy enforcement

## 🔴 Advanced

- Multi-team platform architecture
- Platform APIs
- Kubernetes operators
- Crossplane concepts
- Multi-cluster platforms
- Cost governance
- Security guardrails
- Platform reliability

## 🧩 Example platform

```text
Developer
   ↓
Backstage / Developer Portal
   ↓
Golden Path
   ├── Git repository
   ├── CI pipeline
   ├── Security controls
   ├── Terraform / OpenTofu
   └── GitOps
            ↓
       Kubernetes / Cloud
            ↓
 Observability + Security
```

## ⚫ Interview focus

- What is platform engineering?
- Platform engineering vs DevOps?
- What is an IDP?
- What is a golden path?
- Why use Backstage?
- How do you prevent a platform from becoming a bottleneck?
- How should security be integrated into an IDP?
