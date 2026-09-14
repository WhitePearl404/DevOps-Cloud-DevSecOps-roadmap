# Kubernetes Interview Questions

Use the [Interview Answer Framework](./answer-framework.md). For Kubernetes, be especially precise about **desired state, observed state, controllers, networking, scheduling, security and evidence**.

## Fundamentals

1. What is Kubernetes?
2. What is a Pod?
3. Pod vs Deployment?
4. ReplicaSet vs Deployment?
5. What is a Service?
6. ClusterIP vs NodePort vs LoadBalancer?
7. ConfigMap vs Secret?
8. What is a Namespace?
9. What are labels and selectors?
10. What happens when a container exits?

## Networking

11. How does Kubernetes service discovery work?
12. What is a CNI?
13. What is NetworkPolicy?
14. How does Ingress work?
15. How does traffic reach a pod from outside the cluster?

## Scheduling and resources

16. Requests vs limits?
17. What causes OOMKilled?
18. What are taints and tolerations?
19. What is affinity/anti-affinity?
20. How does the scheduler select a node?

## Security

21. What is RBAC?
22. How do you implement least privilege in Kubernetes?
23. What are Pod Security Standards?
24. How do you secure Kubernetes secrets?
25. How do you restrict pod-to-pod traffic?
26. What is admission control?
27. Kyverno vs OPA/Rego?
28. What does Cilium provide?
29. What is runtime security?

## Troubleshooting

30. How do you troubleshoot CrashLoopBackOff?
31. How do you troubleshoot Pending pods?
32. How do you troubleshoot ImagePullBackOff?
33. A Service has no traffic. What do you check?
34. Pods can reach IPs but not DNS names. What do you check?
35. A pod is healthy but the application is unavailable externally. How do you investigate?

## High-value answer anchors

### 1. Pod is Running but the application is unavailable

Do not equate **Running** with **Ready** or **reachable**.

Check the request path:

```text
Pod process
→ Readiness
→ Service selector/endpoints
→ NetworkPolicy
→ Ingress / LoadBalancer
→ External client
```

Gather evidence at each boundary and identify the first layer where expected behavior stops.

### 2. CrashLoopBackOff

Use:

```text
Current state
→ Previous container state / exit code
→ Events
→ Current and previous logs
→ Configuration / secrets
→ Dependencies
→ Recent changes
```

Explain whether the process is crashing, being killed, failing its probes, or repeatedly starting with invalid configuration.

### 3. Pod stuck Pending

Investigate:

- scheduler events
- resource requests vs node capacity
- taints/tolerations
- affinity/anti-affinity
- node selectors
- topology constraints
- PVC availability where relevant

State the scheduling constraint before proposing a change.

### 4. Service receives no traffic

Check:

```text
Service selector
→ EndpointSlice / endpoints
→ Pod labels
→ Pod readiness
→ NetworkPolicy
→ Service port / targetPort
→ Ingress or external load balancer
```

The key is to distinguish a discovery problem from an application problem.

### 5. Secure an EKS workload

Cover:

- IAM and workload identity
- RBAC
- Pod Security Standards
- NetworkPolicy
- secrets handling
- image provenance and vulnerability controls
- admission policy
- runtime detection where justified
- audit logging
- least privilege

Then explain which control protects which boundary.

## Senior follow-ups

For architecture and troubleshooting questions, expect:

- What is the failure domain?
- What evidence proves your hypothesis?
- What is the blast radius?
- How would you mitigate without causing more disruption?
- How would you prevent recurrence?
- What changes at 10x workload scale?
- What is the operational cost of your design?
