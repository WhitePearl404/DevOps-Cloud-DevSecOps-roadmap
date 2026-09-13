# DevSecOps Interview Questions

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

## Scenario

Design a pipeline that prevents:

- leaked secrets
- vulnerable dependencies
- insecure Terraform
- vulnerable container images
- unsigned artifacts
- unapproved Kubernetes configurations

Your answer should include controls, failure behavior, exceptions, auditing and developer feedback.
