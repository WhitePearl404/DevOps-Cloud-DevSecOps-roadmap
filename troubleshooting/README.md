# Troubleshooting Playbooks

Troubleshooting is a reasoning skill, not a command collection.

## Universal method

```text
Observe
  ↓
Scope
  ↓
Collect evidence
  ↓
Form hypotheses
  ↓
Test one hypothesis
  ↓
Mitigate
  ↓
Verify
  ↓
Prevent recurrence
```

## Evidence hierarchy

Prefer evidence that directly observes the failure:

1. user impact and error rate
2. service/application logs
3. metrics and traces
4. platform events
5. network tests
6. configuration/state
7. recent changes

## Linux

- CPU saturation
- memory pressure
- disk/inode exhaustion
- process crashes
- systemd failures
- port conflicts
- permissions

## Networking

- DNS failure
- timeout vs connection refused
- routing failure
- TLS failure
- load-balancer health checks
- firewall/security-group behavior

## Kubernetes

- Pending
- CrashLoopBackOff
- ImagePullBackOff
- OOMKilled
- Service with no endpoints
- DNS failure
- Ingress 4xx/5xx
- NetworkPolicy denial
- Node NotReady

## CI/CD

- failed authentication
- flaky tests
- missing artifacts
- security gate failures
- deployment succeeded but application is unhealthy

## Terraform

- state lock
- drift
- provider failure
- dependency cycle
- unexpected replacement
- authorization failure

## AWS

- AccessDenied
- unreachable workload
- unhealthy load balancer
- private subnet egress failure
- database connectivity
- unexpected scaling

## Interview rule

Explain **why** you inspect each signal. A list of commands without reasoning is just autocomplete wearing a helmet.
