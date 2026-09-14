# 14 — Interview Preparation

This section is built around the way real technical interviews work: fundamentals, architecture, troubleshooting, security, trade-offs and follow-up questions.

## 🎯 Preparation framework

For every major topic, prepare four levels:

1. **30-second answer** — what it is and the problem it solves
2. **2-minute answer** — how it works and where it fits
3. **Architecture answer** — components, data flow, boundaries and failure domains
4. **Scenario answer** — evidence, diagnosis, mitigation, recovery and prevention

See the full [Interview Answer Framework](./answer-framework.md).

## 📚 Question banks

- [DevOps](./devops.md)
- [Cloud](./cloud.md)
- [AWS](./aws.md)
- [Kubernetes](./kubernetes.md)
- [Terraform / IaC](./terraform.md)
- [DevSecOps](./devsecops.md)
- [Cloud Security](./security.md)
- [Troubleshooting](./troubleshooting.md)
- [Scenario-based](./scenario-based.md)

## 🧠 Default answer structure

```text
Define
→ Explain the problem
→ Explain the architecture / mechanism
→ Give a practical example
→ Cover security and reliability
→ Discuss trade-offs
→ Handle follow-ups
```

For production incidents:

```text
Symptom
→ Scope
→ Evidence
→ Hypotheses
→ Test
→ Mitigate
→ Verify
→ Prevent
```

## 🔥 High-value interview areas

### DevOps
- CI/CD architecture
- deployment strategies
- rollbacks
- pipeline security
- artifact management

### Cloud
- VPC architecture
- IAM
- HA and DR
- scaling
- cost optimization

### Kubernetes
- cluster architecture
- scheduling
- networking
- storage
- security
- troubleshooting

### DevSecOps
- SAST/SCA/DAST
- secrets management
- IaC security
- container security
- SBOM
- signing and provenance

### Cloud Security
- least privilege
- detection and response
- security logging
- Zero Trust
- incident response

## 🚨 Scenario practice

Production incidents should be answered with evidence and a recovery plan, not a collection of increasingly desperate restart commands.

Practice scenarios such as:

- deployment succeeded but users receive 5xx
- Pods are stuck Pending
- Pods are CrashLoopBackOff
- DNS works intermittently
- latency suddenly increases
- AWS credentials are compromised
- Terraform state is locked
- container image contains a critical CVE
- Argo CD reports drift
- CI pipeline starts leaking secrets

## Senior-level follow-ups

For each scenario, be ready to answer:

- What is the blast radius?
- What evidence would you collect first?
- What changed recently?
- What is the safest immediate mitigation?
- How would you verify recovery?
- How would you prevent recurrence?
- What trade-off does your proposed fix introduce?

## Practice standard

Do not memorize model answers. Use the question banks to practice reasoning under constraints and connect answers to evidence from labs and projects.