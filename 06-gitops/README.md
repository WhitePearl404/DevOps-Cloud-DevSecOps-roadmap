# 06 — GitOps

## 💡 Core idea

Git is the source of truth for desired application or infrastructure state. A controller continuously reconciles the actual environment toward that state.

## 🟢 Beginner

- GitOps principles
- Desired vs actual state
- Declarative configuration
- Pull-based deployment
- Repository structure

## 🟡 Intermediate

- Argo CD
- Flux
- Application manifests
- Helm-based delivery
- Environment promotion
- Secrets management
- Sync policies
- Drift detection

## 🔴 Advanced

- Multi-cluster GitOps
- Progressive delivery
- Canary releases
- Blue/green deployment
- Policy enforcement
- Disaster recovery
- GitOps for infrastructure
- Platform engineering integration

## 🛠️ Lab

```text
GitHub
  ↓
Pull Request
  ↓
CI + Security Gates
  ↓
Container Registry
  ↓
GitOps Repository
  ↓
Argo CD / Flux
  ↓
Kubernetes
```

## ⚫ Interview focus

- What is GitOps?
- Push vs pull deployment?
- Why is Git the source of truth?
- How does Argo CD detect drift?
- How do you handle secrets in GitOps?
- How would you implement multi-environment promotion?
- How would you recover from a bad deployment?
