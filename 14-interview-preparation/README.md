# 14 — Interview Preparation

This section is built around the way real technical interviews work: fundamentals, architecture, troubleshooting, trade-offs and follow-up questions.

## 🎯 Preparation framework

For every topic, prepare four levels:

1. **30-second answer** — simple definition
2. **2-minute answer** — how it works
3. **Architecture answer** — components and data flow
4. **Scenario answer** — what you would do when it fails

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

## 🧠 Interview answer template

```text
1. Define the concept
2. Explain why it exists
3. Explain how it works
4. Give a practical example
5. Mention security/reliability concerns
6. Discuss trade-offs
7. Handle follow-up questions
```

## 🔥 High-value interview areas

### DevOps
- CI/CD architecture
- Deployment strategies
- Rollbacks
- Pipeline security
- Artifact management

### Cloud
- VPC architecture
- IAM
- HA and DR
- Scaling
- Cost optimization

### Kubernetes
- Cluster architecture
- Scheduling
- Networking
- Storage
- Security
- Troubleshooting

### DevSecOps
- SAST/SCA/DAST
- Secrets
- IaC security
- Container security
- SBOM
- Signing and provenance

### Cloud Security
- Least privilege
- Detection and response
- Security logging
- Zero Trust
- Incident response

## 🚨 Scenario practice

Never answer a production incident with “I would restart the server.” Humanity has suffered enough.

Practice scenarios such as:

- deployment succeeded but users receive 5xx
- pods are stuck Pending
- pods are CrashLoopBackOff
- DNS works intermittently
- latency suddenly increases
- AWS credentials are compromised
- Terraform state is locked
- container image contains a critical CVE
- Argo CD reports drift
- CI pipeline starts leaking secrets
