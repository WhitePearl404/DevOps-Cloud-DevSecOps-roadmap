# Kyverno vs OPA

## What problem are we solving?

You need policy enforcement for Kubernetes workloads and platform behavior.

## Core difference

- **Kyverno** is Kubernetes-native policy management using YAML-style rules and Kubernetes resources.
- **OPA** is a general-purpose policy engine using Rego and can enforce policy across multiple systems.

## Decision factors

| Factor | Kyverno | OPA |
|---|---|---|
| Kubernetes focus | Excellent | Strong, but broader |
| Policy language | YAML-oriented policy resources | Rego |
| General policy use | More Kubernetes-centric | Broad |
| Admission control | Native Kubernetes experience | Common through Gatekeeper |
| Learning curve | Often easier for Kubernetes teams | Requires learning Rego |
| Cross-platform policy | More limited | Strong |

## Production decision

Choose Kyverno when Kubernetes-native policy authoring and operations are the priority. Choose OPA when you need a broader policy-as-code model or already have Rego expertise and OPA-based controls.

## Security questions

- Are policies fail-open or fail-closed?
- Which resources are exempt and why?
- How are policy changes reviewed and tested?
- What happens when the policy engine is unavailable?
- Are audit and enforcement modes used appropriately?

## Interview question

**When would you choose Kyverno over OPA Gatekeeper?**

Explain Kubernetes-native policy authoring, Rego versus YAML-oriented rules, operational complexity, organizational expertise and whether policy must extend beyond Kubernetes.

## Related

- [Kubernetes](../05-kubernetes/README.md)
- [Cloud Security](../09-cloud-security/README.md)
- [DevSecOps](../07-devsecops/README.md)
