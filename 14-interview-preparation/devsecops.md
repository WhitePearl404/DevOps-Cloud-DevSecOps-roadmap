# DevSecOps Interview Questions

Use the [Interview Answer Framework](./answer-framework.md). Strong DevSecOps answers connect **risk → control → enforcement point → developer feedback → exception handling → evidence**.

1. What is DevSecOps?
2. Why shift security left?
3. SAST vs DAST?
4. SCA vs SAST?
5. What is IaC security?
6. Where should secrets scanning run?
7. How do you handle a critical vulnerability in a production image?
8. What should be a blocking security gate?
9. How do you avoid overwhelming developers with findings?
10. What is an SBOM?
11. Why sign container images?
12. What is provenance?
13. What problem does Sigstore solve?
14. What is policy-as-code?
15. Kyverno vs OPA/Rego?
16. How do you secure GitHub Actions?
17. How do you protect CI/CD secrets?
18. How do you prevent dependency confusion and malicious packages?
19. How would you design a secure software supply chain?
20. How do you measure DevSecOps effectiveness?

## High-value answer anchors

### 1. What should be a blocking security gate?

Do not answer with “everything critical.” Define policy using:

- severity
- exploitability
- asset exposure
- runtime context
- confidence/false-positive rate
- availability of a safe remediation
- exception process

Then explain where the gate runs, who owns exceptions, how exceptions expire, and how results are audited.

### 2. Critical vulnerability in a production image

Use:

```text
Validate finding
→ Identify affected artifacts/workloads
→ Assess exploitability and exposure
→ Contain if necessary
→ Patch/rebuild
→ Rescan
→ Deploy safely
→ Verify runtime state
→ Prevent recurrence
```

Mention rollback, emergency exceptions and evidence preservation when appropriate.

### 3. Secure software supply chain

Cover:

```text
Source
→ Commit protection
→ SAST / SCA / secret scanning
→ IaC policy
→ Build isolation
→ Dependency provenance
→ Image scanning
→ SBOM
→ Signing / provenance
→ Verification at deployment
→ Runtime monitoring
```

Explain which controls are preventive, which are detective, and where trust is established.

### 4. Secure GitHub Actions

Cover:

- least-privilege `GITHUB_TOKEN`
- pinned or trusted actions
- protected environments
- short-lived cloud credentials through workload identity/OIDC where supported
- secret minimization
- pull-request trust boundaries
- artifact integrity
- logging and auditability
- restrictions on untrusted code execution

### 5. Measure DevSecOps effectiveness

Avoid counting scans alone. Consider:

- vulnerability remediation time
- escaped vulnerability rate
- false-positive rate
- security-gate override rate
- percentage of artifacts with SBOM/provenance
- policy compliance
- mean time to detect/respond to supply-chain issues
- developer feedback and remediation friction

## Scenario

Design a pipeline that prevents:

- leaked secrets
- vulnerable dependencies
- insecure Terraform
- vulnerable container images
- unsigned artifacts
- unapproved Kubernetes configurations

Your answer should include controls, enforcement points, failure behavior, exceptions, auditing and developer feedback.

## Senior follow-ups

Expect:

- What happens when a security tool is unavailable?
- What happens when a finding is a false positive?
- Who can approve an exception?
- How does the exception expire?
- Can an attacker bypass the pipeline?
- How do you verify an artifact was not replaced after scanning?
- What evidence would you preserve during a supply-chain incident?
