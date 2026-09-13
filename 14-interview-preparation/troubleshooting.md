# Troubleshooting Interview Guide

Use this sequence unless evidence points elsewhere:

**Observe → Scope → Hypothesize → Test → Mitigate → Verify → Prevent**

## Linux

- CPU saturation
- Memory pressure
- Disk full
- Process crash
- Service not starting
- Port unavailable
- Permission denied
- SSH failure

## Networking

- DNS failure
- TCP connection timeout
- Connection refused
- TLS certificate problems
- Routing failure
- Load balancer health-check failure

## Docker

- Image build failure
- Container exits immediately
- Port mapping issue
- Permission issue
- Image too large
- Registry authentication failure

## Kubernetes

- CrashLoopBackOff
- ImagePullBackOff
- Pending pod
- OOMKilled
- Service has no endpoints
- DNS failure
- Ingress returns 5xx
- NetworkPolicy blocks traffic
- Node NotReady

## CI/CD

- Pipeline timeout
- flaky tests
- authentication failure
- artifact unavailable
- security gate failure
- deployment succeeded but service unhealthy

## Terraform

- State lock
- Drift
- Provider failure
- Dependency cycle
- Unexpected replacement
- Permission denied

## AWS

- AccessDenied
- EC2 unreachable
- ALB unhealthy
- private subnet has no outbound connectivity
- application cannot reach RDS
- unexpected scaling behavior

## Interview requirement

Do not jump to a fix before collecting evidence. Explain the commands, telemetry or metrics you would inspect and why each observation changes your hypothesis.
