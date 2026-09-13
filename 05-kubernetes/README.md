# 05 — Kubernetes

Kubernetes is a major production platform skill. Learn the objects first, then networking, scheduling, security, and troubleshooting.

## 🟢 Beginner

- Cluster architecture
- Control plane and worker nodes
- Pods
- Deployments
- ReplicaSets
- Services
- Namespaces
- Labels/selectors
- ConfigMaps
- Secrets

## 🟡 Intermediate

- Ingress
- StatefulSets
- Jobs/CronJobs
- PersistentVolumes/PVCs
- StorageClasses
- Readiness/liveness/startup probes
- Requests and limits
- Scheduling
- Taints/tolerations
- Affinity/anti-affinity
- Helm
- RBAC
- NetworkPolicy

## 🔴 Advanced

- API server and controllers
- Scheduler internals
- CNI
- CSI
- Admission control
- Pod Security Standards
- Policy engines
- Cluster upgrades
- Multi-cluster architecture
- Runtime security
- Production troubleshooting

## 🟣 Security

- RBAC and least privilege
- NetworkPolicy
- Pod Security Standards
- Security Groups for Pods
- Kyverno
- OPA/Rego
- Cilium
- Tetragon
- Secrets management
- Image verification

## 🚨 Troubleshooting flow

```text
Application problem
 ↓
Pod status/events
 ↓
Logs
 ↓
Service/endpoints
 ↓
DNS
 ↓
Network policy
 ↓
Ingress/load balancer
 ↓
Node/resources
 ↓
Cluster/control plane
```

## ⚫ Interview focus

- Pod vs Deployment
- Service types
- ClusterIP vs NodePort vs LoadBalancer
- ConfigMap vs Secret
- Requests vs limits
- Liveness vs readiness
- StatefulSet vs Deployment
- Ingress architecture
- RBAC design
- NetworkPolicy behavior
- What happens when a pod is OOMKilled?
- How do you troubleshoot CrashLoopBackOff?
- How does Kubernetes scheduling work?
