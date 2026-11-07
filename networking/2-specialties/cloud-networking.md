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
Terraform VPC with public and private subnets, NAT gateway, bastion or SSM access, and a VPN or peering to a second VPC. Include a diagram and a cost note.
