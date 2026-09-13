# Terraform / IaC Interview Questions

1. What is Infrastructure as Code?
2. What is Terraform state?
3. Why use remote state?
4. What is state locking?
5. What is a Terraform module?
6. Resource vs data source?
7. Variable vs local?
8. What does `terraform plan` do?
9. What happens during `terraform apply`?
10. What causes resource replacement?
11. What is drift?
12. How do you import existing resources?
13. How do you secure Terraform state?
14. Terraform vs Ansible?
15. Terraform vs OpenTofu?
16. How do you validate Terraform in CI?
17. How do you scan IaC for security issues?
18. How do you manage multiple environments?
19. How do you design reusable modules?
20. What would you do if Terraform state became unavailable during an incident?

## Senior scenario

A production plan unexpectedly proposes destroying a critical resource.

Explain how you would:

- stop the change
- inspect the plan
- identify state/configuration differences
- verify dependencies
- determine whether drift exists
- correct the configuration safely
- protect future deployments
