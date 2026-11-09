# Cloud Networking

**Role:** designs and secures networks in AWS, Azure or GCP and connects them to on-premises sites.
**Prerequisites:** [CCNA](../1-basics/ccna.md). Pick one cloud first.

## Skills, in order
1. Cloud fundamentals: regions, AZs, shared responsibility
2. VPC/VNet, subnets, route tables
3. Gateways, NAT, security groups vs. NACLs
4. Peering, transit gateways, VPN, private links
5. DNS and load balancing
6. Terraform
7. Hybrid design and cost awareness

**Path at a glance:**
- Beginner: AWS Networking Basics or the Azure AZ-900 path, plus Terraform get-started.
- Intermediate: the VPC docs, the Google Cloud networking course, or the AZ-700 path, depending on your chosen cloud.
- Advanced: Adrian Cantrill for deep AWS teaching.

**Cost warning:** set billing alerts before any lab, and tear down resources when finished.

## Resources
| Resource | Level | Cost | What it is | You will be able to |
|---|---|---|---|---|
| [AWS Skill Builder: AWS Networking Basics](https://skillbuilder.aws) | Beginner | Free | Roughly two-hour introductory course on AWS networking and VPC basics. Optional hands-on labs can cost extra. | Explain core AWS networking services and design a simple VPC. |
| [Microsoft Learn: AZ-900 path](https://learn.microsoft.com) | Beginner | Free | Azure fundamentals learning path. | Explain core Azure concepts before specialising. |
| [Terraform tutorials (AWS get-started)](https://developer.hashicorp.com/terraform/tutorials/aws-get-started) | Beginner to Intermediate | Free | Step-by-step tutorials to create, change and destroy infrastructure. Azure, GCP and Docker versions exist on the same site. | Provision and destroy cloud infrastructure from code. |
| [freeCodeCamp cloud courses](https://www.youtube.com/@freecodecamp) | Beginner | Free | Full-length certification prep videos on YouTube. | Follow a complete cloud course at no cost. |
| [AWS VPC documentation](https://docs.aws.amazon.com/vpc/latest/userguide/what-is-amazon-vpc.html) | Intermediate | Free | Official reference. | Configure subnets, route tables, gateways and endpoints correctly. |
| [Google Cloud: Networking in Google Cloud, Fundamentals](https://www.cloudskillsboost.google/course_templates/35) | Intermediate | Free course, labs can use credits | Roughly five-hour course on VPC networks, sharing, routing and monitoring. Assumes IPv4 and routing knowledge. | Build and share VPCs, and connect networks on Google Cloud. |
| [Microsoft Learn: AZ-700 path](https://learn.microsoft.com/training/paths/design-implement-microsoft-azure-networking-solutions-az-700) | Intermediate to Advanced | Free | Official path for the Azure networking exam. Expects experience with the Azure portal and PowerShell. | Design hybrid connectivity, routing and secured Azure networks. |
| [Adrian Cantrill](https://learn.cantrill.io) | Intermediate to Advanced | Paid | Deep AWS video courses. Worth buying one course. | Understand AWS networking internals, not just the console. |

## Certifications
AWS Cloud Practitioner, Solutions Architect Associate, Advanced Networking Specialty. Azure: AZ-900, then AZ-700.

## Project

### Tutorial projects
Each project takes about a week (roughly 8 to 12 hours) and covers several skills from the list above. Do them in order, and keep each one in its own Git repo or folder.

1. **Core VPC in Terraform** (Beginner, ~1 week)
   - **Build:** a VPC across two availability zones with public and private subnets, internet and NAT gateways and route tables, written as a reusable Terraform module. Set a billing alert first.
   - **Practice:** VPC design, CIDR planning, Terraform modules and variables.
   - **Done when:** `apply` and `destroy` both run cleanly and your diagram matches the deployed resources.
2. **Secure access and traffic control** (Intermediate, ~1 week)
   - **Build:** add security groups, NACLs, SSM access with no bastion, VPC endpoints and flow logs, with a test table.
   - **Practice:** security groups vs NACLs, private connectivity, logging.
   - **Done when:** private instances have no public path in, yet can reach required services, and flow logs prove blocked traffic.
3. **Connectivity and delivery** (Intermediate, ~1 week)
   - **Build:** a second VPC with peering, private DNS and an internal load balancer in front of two instances.
   - **Practice:** peering, routing, DNS, load balancing.
   - **Done when:** traffic is balanced across both AZs and survives the loss of one instance.

### Final project
**Time:** 3 to 4 weeks. A dev and prod network pair built from shared Terraform modules, hosting a small private app behind a load balancer, with a simulated on-premises site connected by VPN.

**Specific to this project:**
- CI on pull requests that runs `plan` and a Checkov scan, and a gated `apply`.
- Flow logs and at least three CloudWatch-style alarms (or the equivalent on your cloud).
- Monthly cost estimate, billing alert and a tested teardown command.
- A runbook for lost connectivity, a bad route change and a failed NAT.

Also meets the [production-like bar](../../README.md#what-production-like-means).
