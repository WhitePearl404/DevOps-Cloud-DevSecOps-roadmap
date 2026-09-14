# Helm vs Kustomize

## What problem are we solving?

You need a maintainable way to generate or customize Kubernetes manifests across environments.

## Core difference

- **Helm** packages Kubernetes resources into charts with templates, values and release management.
- **Kustomize** customizes ordinary Kubernetes YAML using overlays and patches without requiring a separate templating language.

## Decision factors

| Factor | Helm | Kustomize |
|---|---|---|
| Packaging | Strong | Minimal |
| Templating | Native | Intentionally limited |
| Reuse | Charts and values | Bases and overlays |
| Dependency management | Strong | Simpler composition |
| Application distribution | Excellent | Less package-oriented |
| GitOps workflows | Widely used | Widely used |

## Production decision

Use Helm when you need reusable application packages, configurable releases or dependency management. Use Kustomize when you want Kubernetes-native YAML with environment-specific overlays and minimal abstraction. They can also be combined.

## Security questions

- Can generated manifests be reviewed before deployment?
- Are secrets kept out of Git and template values?
- Are chart dependencies trusted and version-pinned?
- Are rendered manifests scanned for insecure configuration?

## Interview question

**Why might a team choose Kustomize instead of Helm?**

Discuss abstraction level, YAML ownership, overlays, packaging requirements, maintainability and GitOps reviewability. Avoid the childish answer that one tool is simply "better."

## Related

- [Kubernetes](../05-kubernetes/README.md)
- [GitOps](../06-gitops/README.md)
- [DevSecOps](../07-devsecops/README.md)
