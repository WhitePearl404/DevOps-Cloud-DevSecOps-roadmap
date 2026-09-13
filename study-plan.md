# Study Plan

A progressive plan for a college student or beginner. Move forward when you can **explain, build, break, and fix** the current topic.

## Phase 0 — Foundations

**Goal:** become comfortable with the systems DevOps operates.

- 🟢 Linux filesystem, processes, users, permissions, SSH, services, logs
- 🟢 Networking: IP, CIDR, DNS, TCP/UDP, HTTP/HTTPS, TLS, ports, routing
- 🟢 Git: commits, branches, merge/rebase, tags, remotes, pull requests
- 🟢 Bash fundamentals
- 🟢 Python fundamentals for automation
- 🟢 YAML and JSON

**Exit test:** deploy a small application to a Linux server and explain every network hop.

## Phase 1 — DevOps fundamentals

- DevOps culture and feedback loops
- SDLC and release strategies
- CI vs CD vs continuous deployment
- Artifact management
- Build automation
- Git workflows
- Environment management
- Configuration management

**Hands-on:** create a CI pipeline that tests and packages an application.

## Phase 2 — Containers

- Container vs VM
- Docker architecture
- Dockerfile
- Layers and caching
- Volumes and networks
- Multi-stage builds
- Image registries
- Image tagging
- Container resource limits
- Container security

**Hands-on:** containerize an application, scan the image, publish it to a registry.

## Phase 3 — Cloud

Start with AWS, then map concepts to Azure and GCP.

### AWS core
- IAM
- VPC, subnets, route tables, security groups
- EC2
- Load balancing
- Auto Scaling
- S3
- RDS
- CloudFront
- Route 53
- CloudWatch
- KMS
- Secrets Manager

### Architecture
- High availability
- Fault tolerance
- Scalability
- Disaster recovery
- Cost awareness
- Shared responsibility model

**Hands-on:** build a secure multi-tier AWS environment.

## Phase 4 — Infrastructure as Code

- Terraform fundamentals
- Providers, resources, variables, outputs
- State and locking
- Modules
- Workspaces and environment design
- Remote state
- Drift
- Import and lifecycle management
- Testing and validation
- OpenTofu concepts
- Ansible configuration management
- Policy-as-code

**Hands-on:** provision cloud infrastructure from code and review it through CI.

## Phase 5 — Kubernetes

### Beginner
- Cluster architecture
- Pods
- Deployments
- ReplicaSets
- Services
- Namespaces
- ConfigMaps
- Secrets

### Intermediate
- Ingress
- Storage
- StatefulSets
- Jobs/CronJobs
- Probes
- Resource requests/limits
- Scheduling
- RBAC
- NetworkPolicy
- Helm

### Advanced
- Cluster upgrades
- Multi-cluster architecture
- Network plugins
- CNI internals
- Admission control
- Pod Security Standards
- Policy-as-code
- Runtime security
- Production troubleshooting

**Hands-on:** deploy and secure an application on Kubernetes/EKS.

## Phase 6 — CI/CD + GitOps

- GitHub Actions
- Jenkins concepts
- Pipeline design
- Secrets management
- Build/test/package/deploy stages
- Argo CD
- Flux
- GitOps principles
- Progressive delivery
- Canary and blue/green deployments

**Hands-on:** GitHub → CI → image registry → GitOps → Kubernetes.

## Phase 7 — DevSecOps

Learn security throughout the lifecycle:

```text
Code
 ↓
SAST → SCA → Secrets Scan
 ↓
IaC Security
 ↓
Container Scan
 ↓
SBOM
 ↓
Artifact Signing + Provenance
 ↓
Deployment Policy
 ↓
Runtime Detection
```

Tools to study:
- Semgrep
- Trivy
- Gitleaks
- Checkov
- tfsec concepts
- Syft
- Grype
- Cosign
- Sigstore
- Kyverno
- OPA/Rego

## Phase 8 — Cloud Security

### AWS security
- IAM least privilege
- IAM Access Analyzer
- Security Hub
- GuardDuty
- Inspector
- Macie
- AWS Config
- CloudTrail
- Security Lake
- KMS
- Secrets Manager
- Organizations and SCPs
- EventBridge
- Lambda-based response

### Kubernetes security
- RBAC
- Pod Security Standards
- NetworkPolicy
- Security Groups for Pods
- Kyverno
- OPA/Rego
- Cilium
- Tetragon

## Phase 9 — Observability

- Metrics
- Logs
- Traces
- SLI/SLO/SLA
- Alerting
- Prometheus
- Grafana
- OpenTelemetry
- Centralized logging
- Distributed tracing

**Hands-on:** instrument an application and investigate a deliberately injected failure.

## Phase 10 — Platform Engineering

- Internal Developer Platforms
- Developer experience
- Golden paths
- Self-service infrastructure
- Backstage
- Terraform/OpenTofu
- Crossplane concepts
- GitOps
- Policy and governance
- Platform security

## Phase 11 — Advanced cloud-native

Explore after the core stack is strong:

- Cilium
- Tetragon
- Service mesh
- Istio
- Multi-cluster Kubernetes
- Chaos engineering
- Confidential computing
- Firecracker/gVisor
- AI/ML infrastructure
- AI-assisted operations
- Agentic cloud engineering and secure agent runtimes

## 16-week example schedule

| Weeks | Focus | Output |
|---|---|---|
| 1–2 | Linux + networking | Linux lab + network notes |
| 3 | Git + scripting | automation scripts |
| 4 | DevOps + CI/CD | working CI pipeline |
| 5 | Docker | secure container image |
| 6–7 | AWS | multi-tier architecture |
| 8 | Terraform | infrastructure repository |
| 9–10 | Kubernetes | application deployment |
| 11 | Helm + GitOps | Argo CD deployment |
| 12 | DevSecOps | security pipeline |
| 13 | Cloud security | AWS security controls |
| 14 | Observability | metrics/logs/traces |
| 15 | Platform engineering | golden-path prototype |
| 16 | Projects + interviews | architecture + interview notebook |

## The rule

Do not measure progress by the number of tools installed.

Measure it by whether you can:

**Explain it → Build it → Secure it → Break it → Fix it → Defend the design.**
