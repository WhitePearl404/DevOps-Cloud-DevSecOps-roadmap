# Scenario-Based Interview Guide

Scenario questions test engineering judgment more than memorized definitions.

## Architecture

1. Design a highly available AWS application.
2. Design a secure EKS platform.
3. Design CI/CD for multiple environments.
4. Design a zero-trust cloud architecture.
5. Design a centralized cloud-security monitoring system.
6. Design a multi-cluster Kubernetes platform.
7. Design an internal developer platform.

## Production incidents

8. Production latency increases suddenly.
9. Error rate increases after a deployment.
10. Kubernetes nodes become NotReady.
11. A critical container vulnerability is discovered before release.
12. AWS credentials appear compromised.
13. Terraform state is locked during an incident.
14. Argo CD reports unexpected drift.
15. CI starts exposing sensitive values in logs.

## Answer framework

For every scenario, structure the response:

```text
1. Clarify the impact
2. Establish scope
3. Collect evidence
4. Form hypotheses
5. Test hypotheses
6. Mitigate immediate impact
7. Restore service securely
8. Validate recovery
9. Find root cause
10. Add preventive controls
11. Document lessons learned
```

## Senior-level follow-ups

Expect questions about:

- blast radius
- failure domains
- trade-offs
- security implications
- observability
- automation
- rollback
- cost
- operational ownership
- long-term prevention
