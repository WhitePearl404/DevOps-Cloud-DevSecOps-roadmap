# Docker vs Podman

## What problem are we solving?

You need a container workflow for local development, CI, image building and operational tooling.

## Core difference

- **Docker** provides a mature developer ecosystem centered around the Docker Engine, CLI and Docker Desktop.
- **Podman** provides a daemonless container engine with a Docker-compatible CLI and strong rootless-container support.

## Decision factors

| Factor | Docker | Podman |
|---|---|---|
| Developer ecosystem | Very broad | Strong and growing |
| CLI familiarity | Industry default | Docker-compatible in many workflows |
| Daemon model | Docker Engine daemon | Daemonless |
| Rootless workflows | Supported | Strong emphasis |
| Kubernetes direction | Docker Desktop integrates with Kubernetes tooling | Podman integrates with Kubernetes-oriented workflows |
| Enterprise standardization | Common | Common in some Linux/RHEL-oriented environments |

## Production decision

Choose based on the organization's runtime, developer tooling, security requirements and existing platform standards. Container images follow OCI standards, so the engine choice does not automatically determine the runtime platform.

## Security questions

- Are containers running rootless where practical?
- Who owns the image-building process?
- How are images scanned and signed?
- Where are credentials exposed during builds?
- Is the host runtime hardened?

## Interview question

**When would you choose Podman over Docker?**

A strong answer should discuss daemon architecture, rootless operation, ecosystem compatibility, enterprise Linux environments, developer experience and the actual operational constraints rather than claiming one tool is universally more secure.

## Related

- [Containers](../02-containers/README.md)
- [DevSecOps](../07-devsecops/README.md)
- [Supply Chain Security](../08-supply-chain-security/README.md)
