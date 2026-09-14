# 🚀 Start Here

New to DevOps, Cloud or DevSecOps? Start here instead of opening 40 tabs and learning Kubernetes before you understand networking. Humanity has suffered enough from that particular tradition.

## 🎯 Choose your starting point

| Your current level | Start here |
|---|---|
| 🟢 Complete beginner | [`00-foundations`](./00-foundations/) |
| 🟢 Know Linux basics | Networking → Git → DevOps fundamentals |
| 🟡 Know Docker | Cloud → IaC → Kubernetes |
| 🟡 Know AWS | Terraform → CI/CD → Kubernetes → GitOps |
| 🟠 Know Kubernetes | GitOps → DevSecOps → Cloud Security → Observability |
| 🔴 Working in DevOps | Production Engineering → Security → Platform Engineering |

## 🧭 The recommended learning order

```text
Linux + Networking + Git
          ↓
   DevOps Fundamentals
          ↓
       Docker
          ↓
        AWS
          ↓
 Terraform / OpenTofu
          ↓
    CI/CD + GitHub Actions
          ↓
     Kubernetes + Helm
          ↓
      GitOps + Argo CD
          ↓
 DevSecOps + Supply Chain
          ↓
     Cloud Security
          ↓
 Observability + Reliability
          ↓
 Platform / Production Engineering
          ↓
 Advanced Cloud-Native
```

Do not treat this as a rigid checklist. It is a dependency-aware order. Move faster through topics you already understand and spend more time where your fundamentals are weak.

## ⏱️ Pick a time horizon

### 3-month foundation path

Focus on employable fundamentals:

1. Linux
2. Networking
3. Git
4. Bash/Python basics
5. DevOps fundamentals
6. Docker
7. AWS fundamentals
8. Terraform
9. GitHub Actions
10. One complete deployment project

**Goal:** understand how code becomes a running application in the cloud.

### 6-month engineering path

Complete the 3-month path, then add:

1. Kubernetes
2. Helm
3. GitOps
4. Observability
5. DevSecOps fundamentals
6. AWS security
7. Two production-style projects
8. Troubleshooting and interview preparation

**Goal:** build, deploy, secure and troubleshoot cloud-native workloads.

### 12-month professional path

Complete the 6-month path, then add:

1. Supply-chain security
2. Advanced Kubernetes security
3. SLOs and production engineering
4. Platform engineering
5. Runtime security
6. Multi-cluster concepts
7. Advanced cloud architecture
8. Incident response
9. Senior-level architecture interviews

**Goal:** reason about production systems, trade-offs, security and failure recovery.

## 🧠 Learn → Use → Master

Not every technology deserves the same depth.

### 🟢 Learn
Understand the purpose, architecture, core concepts and common commands.

Examples: YAML, Git basics, Docker fundamentals.

### 🔵 Use
Build something real and troubleshoot common failures.

Examples: Terraform modules, GitHub Actions, Kubernetes workloads, Helm.

### 🟣 Master
Understand internals, production trade-offs, failure modes, security and architecture decisions.

Examples: Kubernetes networking, AWS IAM design, Terraform state, CI/CD security, production observability.

### ⚪ Awareness
Know what the technology does and when it may be useful. Do not spend weeks mastering it yet.

Examples: service meshes, Crossplane, Kubeflow, advanced eBPF internals when you are still learning Kubernetes fundamentals.

## 🧑‍💻 Choose a career direction

Once you understand the core path, specialize:

| Role | Primary focus |
|---|---|
| [Cloud Engineer](./career-paths/cloud-engineer.md) | AWS, networking, IAM, infrastructure, automation |
| [DevOps Engineer](./career-paths/devops-engineer.md) | CI/CD, IaC, containers, cloud, reliability |
| [DevSecOps Engineer](./career-paths/devsecops-engineer.md) | Secure CI/CD, IaC security, containers, supply chain |
| [Cloud Security Engineer](./career-paths/cloud-security-engineer.md) | AWS security, IAM, detection, Kubernetes security |
| [SRE](./career-paths/sre.md) | Reliability, observability, SLOs, incident response |
| [Platform Engineer](./career-paths/platform-engineer.md) | Developer platforms, golden paths, automation, governance |

You do not need to specialize immediately. Build the common foundation first.

## 🧪 How to study each topic

For every important technology:

```text
Understand the problem
        ↓
Learn the architecture
        ↓
Build a small example
        ↓
Secure it
        ↓
Break it intentionally
        ↓
Troubleshoot from evidence
        ↓
Fix and verify
        ↓
Explain the trade-offs
```

Use the repository's [labs](./labs/), [troubleshooting](./troubleshooting/), [decision guides](./decision-guides/) and [interview preparation](./14-interview-preparation/) to turn theory into engineering practice.

## 🚫 What not to learn first

If you are a beginner, do **not** start with:

- Service mesh internals
- Multi-cluster Kubernetes
- Advanced eBPF internals
- Crossplane
- Kubeflow
- Complex platform engineering stacks
- Highly specialized runtime-security tooling

First become comfortable with Linux, networking, Git, containers, AWS, Terraform, CI/CD and Kubernetes fundamentals.

## 🏁 Your first project

Build one small project all the way through instead of starting ten unfinished projects.

Recommended sequence:

```text
Application
  ↓
Docker
  ↓
GitHub Actions
  ↓
AWS
  ↓
Terraform
  ↓
Security scanning
  ↓
Deployment
  ↓
Monitoring
  ↓
Failure drill
  ↓
Documentation
```

Then move to the [project ladder](./13-projects/).

## 📚 Main repository map

- [Foundations](./00-foundations/)
- [DevOps Fundamentals](./01-devops-fundamentals/)
- [Containers](./02-containers/)
- [Cloud](./03-cloud/)
- [Infrastructure as Code](./04-infrastructure-as-code/)
- [Kubernetes](./05-kubernetes/)
- [GitOps](./06-gitops/)
- [DevSecOps](./07-devsecops/)
- [Supply Chain Security](./08-supply-chain-security/)
- [Cloud Security](./09-cloud-security/)
- [Observability](./10-observability/)
- [Platform Engineering](./11-platform-engineering/)
- [Production Engineering](./15-production-engineering/)
- [Advanced Cloud-Native](./12-advanced-cloud-native/)
- [Projects](./13-projects/)
- [Interview Preparation](./14-interview-preparation/)

## ✅ Progress rule

Do not measure progress by how many tools you have installed.

Measure it by whether you can:

- explain the architecture,
- build the system,
- secure it,
- break it,
- troubleshoot it,
- recover it,
- explain your design decisions.

That is the difference between **knowing a tool exists** and **being able to engineer with it**.
