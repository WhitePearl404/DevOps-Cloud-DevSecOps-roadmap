# Cloud Security Interview Questions

Use the [Interview Answer Framework](./answer-framework.md). Strong cloud-security answers connect **identity → preventive control → detection → response → recovery → evidence**.

1. What is least privilege?
2. How do IAM policy evaluation rules work?
3. IAM role vs access key?
4. How would you secure an AWS account from day one?
5. How do you centralize audit logs?
6. GuardDuty vs Security Hub?
7. What does Inspector detect?
8. What does Macie help protect?
9. What is AWS Config used for?
10. What is Security Lake?
11. How would you detect compromised credentials?
12. How would you automate containment?
13. What is Zero Trust?
14. What is defense in depth?
15. How do SCPs differ from IAM policies?
16. How do you secure an EKS cluster?
17. How do you implement Kubernetes network segmentation?
18. How do you secure Kubernetes workloads at runtime?
19. How would you design a cloud incident-response workflow?
20. How do you balance security with developer velocity?

## High-value answer anchors

### 1. Secure an AWS account from day one

Structure the answer by control layer:

```text
Identity
→ Organization / guardrails
→ Audit logging
→ Detection
→ Network boundaries
→ Data protection
→ Vulnerability management
→ Incident response
```

Discuss root-user protection, least privilege, MFA, centralized logging, preventive guardrails, encryption, findings aggregation and automated response. Explain which controls are organization-wide versus workload-specific.

### 2. GuardDuty vs Security Hub

Do not treat them as interchangeable products.

Explain:

- what each service is intended to detect or aggregate
- where findings originate
- how findings move through the security workflow
- how they complement other AWS security services
- where automation such as EventBridge/Lambda can fit

### 3. Suspicious IAM activity

Use:

```text
Detect
→ Validate
→ Contain
→ Preserve evidence
→ Scope
→ Recover
→ Prevent recurrence
```

Consider CloudTrail and relevant detection findings, identity/session context, recent changes, affected resources, credential revocation/rotation and verification of containment.

### 4. Secure EKS

Cover multiple boundaries:

- AWS IAM and workload identity
- cluster/API access
- Kubernetes RBAC
- Pod Security Standards
- NetworkPolicy
- secrets
- image and supply-chain controls
- admission policy
- node/workload isolation
- audit logging
- runtime detection

Then explain why each layer exists instead of merely listing security products.

### 5. Automate containment

A defensible response should specify:

1. trigger and confidence threshold
2. affected identity/resource
3. safe containment action
4. approval or exception path where required
5. evidence preservation
6. verification
7. rollback/recovery
8. post-incident control improvement

Automation should reduce response time without blindly destroying evidence or causing a larger outage.

## Scenario

An IAM principal shows suspicious API activity from an unfamiliar location.

Explain:

1. detection source
2. validation
3. containment
4. credential rotation/revocation
5. scope assessment
6. forensic evidence
7. recovery
8. lessons learned
9. preventive controls

## Senior follow-ups

Expect:

- What is the blast radius?
- Which logs are authoritative?
- How do you distinguish a compromised credential from legitimate automation?
- What happens if the attacker has persistence?
- Which actions can be automated safely?
- How do you test the response workflow?
- How do you avoid blocking developers unnecessarily?
