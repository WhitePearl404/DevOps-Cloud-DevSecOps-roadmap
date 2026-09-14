# Terraform Deep Dive

## 💡 What is Terraform?

Terraform is a declarative infrastructure-as-code tool. You describe desired infrastructure, Terraform builds a dependency graph, compares configuration with state and the observed provider data, and proposes changes.

## 🧠 Core model

```text
Configuration
     ↓
  Provider
     ↓
  Dependency graph
     ↓
    Plan
     ↓
   Apply
     ↓
 Infrastructure
     ↓
    State
```

## 🟢 Beginner

Learn:

- providers
- resources
- variables
- locals
- outputs
- data sources
- expressions
- plan/apply/destroy
- state

## 🟡 Intermediate

- modules
- remote state
- locking
- imports
- lifecycle rules
- dependencies
- multiple environments
- CI validation
- formatting and linting
- secrets handling

## 🔴 Advanced

- module interfaces
- multi-account architecture
- drift detection
- testing
- policy-as-code
- security scanning
- controlled state migration
- GitOps integration
- platform provisioning

## 🛡️ Security

Never treat Terraform code as harmless text. It can create privileged identities, public networks and data stores.

Controls should include:

- secret scanning
- IaC scanning
- least-privilege deployment identities
- protected state
- review gates
- plan review
- policy-as-code
- audit logging

## 🚨 Dangerous plan scenario

If production proposes destroying a critical resource:

```text
STOP
 ↓
Do not apply
 ↓
Inspect plan
 ↓
Compare configuration/state
 ↓
Check recent changes
 ↓
Investigate drift
 ↓
Validate dependencies
 ↓
Correct safely
 ↓
Re-plan
 ↓
Apply only after review
```

## 🛠️ Lab

Build a reusable AWS VPC module and require:

- `terraform fmt`
- `terraform validate`
- plan review
- IaC security scanning
- secret scanning
- controlled environment promotion

Then intentionally introduce a configuration change that would replace a resource and explain why Terraform proposes it.

## ⚫ Interview questions

- Why does Terraform need state?
- What is drift?
- What is the dependency graph?
- Why can a resource be replaced instead of updated?
- How do you secure remote state?
- How do you structure modules?
- Terraform vs Ansible?
- Terraform vs OpenTofu?
