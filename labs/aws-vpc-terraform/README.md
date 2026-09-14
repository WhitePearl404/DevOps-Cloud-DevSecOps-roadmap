# Lab 01 — Secure AWS VPC with Terraform

## 🎯 Objective

Build a small production-style AWS network and learn to reason about segmentation, routing, security boundaries, failure modes and cost.

## Prerequisites

- Basic Linux and networking knowledge
- AWS account with appropriate permissions
- Terraform/OpenTofu installed
- AWS CLI configured without hard-coded credentials

## Architecture

```text
                         Internet
                            │
                     Internet Gateway
                            │
             ┌──────────────┴──────────────┐
             │                             │
        Public Subnet                 Public Subnet
             │                             │
        NAT Gateway                   NAT Gateway
             │                             │
        Private Subnet                Private Subnet
             │                             │
             └──────── Application ────────┘
                            │
                      Database tier
```

## 🟢 Build

Create with Terraform/OpenTofu:

- one VPC
- two availability zones
- public and private subnets
- route tables
- internet connectivity for public resources
- controlled outbound connectivity for private resources
- security groups

Verify with `terraform plan` before applying changes. Record the final architecture and important outputs.

## Expected outcome

You should be able to explain:

- why the application tier is private
- why the database should not be public
- why route tables matter
- how Internet Gateway and NAT Gateway differ
- where the security boundaries are
- which components create recurring cost

## 🟡 Explain before deploying

Answer these without looking at the implementation:

1. Why use two AZs?
2. What happens when a private subnet has no valid egress route?
3. Why is a security group not a replacement for network segmentation?
4. What changes if the application needs no internet access at all?
5. What would you change for a multi-account environment?

## 🛡️ Security challenge

After the baseline works:

1. remove public SSH access
2. restrict security-group sources
3. use IAM roles instead of embedded credentials
4. enable relevant network and audit logging
5. run an IaC security scan
6. check for accidental public exposure

Document each control and what risk it reduces.

## 🚨 Break it

Intentionally introduce one failure at a time:

- remove or corrupt a route
- block the application security group
- misconfigure DNS
- remove private-subnet egress
- introduce an overly broad security-group rule

For each failure record:

```text
Symptom
→ Evidence
→ Hypothesis
→ Test
→ Fix
→ Verification
→ Preventive control
```

## 🔎 Evidence to collect

Use the evidence appropriate to the failure:

- Terraform plan/state information
- route tables
- security-group rules
- subnet and AZ configuration
- VPC Flow Logs where enabled
- DNS resolution tests
- application connectivity tests
- AWS audit logs where relevant

Do not treat “it works now” as verification. State what changed and what evidence proves recovery.

## 💰 Cost considerations

Identify the main cost drivers before deployment. In particular, understand NAT Gateway, data transfer, logging and always-on resource costs. Destroy disposable resources after the exercise.

## 🧹 Cleanup

Run the planned teardown and verify that resources were actually removed. Check the AWS console and billing/cost views for resources that survived the teardown.

## ⚫ Interview questions

- Why use two AZs?
- NAT Gateway vs Internet Gateway?
- Security Group vs NACL?
- How would you make the design more resilient?
- How would you reduce NAT cost?
- How would you detect accidental public exposure?
- How would you design this across multiple AWS accounts?
- How would you prove a network failure rather than guess at it?

## Extension challenge

Design a version with no direct internet access for application workloads. Explain the required AWS endpoints, routing changes, security implications and cost trade-offs before implementing it.