# Cloud Networking

## What this role does
Designs and secures networks in AWS, Azure, or GCP: virtual networks, routing, connectivity to on-premises sites, and load balancing. It is the fastest-growing part of networking.

## Prerequisites
Finish [CCNA](../1-basics/ccna.md). Subnetting, routing, NAT, and DNS knowledge transfers directly. Pick one cloud and learn it well before adding others.

## Skills to learn, in order
1. Cloud fundamentals: regions, availability zones, shared responsibility
2. Virtual networks: AWS VPC / Azure VNet, subnets, route tables
3. Internet access: gateways, NAT, security groups vs. network ACLs
4. Connectivity: peering, transit gateways, site-to-site VPN, private links
5. DNS and load balancing
6. Infrastructure as Code with Terraform
7. Hybrid design and cost awareness

## Resources
| Resource | Type | Level | Free/Paid | Notes |
|---|---|---|---|---|
| [AWS Skill Builder](https://skillbuilder.aws) | Courses | Beginner | Free tier | Cloud Practitioner prep and networking fundamentals. |
| [Microsoft Learn](https://learn.microsoft.com) | Courses | Beginner | Free | Free learning paths for AZ-900 and the Azure networking exam. |
| [Google Cloud Skills Boost](https://www.cloudskillsboost.google) | Labs | Beginner | Free + paid | Hands-on labs, with some free credits. |
| [Terraform tutorials](https://developer.hashicorp.com/terraform/tutorials) | Tutorials | Intermediate | Free | Build cloud networks as code. |
| Cloud provider free tiers | Sandbox | Beginner | Free | Set billing alerts before experimenting. |
| [Adrian Cantrill courses](https://learn.cantrill.io) | Video courses | Intermediate | Paid | Widely considered the deepest AWS teaching. Worth paying for one course. |

## Certifications
AWS Cloud Practitioner, then Solutions Architect Associate, then the AWS Advanced Networking Specialty. On Azure: AZ-900, then the Azure Network Engineer Associate (AZ-700). Verify current exam codes before booking.

## Project to build
A VPC in Terraform with public and private subnets, a NAT gateway, a bastion or SSM access, and a VPN or peering to a second VPC. Keep it in a Git repo with a diagram and a cost note.
