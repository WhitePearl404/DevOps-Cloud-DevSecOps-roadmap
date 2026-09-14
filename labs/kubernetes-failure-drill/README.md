# Lab 02 — Kubernetes Failure Drill

## 🎯 Objective

Learn to troubleshoot a Kubernetes application using evidence rather than random restarts. The goal is to understand Kubernetes state, dependency failures, networking and resource behavior.

## Prerequisites

- Basic Kubernetes concepts
- `kubectl`
- Access to a disposable Kubernetes cluster
- Basic container and networking knowledge

## Starting architecture

```text
Client
  ↓
Ingress
  ↓
Service
  ↓
Deployment
  ↓
Pods
```

## 🟢 Baseline

Deploy a simple HTTP application with:

- Deployment
- Service
- readiness probe
- liveness probe
- resource requests/limits

Verify:

- Pod is Ready
- Service has endpoints
- application responds
- requested resources are visible

Record the healthy state before introducing failures.

## Failure investigation standard

For every failure, use:

```text
Symptom
→ Scope / blast radius
→ Evidence
→ Hypothesis
→ Test
→ Mitigation
→ Verification
→ Preventive control
```

Useful evidence includes Pod status, events, logs, Service endpoints, Deployment state, node conditions, resource metrics and network-policy configuration.

## 💥 Failure 1 — Bad image

Change the image reference to a nonexistent tag.

Expected investigation:

```text
Pod status
 ↓
Events
 ↓
ImagePullBackOff
 ↓
Image reference / registry / credentials
```

Do not fix the image until you can explain why the cluster cannot obtain it.

## 💥 Failure 2 — Readiness failure

Break the readiness endpoint.

Determine:

- why the Pod can remain Running
- why the Service stops sending it traffic
- which condition controls readiness
- how you would verify recovery

## 💥 Failure 3 — Resource pressure

Set an intentionally inappropriate memory limit and observe the resulting behavior.

Explain:

- OOMKilled
- container limit vs node capacity
- application failure vs node-level memory pressure
- which metrics or events would distinguish them

## 💥 Failure 4 — NetworkPolicy

Apply a restrictive policy and break application connectivity.

Determine:

- source identity
- destination identity
- port
- namespace
- ingress/egress direction
- whether the policy selects the expected Pods

## 🔐 Security extension

After restoring connectivity, harden the workload:

- run as non-root where practical
- use least-privilege ServiceAccount permissions
- define resource requests/limits
- restrict network traffic to required paths
- avoid plaintext secrets in manifests

Explain which control reduces which risk.

## 🧠 Deliverable

For every failure write:

1. symptom
2. scope
3. evidence
4. hypothesis
5. test
6. mitigation
7. verification
8. preventive control

A good write-up should make it possible for another engineer to reproduce the failure and follow your reasoning.

## 💰 Operational considerations

Record cluster/resource costs if using a managed or cloud-hosted cluster. Prefer a disposable environment and clean it up after the drill.

## ⚫ Interview challenge

Your interviewer says: “The pod is Running. Why is the application down?”

Do not answer with another command. Explain the Kubernetes state model and the signals you would inspect, then describe how you would narrow the failure domain.

## Extension challenge

Introduce a second failure while the first is present. Determine whether the symptoms are independent or causally related, and document how you distinguish correlation from root cause.