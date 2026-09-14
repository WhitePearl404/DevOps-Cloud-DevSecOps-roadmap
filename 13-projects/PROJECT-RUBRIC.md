# Project Scoring Rubric

Use this rubric to judge whether a project demonstrates engineering ability rather than simply containing a large number of technologies.

## Scorecard

| Area | Weight | What good evidence looks like |
|---|---:|---|
| Architecture | 15 | Clear components, data flow, boundaries, dependencies and failure domains |
| Infrastructure as Code | 10 | Reproducible infrastructure, variables, state handling and safe changes |
| Automation | 10 | Repeatable build, deployment, testing or operational workflows |
| Security | 15 | Identity, secrets, network, workload and supply-chain controls are designed in |
| CI/CD | 10 | Quality gates, artifact flow, deployment strategy and rollback behavior |
| Observability | 10 | Useful logs, metrics and/or traces with actionable signals |
| Reliability | 10 | Health checks, failure handling, recovery and resilience are demonstrated |
| Documentation | 10 | Architecture, setup, decisions, troubleshooting and limitations are documented |
| Cost awareness | 5 | Material cost drivers and cleanup/optimization choices are identified |
| Troubleshooting | 5 | At least one failure is intentionally reproduced, investigated and fixed |
| **Total** | **100** | |

## Rating

| Score | Interpretation |
|---:|---|
| 90–100 | **Portfolio-ready**: strong evidence of production-oriented engineering thinking |
| 75–89 | **Strong**: good engineering depth with a few gaps to close |
| 60–74 | **Developing**: useful project, but important production concerns remain |
| Below 60 | **Educational**: demonstrates learning, not yet strong portfolio evidence |

## Evidence-first scoring

Score evidence, not technology count.

A project using 25 tools without explaining why they exist should score lower than a smaller system with clear architecture, security controls, failure testing and operational reasoning.

### Architecture — 15 points

Check for:

- requirements and constraints
- component responsibilities
- traffic/data flow
- trust boundaries
- failure domains
- explicit design decisions

### Infrastructure as Code — 10 points

Check for:

- reproducibility
- variables and outputs
- safe defaults
- state strategy
- validation
- plan/review workflow
- cleanup

### Automation — 10 points

Check for:

- repeatable setup
- automated tests or checks
- deployment automation
- idempotent operations where appropriate
- reduced manual steps

### Security — 15 points

Check for:

- least-privilege identity
- secret handling
- network segmentation
- workload security
- dependency/container/IaC scanning where relevant
- policy enforcement
- auditability

### CI/CD — 10 points

Check for:

- source-to-artifact flow
- quality/security gates
- immutable or traceable artifacts
- deployment strategy
- rollback or recovery path

### Observability — 10 points

Check for:

- logs
- metrics
- traces when appropriate
- health indicators
- actionable alerts
- correlation between symptoms and evidence

### Reliability — 10 points

Check for:

- health checks
- graceful failure behavior
- redundancy where justified
- backup/recovery considerations
- recovery verification
- defined availability or performance expectations where appropriate

### Documentation — 10 points

Check for:

- architecture diagram
- prerequisites
- deployment steps
- security decisions
- troubleshooting guide
- limitations
- cleanup
- decision records or trade-offs

### Cost awareness — 5 points

Identify:

- major cost drivers
- unnecessary always-on resources
- data transfer implications
- storage/retention costs
- cleanup strategy

### Troubleshooting — 5 points

Require at least one controlled failure:

```text
Break
→ Observe
→ Gather evidence
→ Form hypothesis
→ Test
→ Fix
→ Verify
→ Prevent
```

## Portfolio evidence checklist

Before calling a project portfolio-ready, make sure the repository contains most of the following:

- [ ] architecture diagram
- [ ] reproducible setup
- [ ] IaC
- [ ] automated validation
- [ ] security controls
- [ ] CI/CD workflow
- [ ] observability
- [ ] failure drill
- [ ] troubleshooting notes
- [ ] cost considerations
- [ ] cleanup procedure
- [ ] design trade-offs
- [ ] interview questions

## Senior-level test

A project should not be considered senior-level merely because it uses Kubernetes, Terraform, AWS or a long list of security tools.

Ask:

1. What problem does the architecture solve?
2. What are the important failure modes?
3. What is the security boundary?
4. How do you know the system is healthy?
5. What happens during a bad deployment?
6. How do you recover?
7. What would you change at 10x scale?
8. What would you remove if cost became the primary constraint?
9. Which controls are preventive and which are detective?
10. What evidence proves the design works?

If the project cannot answer these questions, add depth before adding another technology.