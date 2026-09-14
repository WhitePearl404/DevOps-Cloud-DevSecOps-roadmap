# Cloud Interview Questions

Use four levels for every answer: **definition → mechanism → architecture → failure/trade-off**.

## Fundamentals

1. IaaS vs PaaS vs SaaS?
2. Region vs Availability Zone?
3. Scalability vs elasticity?
4. High availability vs disaster recovery?
5. Horizontal vs vertical scaling?
6. What is a load balancer?
7. What is a reverse proxy?
8. What is a CDN?
9. What is a VPC?
10. Public vs private subnet?
11. What is NAT?
12. What is shared responsibility?
13. What is fault tolerance?
14. What is stateless vs stateful architecture?
15. What is autoscaling?
16. What is a health check?
17. What is an availability domain/failure domain?
18. What is infrastructure as code?
19. Why use managed services?
20. What is cloud vendor lock-in?

## Architecture

21. Design a highly available web application.
22. Design a three-tier application in a VPC.
23. Design a private application tier with a managed database.
24. How would you design for an Availability Zone failure?
25. How would you design disaster recovery?
26. How would you migrate a traditional application to the cloud?
27. How would you design a multi-account environment?
28. How would you centralize logging across accounts?
29. How would you design secure private access to cloud services?
30. How would you design a globally distributed application?

## Security

31. How do you implement least privilege?
32. Why prefer temporary workload credentials over long-lived keys?
33. How do you segment cloud networks?
34. How do you protect secrets?
35. How do you encrypt data at rest and in transit?
36. How do you detect public exposure of resources?
37. How would you respond to compromised credentials?
38. How do you centralize security findings?
39. How do you design security logging that attackers cannot easily tamper with?
40. How do you balance security controls with developer velocity?

## Reliability and cost

41. How do you design for failure?
42. How do RTO and RPO influence architecture?
43. How do you test disaster recovery?
44. How do you reduce cloud cost without weakening reliability?
45. How do you identify an over-provisioned workload?
46. What makes an alert actionable?
47. What is an SLO and why does it matter?
48. How would you safely deploy a high-risk change?
49. How would you investigate a sudden latency increase?
50. What makes a system production-ready?

## Scenario

Design a production service with:

- high availability
- private application/database tiers
- centralized logging
- encryption
- least-privilege IAM
- automated deployment
- monitoring and alerting
- backup and recovery
- defined RTO/RPO
- documented failure modes

Explain the architecture, request path, trust boundaries, failure domains, operational model and trade-offs.

## Follow-up rule

For every architecture answer, expect:

- Why this design?
- What can fail?
- What is the blast radius?
- How do you secure it?
- How do you monitor it?
- How does it scale?
- What does it cost?
- How do you recover?
- What would make you choose a different design?
