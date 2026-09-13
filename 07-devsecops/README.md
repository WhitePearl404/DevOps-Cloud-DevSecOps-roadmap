# 07 — DevSecOps

Security belongs throughout the software lifecycle, not in a panic-driven meeting five minutes before release.

## 🟢 Beginner

- Secure SDLC
- Threat awareness
- Vulnerability vs threat vs risk
- Dependency security
- Secrets security
- Basic static analysis

## 🟡 Intermediate

### SAST
- Semgrep
- Secure coding patterns

### SCA
- Dependency vulnerability scanning
- Dependency pinning
- License awareness

### Secrets
- Gitleaks
- Secret rotation
- CI secret handling

### IaC security
- Checkov
- tfsec concepts
- Misconfiguration detection

### Container security
- Trivy
- Image hardening
- Runtime basics

### DAST
- Dynamic application testing
- OWASP-aligned testing

## 🔴 Advanced

- Security gates and risk thresholds
- Vulnerability management
- Security exceptions
- Policy-as-code
- Runtime detection
- Supply-chain security
- Provenance and artifact verification
- Security observability

## 🧩 Reference pipeline

```text
Developer
  ↓
SAST ── SCA ── Gitleaks
  ↓
IaC Scan
  ↓
Build
  ↓
Container Scan
  ↓
SBOM
  ↓
Sign + Provenance
  ↓
Policy Verification
  ↓
Deploy
  ↓
Runtime Detection
```

## ⚫ Interview focus

- What is DevSecOps?
- SAST vs DAST?
- SCA vs SAST?
- How do you prevent secrets in Git?
- Where should IaC scanning run?
- What should block a deployment?
- How do you handle a critical vulnerability that cannot be fixed immediately?
- How do SBOMs improve vulnerability management?
