# VMs vs Containers

## What problem are we solving?

You need to isolate workloads while balancing security, startup time, density, portability and operational complexity.

## Core difference

- **Virtual machines** isolate workloads with separate guest operating systems through a hypervisor.
- **Containers** isolate processes while sharing the host kernel.

## Decision factors

| Factor | VMs | Containers |
|---|---|---|
| Isolation boundary | Stronger OS-level boundary | Shared host kernel |
| Startup | Usually slower | Usually faster |
| Density | Lower | Higher |
| OS flexibility | Full guest OS | Host-kernel dependent |
| Operational model | VM lifecycle | Image and workload lifecycle |
| Common use | Strong isolation, legacy workloads | Microservices, CI/CD, cloud-native apps |

## Production decision

Containers are not automatically a replacement for VMs. Many production platforms use both: VMs provide infrastructure isolation while containers provide application packaging and process isolation.

## Security questions

- What isolation boundary does the workload require?
- Is the container runtime hardened?
- Are containers privileged unnecessarily?
- Are host and container vulnerabilities patched?
- Would a stronger boundary such as a VM or sandboxed runtime be appropriate?

## Interview question

**Why are containers generally lighter than VMs?**

Explain the shared-kernel model, image layers, process isolation and the trade-off between density and isolation. Do not claim that containers provide the same isolation boundary as a full VM.

## Related

- [Containers](../02-containers/README.md)
- [Kubernetes](../05-kubernetes/README.md)
- [Advanced Cloud Native](../12-advanced-cloud-native/README.md)
