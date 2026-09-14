# Lab 01 — Secure AWS VPC with Terraform

## 🎯 Objective

Build a small production-style network while learning why each component exists.

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

Create:

- one VPC
- two availability zones
- public and private subnets
- route tables
- internet connectivity for public resources
- controlled outbound connectivity for private resources
- security groups

## 🟡 Explain

Before deployment, explain:

- why the application tier is private
- why the database should not be public
- why route tables matter
- why security groups are not a substitute for subnet design
- what failure occurs if private workloads have no egress path

## 🛡️ Security challenge

After the basic implementation works:

1. remove public SSH access
2. restrict security-group sources
3. use IAM roles instead of embedded credentials
4. enable relevant logging
5. run an IaC security scan

## 🚨 Break it

Intentionally:

- remove a route
- block the application security group
- misconfigure DNS
- remove private-subnet egress

Then diagnose from evidence rather than guessing.

## 🧹 Cleanup

Destroy all disposable resources after verification. Check the AWS console and billing/cost views for resources that survived the teardown.

## ⚫ Interview questions

- Why use two AZs?
- Why are databases private?
- NAT Gateway vs Internet Gateway?
- Security Group vs NACL?
- How would you make the design more resilient?
- How would you reduce NAT cost?
- How would you detect accidental public exposure?
