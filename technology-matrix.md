# Technology Matrix

A practical guide to what to learn now, what to learn next, and what to watch.

> Priority is based on industry relevance, transferability, ecosystem maturity, and usefulness in production environments. It is not a popularity contest between logos.

| Technology | Area | Status | Priority | Learn after |
|---|---|---:|---:|---|
| Linux | Foundations | 🟢 Core | 🔥 Critical | — |
| Git | Foundations | 🟢 Core | 🔥 Critical | — |
| Docker | Containers | 🟢 Production | 🔥 Critical | Linux |
| GitHub Actions | CI/CD | 🟢 Production | 🔥 Critical | Git |
| AWS | Cloud | 🟢 Production | 🔥 Critical | Networking |
| Terraform | IaC | 🟢 Production | 🔥 Critical | Cloud fundamentals |
| Kubernetes | Orchestration | 🟢 Production | 🔥 Critical | Containers |
| Helm | Kubernetes packaging | 🟢 Production | 🔥 High | Kubernetes |
| Argo CD | GitOps | 🟢 Production | 🔥 High | Kubernetes + Git |
| Prometheus | Metrics | 🟢 Production | 🔥 High | Linux + Kubernetes |
| Grafana | Visualization | 🟢 Production | 🔥 High | Prometheus |
| OpenTelemetry | Observability | 🟢 Graduated | 🔥 High | Observability basics |
| Kyverno | Policy-as-code | 🟢 Graduated | 🔥 High | Kubernetes |
| Cilium | Networking/security | 🟢 Production | 🔥 High | Kubernetes networking |
| Trivy | DevSecOps | 🟢 Production | 🔥 High | Containers |
| Semgrep | SAST | 🟢 Production | High | Programming basics |
| Gitleaks | Secrets security | 🟢 Production | High | Git |
| Checkov | IaC security | 🟢 Production | High | Terraform |
| Syft | SBOM | 🟢 Production | High | Containers |
| Grype | Vulnerability scanning | 🟢 Production | High | SBOM |
| Cosign / Sigstore | Artifact signing | 🟢 Production | High | Container registries |
| Backstage | Platform engineering | 🟢 Production | High | Kubernetes + CI/CD |
| Crossplane | Cloud/platform control | 🟡 Advanced | Medium-High | Kubernetes + IaC |
| Tetragon | Runtime security | 🟡 Advanced | Medium-High | Cilium + Kubernetes |
| Flux | GitOps | 🟢 Production | Medium | Argo CD |
| Istio | Service mesh | 🟡 Advanced | Medium | Kubernetes networking |
| Kubeflow | AI/ML infrastructure | 🟡 Specialized | Medium | Kubernetes |
| Firecracker | Secure workload isolation | 🟡 Advanced | Medium | Linux + containers |
| gVisor | Container isolation | 🟡 Advanced | Medium | Containers |
| Agentic cloud engineering | Emerging | 🧪 Emerging | Watch | Strong cloud fundamentals |

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
