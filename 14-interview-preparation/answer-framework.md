# Interview Answer Framework

Use this framework to turn a tool-level answer into an engineering answer.

## 1. The 30-second answer

State:

1. what the technology or concept is
2. the problem it solves
3. where it fits in the system

Keep it precise. Do not list every feature you have ever seen in documentation.

## 2. The 2-minute answer

Use this sequence:

```text
Definition
→ Problem
→ Architecture
→ How it works
→ Practical example
→ Security / reliability
→ Trade-offs
```

A strong answer explains causality, not vocabulary.

## 3. The production answer

When the interviewer adds a production constraint, structure the response as:

```text
Context
→ Symptoms
→ Evidence
→ Hypotheses
→ Tests
→ Mitigation
→ Verification
→ Prevention
```

Examples of evidence:

- application logs
- metrics
- traces
- Kubernetes events and object state
- cloud audit logs
- CI/CD logs
- Terraform plan/state information
- network flow or policy telemetry

## 4. The architecture answer

For architecture questions, cover:

| Area | Questions to answer |
|---|---|
| Requirements | What are the availability, latency, security and cost constraints? |
| Components | What services or layers are required? |
| Data flow | How does traffic or data move through the system? |
| Failure domains | What happens when a component, AZ, node or dependency fails? |
| Security | Where are identity, network, secrets and policy controls enforced? |
| Observability | What signals prove the system is healthy? |
| Recovery | How is failure detected, contained and recovered? |
| Cost | Which choices materially affect operating cost? |
| Trade-offs | What did you deliberately choose not to optimize? |

## 5. The troubleshooting answer

Never jump directly to a fix.

```text
1. Define the user-visible symptom
2. Establish scope and blast radius
3. Check recent changes
4. Gather evidence
5. Form ranked hypotheses
6. Test the safest hypothesis
7. Mitigate impact
8. Verify recovery
9. Identify the preventive control
```

## 6. The security answer

For security questions, think in layers:

```text
Identity
→ Network
→ Workload
→ Data
→ Supply chain
→ Detection
→ Response
→ Recovery
```

Explain both preventive and detective controls. A control that exists only in a diagram is not a control.

## 7. The trade-off answer

Senior interviews often test judgment rather than product recall.

Use:

```text
Option A is better when...
Option B is better when...
The deciding constraint is...
The operational cost is...
The security/reliability impact is...
I would choose ... because...
```

## 8. Follow-up defense

Expect questions such as:

- Why this design instead of the obvious alternative?
- What fails first?
- How would you detect that failure?
- How would you roll it back?
- What is the security boundary?
- What happens at 10x traffic?
- What would you automate?
- What would you monitor?
- What would you change if cost were the primary constraint?

## 9. Weak-answer patterns to avoid

| Weak pattern | Better approach |
|---|---|
| Tool-name dumping | Explain the problem and architecture |
| “It depends” with no decision | State the deciding constraints and choose |
| Fix-first troubleshooting | Evidence → hypothesis → test → fix |
| Security as an afterthought | Include security boundaries in the design |
| “Highly available” with no failure model | Name failure domains and recovery behavior |
| “I would monitor it” | Name signals, thresholds and useful alerts |
| “I have used Kubernetes” | Explain one real deployment, failure and recovery path |

## 10. Evidence standard

For portfolio-backed answers, connect the answer to evidence:

- repository design
- Terraform code
- Kubernetes manifests
- CI/CD workflow
- security scan output
- failure-drill notes
- architecture diagram
- incident or troubleshooting record

Do not claim production experience you cannot demonstrate. Strong reasoning is more credible than inflated experience.

## Practice rule

For each major topic, prepare:

- one 30-second explanation
- one 2-minute explanation
- one architecture scenario
- one failure scenario
- one security question
- one trade-off question
- two likely follow-ups

The goal is not memorization. The goal is being able to reason under constraints.