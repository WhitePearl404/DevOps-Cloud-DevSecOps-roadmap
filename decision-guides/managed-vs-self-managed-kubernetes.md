# Managed vs Self-Managed Kubernetes

## What problem are we solving?

You need Kubernetes while deciding how much of the control plane and underlying infrastructure your team should operate.

## Core difference

- **Managed Kubernetes** delegates significant control-plane operations to a cloud provider or managed platform.
- **Self-managed Kubernetes** requires the organization to own substantially more of cluster lifecycle, upgrades, control-plane reliability and supporting infrastructure.

## Decision factors

| Factor | Managed | Self-managed |
|---|---|---|
| Control-plane operations | Provider-managed | Team-managed |
| Operational burden | Lower | Higher |
| Customization | Provider constraints apply | Greater control |
| Upgrades | Provider-supported workflow | Team responsibility |
| Reliability responsibility | Shared with provider | Primarily team-owned |
| Cost model | Service + infrastructure costs | Infrastructure + engineering cost |

## Production decision

For most organizations, managed Kubernetes is the sensible default unless there is a concrete requirement for deeper infrastructure control, unusual networking, specialized environments or a platform capability that the managed service cannot provide.

## Security questions

- Who patches the control plane and nodes?
- Who owns IAM integration and cluster access?
- How are audit logs collected?
- Which responsibilities remain with the customer under the provider's shared-responsibility model?
- How are upgrades and emergency recovery tested?

## Interview question

**Why would a company choose managed Kubernetes?**

Discuss reduced control-plane operations, provider integrations, reliability, upgrade workflows, shared responsibility, cost and the remaining operational responsibilities such as nodes, workloads, RBAC, networking and application security.

## Related

- [Kubernetes](../05-kubernetes/README.md)
- [AWS](../03-cloud/aws/README.md)
- [Production Engineering](../15-production-engineering/README.md)
