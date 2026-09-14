# Amazon EKS vs Amazon ECS

## 💡 Problem

You need to run containers on AWS. The choice is between a Kubernetes-based control model and an AWS-native container orchestration model.

## 🟢 ECS is attractive when

- the workload is primarily AWS-focused
- the team does not need the Kubernetes API
- operational simplicity is a priority
- AWS-native integrations cover the requirements

## 🟡 EKS is attractive when

- Kubernetes portability matters
- the organization already operates Kubernetes
- Kubernetes ecosystem tooling is required
- advanced scheduling, operators, policy or multi-cluster patterns matter

## 🔴 Decision factors

| Factor | ECS | EKS |
|---|---|---|
| Platform complexity | Lower | Higher |
| Kubernetes ecosystem | No | Yes |
| AWS-native integration | Strong | Strong |
| Portability | Lower | Higher |
| Team skill requirement | AWS/container focused | Kubernetes + AWS |
| Control-plane operations | AWS managed | AWS managed, but more platform responsibility |

## 🛡️ Security

For either platform evaluate:

- workload IAM
- network segmentation
- image provenance
- secrets
- logging
- runtime detection
- patching
- least privilege

## ⚫ Interview question

Do not answer “EKS is more advanced.” Explain whether Kubernetes capabilities justify the additional platform complexity for the workload and team.
