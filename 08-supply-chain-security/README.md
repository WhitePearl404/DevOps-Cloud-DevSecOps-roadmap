# 08 — Software Supply Chain Security

## 🟢 Beginner

- Software supply-chain risk
- Dependencies
- Registries
- Immutable artifacts
- Basic vulnerability scanning

## 🟡 Intermediate

- SBOM concepts
- SPDX and CycloneDX concepts
- Syft
- Grype
- Image signing
- Cosign
- Sigstore

## 🔴 Advanced

- Provenance
- Attestations
- SLSA concepts
- in-toto concepts
- Verification at deployment
- Trusted build systems
- Artifact promotion
- Hermetic/reproducible build concepts

## 🔐 Security chain

```text
Source
 ↓
Build
 ↓
Dependencies
 ↓
SBOM
 ↓
Vulnerability Scan
 ↓
Provenance
 ↓
Signature
 ↓
Registry
 ↓
Verification
 ↓
Deployment
```

## ⚫ Interview focus

- What is an SBOM?
- Why sign container images?
- What problem does provenance solve?
- Syft vs Grype?
- What is Sigstore?
- What is SLSA?
- How would you prevent an untrusted image from reaching production?
