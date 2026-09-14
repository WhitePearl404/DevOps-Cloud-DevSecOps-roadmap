# Terraform vs OpenTofu

## 💡 Problem

Both tools provide declarative infrastructure-as-code workflows. The decision is not simply about syntax. Consider ecosystem compatibility, governance, provider/module support, licensing requirements, team familiarity and operational tooling.

## 🟢 Beginner

Learn Terraform concepts first if it is the first IaC tool you encounter:

- providers
- resources
- variables
- outputs
- state
- modules
- plan/apply

Then understand OpenTofu as a compatible open-source IaC ecosystem with its own roadmap and tooling.

## 🟡 Decision factors

| Factor | Terraform | OpenTofu |
|---|---|---|
| Core IaC model | Mature | Terraform-compatible model |
| Ecosystem | Very broad | Broad and growing |
| Existing team skill | Often decisive | Often decisive |
| Governance/licensing | Review current terms | Open-source governance model |
| Migration effort | Depends on existing state/config | Depends on providers/modules/workflow |

Do not treat compatibility as a guarantee that every future feature or third-party integration will remain identical.

## 🔴 Production decision

Choose based on:

- existing state and modules
- provider support
- CI/CD integration
- policy and security tooling
- vendor requirements
- team expertise
- long-term governance
- migration cost

## ⚫ Interview question

**When would you choose OpenTofu over Terraform?**

A strong answer starts with organizational requirements, ecosystem compatibility and governance rather than declaring one tool universally superior.
