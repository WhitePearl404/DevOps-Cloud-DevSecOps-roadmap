# Lab 02 — Kubernetes Failure Drill

## 🎯 Objective

Learn to troubleshoot a Kubernetes application using evidence rather than random restarts.

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

## 🛠️ Baseline

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

## 💥 Failure 2 — Readiness failure

Break the readiness endpoint.

Question: why can the Pod be Running while the Service sends it no traffic?

## 💥 Failure 3 — Resource pressure

Set an intentionally inappropriate memory limit and observe the resulting behavior.

Explain OOMKilled and the difference between application failure and node-level memory pressure.

## 💥 Failure 4 — NetworkPolicy

Apply a restrictive policy and break application connectivity.

Determine:

- source identity
- destination identity
- port
- namespace
- policy direction

## 🧠 Deliverable

For every failure write:

1. symptom
2. evidence
3. hypothesis
4. test
5. mitigation
6. verification
7. preventive control

## ⚫ Interview challenge

Your interviewer says: “The pod is Running. Why is the application down?”

Do not answer with another command. Explain the state model and the signals you would inspect.
