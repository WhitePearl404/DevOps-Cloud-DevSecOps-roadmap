# Technology Matrix

A practical guide to what to learn now, what to learn next, and what to watch.

> Priority is based on industry relevance, transferability, ecosystem maturity, and usefulness in production environments. It is not a popularity contest between logos.

| Technology | Area | Status | Priority | Depth | Learn after |
|---|---|---:|---:|---|---|
| Linux | Foundations | 🟢 Core | 🔥 Critical | Master | — |
| Git | Foundations | 🟢 Core | 🔥 Critical | Master | — |
| Docker | Containers | 🟢 Production | 🔥 Critical | Use | Linux |
| GitHub Actions | CI/CD | 🟢 Production | 🔥 Critical | Use | Git |
| AWS | Cloud | 🟢 Production | 🔥 Critical | Master | Networking |
| Terraform | IaC | 🟢 Production | 🔥 Critical | Master | Cloud fundamentals |
| Kubernetes | Orchestration | 🟢 Production | 🔥 Critical | Master | Containers |
| Helm | Kubernetes packaging | 🟢 Production | 🔥 High | Use | Kubernetes |
| Argo CD | GitOps | 🟢 Production | 🔥 High | Use | Kubernetes + Git |
| Prometheus | Metrics | 🟢 Production | 🔥 High | Use | Linux + Kubernetes |
| Grafana | Visualization | 🟢 Production | 🔥 High | Use | Prometheus |
| OpenTelemetry | Observability | 🟢 Graduated | 🔥 High | Use | Observability basics |
| Kyverno | Policy-as-code | 🟢 Graduated | 🔥 High | Use | Kubernetes |
| Cilium | Networking/security | 🟢 Production | 🔥 High | Master | Kubernetes networking |
| Trivy | DevSecOps | 🟢 Production | 🔥 High | Use | Containers |
| Semgrep | SAST | 🟢 Production | High | Use | Programming basics |
| Gitleaks | Secrets security | 🟢 Production | High | Use | Git |
| Checkov | IaC security | 🟢 Production | High | Use | Terraform |
| Syft | SBOM | 🟢 Production | High | Use | Containers |
| Grype | Vulnerability scanning | 🟢 Production | High | Use | SBOM |
| Cosign / Sigstore | Artifact signing | 🟢 Production | High | Use | Container registries |
| Backstage | Platform engineering | 🟢 Production | High | Use | Kubernetes + CI/CD |
| Crossplane | Cloud/platform control | 🟡 Advanced | Medium-High | Awareness → Use | Kubernetes + IaC |
| Tetragon | Runtime security | 🟡 Advanced | Medium-High | Awareness → Use | Cilium + Kubernetes |
| Flux | GitOps | 🟢 Production | Medium | Awareness → Use | Argo CD |
| Istio | Service mesh | 🟡 Advanced | Medium | Awareness → Use | Kubernetes networking |
| Kubeflow | AI/ML infrastructure | 🟡 Specialized | Medium | Awareness | Kubernetes |
| Firecracker | Secure workload isolation | 🟡 Advanced | Medium | Awareness | Linux + containers |
| gVisor | Container isolation | 🟡 Advanced | Medium | Awareness | Containers |
| Agentic cloud engineering | Emerging | 🧪 Emerging | Watch | Awareness | Strong cloud fundamentals |

## 🧠 Depth model

Use the **Learn → Use → Master → Awareness** model instead of treating every tool equally.

### 🟢 Learn
Understand the purpose, architecture, core concepts and basic operation.

### 🔵 Use
Build a working implementation and troubleshoot common failures.

### 🟣 Master
Understand internals, production failure modes, security, performance and architectural trade-offs.

### ⚪ Awareness
Know what the technology does, when it may help, and what problem it solves. Do not spend weeks mastering it yet.

> A technology can be important without requiring mastery for every role. Depth should follow the career path you choose.

## How to use this matrix

### 🔥 Critical
Learn deeply. These skills appear repeatedly across DevOps, Cloud, Platform Engineering and DevSecOps roles.

### High
Learn enough to build and explain production-style implementations.

### Medium-High
Add after the core stack is comfortable. These can differentiate an advanced candidate.

### Medium / Emerging
Explore through labs and architecture studies. Do not replace fundamentals with trend-chasing.

## 2026+ focus areas

The modern cloud-native stack increasingly connects:

**Cloud → Kubernetes → GitOps → Security → Supply Chain → Observability → Platform Engineering → AI-enabled infrastructure**

The roadmap therefore treats security and operations as part of engineering rather than a final checkbox.

## Review policy

- Review this matrix at least every 6 months.
- Prefer official project documentation for current features.
- Do not mark a technology “obsolete” merely because a newer tool exists.
- Do not recommend an emerging tool as a replacement for a mature foundational skill without evidence.
