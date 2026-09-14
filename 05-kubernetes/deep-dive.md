# Kubernetes Deep Dive

## 💡 What is Kubernetes?

Kubernetes is a declarative orchestration platform for managing containerized workloads. The important idea is reconciliation: you describe desired state and controllers work to move the cluster toward it.

## 🎯 Learning order

```text
Containers
   ↓
Pods
   ↓
Deployments + Services
   ↓
Networking
   ↓
Storage
   ↓
Scheduling
   ↓
Security
   ↓
Observability
   ↓
Troubleshooting
   ↓
Production architecture
```

## 🟢 Beginner

Understand:

- Pod
- Deployment
- ReplicaSet
- Service
- Namespace
- ConfigMap
- Secret
- labels and selectors

For every object explain its desired state and what controller or component acts on it.

## 🟡 Intermediate

- Ingress
- StatefulSet
- Jobs and CronJobs
- PV/PVC/StorageClass
- probes
- requests and limits
- scheduling
- taints and tolerations
- affinity
- Helm
- RBAC
- NetworkPolicy

## 🔴 Advanced

- API server
- etcd concepts
- controllers
- scheduler
- admission control
- CNI
- CSI
- cluster upgrades
- multi-cluster architecture
- runtime security

## 🛡️ Security model

```text
Identity
  ↓
RBAC
  ↓
Admission policy
  ↓
Pod security
  ↓
Network policy
  ↓
Image verification
  ↓
Secrets
  ↓
Runtime detection
```

Relevant technologies include Kyverno, OPA/Rego, Cilium and Tetragon. Learn the underlying security problem before learning the tool.

## 🚨 Troubleshooting method

When a workload fails:

1. establish the user-visible symptom
2. inspect workload state
3. inspect events
4. inspect logs
5. inspect service/endpoints
6. inspect DNS
7. inspect network policy
8. inspect node resources
9. inspect ingress/load balancer
10. inspect cluster components

Do not restart random things until the evidence tells you what is broken.

## 🛠️ Lab progression

### Lab A
Deploy a web application.

### Lab B
Expose it through a Service and Ingress.

### Lab C
Add readiness and liveness probes.

### Lab D
Apply resource requests and limits.

### Lab E
Restrict traffic with NetworkPolicy.

### Lab F
Apply an admission policy.

### Lab G
Break the application and document the troubleshooting path.

## ⚫ Interview questions

- Why is a Pod not the same thing as a container?
- How does a Deployment maintain replicas?
- How does service discovery work?
- What happens when a node fails?
- Why can a Pod be Running but not Ready?
- What causes Pending?
- How does the scheduler choose a node?
- How do RBAC and admission policies differ?
- How would you secure an EKS cluster?
