# Decision Guides

Engineering is mostly choosing between imperfect options while pretending the requirements were clear. These guides make the reasoning explicit.

## How to use a decision guide

For each comparison, answer:

1. What problem are we solving?
2. What constraints matter?
3. What are the viable options?
4. What are the operational costs?
5. What are the security implications?
6. What happens when the choice fails?
7. When should we *not* use the technology?

## Core comparisons

| Guide | Main decision |
|---|---|
| [Terraform vs OpenTofu](./terraform-vs-opentofu.md) | IaC ecosystem choice |
| [EKS vs ECS](./eks-vs-ecs.md) | AWS container platform |
| [Docker vs Podman](./docker-vs-podman.md) | Container tooling |
| [Argo CD vs Flux](./argocd-vs-flux.md) | GitOps controller |
| [Helm vs Kustomize](./helm-vs-kustomize.md) | Kubernetes configuration |
| [Kyverno vs OPA](./kyverno-vs-opa.md) | Kubernetes policy |
| [VMs vs containers](./vm-vs-container.md) | Workload isolation |
| [Managed vs self-managed Kubernetes](./managed-vs-self-managed-kubernetes.md) | Operational ownership |

## Rule

Never select a tool because it appears in a job description. Select it because you can explain the problem it solves, its trade-offs, its failure modes and its operational model.
