# DevOps • Cloud • DevSecOps Roadmap

A beginner-friendly, production-oriented learning path for **DevOps, Cloud, Kubernetes, DevSecOps, Cloud Security, GitOps, Observability, Platform Engineering, and production engineering**.

> **Learn → Understand → Implement → Break → Secure → Operate → Explain**

This repository is designed for college students, freshers, career switchers, and engineers who want a structured path from fundamentals to advanced cloud-native engineering.

## 🎯 What this repository covers

| Level | Focus |
|---|---|
| 🟢 Beginner | Linux, networking, Git, scripting, YAML/JSON, DevOps fundamentals |
| 🟡 Intermediate | Docker, CI/CD, AWS, Terraform/OpenTofu, Kubernetes, Helm |
| 🔴 Advanced | GitOps, DevSecOps, cloud security, supply-chain security, observability |
| 🟣 Professional | Platform engineering, policy-as-code, runtime security, multi-cluster, production engineering |
| ⚫ Interview | Concepts, architecture, troubleshooting, scenarios, trade-offs and follow-ups |

## 🗺️ Learning path

```text
FOUNDATIONS
   ↓
DEVOPS FUNDAMENTALS
   ↓
CONTAINERS
   ↓
CLOUD
   ↓
INFRASTRUCTURE AS CODE
   ↓
KUBERNETES
   ↓
CI/CD + GITOPS
   ↓
DEVSECOPS + SUPPLY CHAIN SECURITY
   ↓
CLOUD SECURITY
   ↓
OBSERVABILITY
   ↓
PLATFORM ENGINEERING
   ↓
PRODUCTION ENGINEERING
   ↓
ADVANCED CLOUD-NATIVE
   ↓
LABS + PROJECTS + INTERVIEWS
```

## 📚 Repository map

| Directory | What you learn |
|---|---|
| [`00-foundations`](./00-foundations/) | Linux, networking, Git, scripting, YAML/JSON |
| [`01-devops-fundamentals`](./01-devops-fundamentals/) | DevOps, CI/CD, automation, artifacts |
| [`02-containers`](./02-containers/) | Docker, images, registries, container security |
| [`03-cloud`](./03-cloud/) | AWS first, plus Azure/GCP concepts |
| [`04-infrastructure-as-code`](./04-infrastructure-as-code/) | Terraform, OpenTofu, Ansible, policy-as-code |
| [`05-kubernetes`](./05-kubernetes/) | Kubernetes from fundamentals to production |
| [`06-gitops`](./06-gitops/) | Argo CD, Flux, progressive delivery |
| [`07-devsecops`](./07-devsecops/) | SAST, SCA, secrets, IaC, container and DAST security |
| [`08-supply-chain-security`](./08-supply-chain-security/) | SBOM, signing, provenance, verification |
| [`09-cloud-security`](./09-cloud-security/) | AWS security, Kubernetes security, Zero Trust, response |
| [`10-observability`](./10-observability/) | Metrics, logs, traces, OpenTelemetry |
| [`11-platform-engineering`](./11-platform-engineering/) | IDPs, Backstage, golden paths, platform security |
| [`12-advanced-cloud-native`](./12-advanced-cloud-native/) | Cilium, service mesh, multi-cluster, chaos, AI infrastructure |
| [`13-projects`](./13-projects/) | Hands-on projects from beginner to advanced |
| [`14-interview-preparation`](./14-interview-preparation/) | Technical + scenario + troubleshooting interviews |
| [`15-production-engineering`](./15-production-engineering/) | Reliability, SLOs, DR, incident response, production readiness |
| [`labs`](./labs/) | Build, break, troubleshoot and secure real systems |
| [`decision-guides`](./decision-guides/) | Technology choices and engineering trade-offs |
| [`troubleshooting`](./troubleshooting/) | Evidence-driven troubleshooting playbooks |
| [`glossary`](./glossary/) | Common DevOps, Cloud and security terminology |
| [`resources`](./resources/) | Official docs, labs, books, courses and communities |

## 🧠 How to learn a technology

Do not start by memorizing commands.

For every major technology answer:

1. 💡 What problem does it solve?
2. 🎯 Why does that problem matter?
3. 🧠 What are the core concepts?
4. 🔵 What is the architecture and request/data flow?
5. 🟢 What should a beginner know?
6. 🟡 What changes at production scale?
7. 🔴 What are the advanced capabilities?
8. 🟣 How can it fail or be abused?
9. 🛡️ How is it secured?
10. 🛠️ Can I build it?
11. 💥 Can I intentionally break it?
12. 🚨 Can I troubleshoot it from evidence?
13. ⚖️ What are the alternatives and trade-offs?
14. ⚫ Can I explain the design in an interview?

This is the central philosophy of the repository.

## 🔥 Technology philosophy

“Latest” does **not** mean collecting every tool released last Tuesday. This roadmap separates technologies into:

- 🟢 **Core / Production:** broad industry relevance
- 🔵 **Modern / High-growth:** increasingly important in cloud-native environments
- 🟣 **Advanced / Specialized:** valuable after fundamentals are solid
- 🧪 **Emerging:** worth tracking and experimenting with

See [`technology-matrix.md`](./technology-matrix.md).

## 🏗️ How everything fits together

```mermaid
flowchart LR
    Dev[Developer] --> Git[Git / GitHub]
    Git --> CI[CI Pipeline]
    CI --> Sec[Security Gates]
    Sec --> Build[Build + Test]
    Build --> SBOM[SBOM + Sign + Provenance]
    SBOM --> Registry[Container Registry]
    Registry --> GitOps[GitOps]
    GitOps --> K8s[Kubernetes / EKS]
    Infra[Terraform / OpenTofu] --> Cloud[AWS / Azure / GCP]
    Cloud --> K8s
    K8s --> Obs[OpenTelemetry / Prometheus / Grafana]
    K8s --> Runtime[Runtime Security]
    Cloud --> CloudSec[Cloud Security]
    Runtime --> SIEM[Detection + Response]
    CloudSec --> SIEM
```

## 🧪 Learn by breaking things

The repository deliberately treats failure as part of learning.

```text
Build
  ↓
Verify
  ↓
Break intentionally
  ↓
Observe evidence
  ↓
Form a hypothesis
  ↓
Fix
  ↓
Verify recovery
  ↓
Add prevention
```

See [`labs/`](./labs/) and [`troubleshooting/`](./troubleshooting/).

## ⚖️ Learn to choose, not just use

Senior engineering requires explaining why one design is preferable under specific constraints.

See [`decision-guides/`](./decision-guides/) for comparisons such as Terraform vs OpenTofu, EKS vs ECS and Argo CD vs Flux.

## 🧪 Project ladder

### 🟢 Beginner
- Linux server deployment
- Git branching workflow
- Dockerize a Flask application
- GitHub Actions CI
- Static website deployment
- AWS EC2 deployment
- Terraform VPC

### 🟡 Intermediate
- Three-tier AWS architecture
- Docker + CI/CD
- Kubernetes application deployment
- Terraform + AWS
- Argo CD GitOps
- Prometheus + Grafana
- Kubernetes security policies

### 🔴 Advanced
- Production-style AWS EKS platform
- Secure DevSecOps supply chain
- Cloud-native security platform
- Internal Developer Platform
- Multi-cluster platform with observability and security

### ⚫ Production challenge

For every serious project, answer:

**Architecture → security → failure modes → observability → cost → deployment safety → recovery → trade-offs.**

## 📈 Suggested weekly study cycle

```text
Day 1 → Learn the concept
Day 2 → Read official documentation
Day 3 → Build a small lab
Day 4 → Break it intentionally
Day 5 → Troubleshoot and document
Day 6 → Build an interview explanation
Day 7 → Review + teach the concept
```

## 🤝 Contribution

This is intended to remain a living learning resource. Corrections, examples, labs, diagrams, interview questions, and updated technology references are welcome.

See [`CONTRIBUTING.md`](./CONTRIBUTING.md).

## 📜 License

Educational content is provided under the MIT License. Individual third-party trademarks and technologies remain the property of their respective owners.
