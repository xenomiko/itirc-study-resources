# Cloud Security

**Role:** secures identities, workloads, data and configurations in AWS, Azure or GCP.
**Prerequisites:** [Cloud networking](../networking/2-specialties/cloud-networking.md) and [fundamentals](fundamentals.md). Pick one cloud first.

**Cost warning:** use a dedicated sandbox account, set billing alerts before any lab, and destroy resources when finished. Never run vulnerable-by-design scenarios in an account with real data.

## Skills, in order
1. Shared responsibility and identity (IAM)
2. Logging and monitoring
3. Storage and data exposure
4. Infrastructure-as-code scanning
5. Cloud posture auditing
6. Attack paths and remediation
7. Kubernetes risks

**Path at a glance:**
- Beginner: Microsoft Learn security fundamentals or AWS Skill Builder security content.
- Intermediate: Checkov on your Terraform, Prowler audits, Google Cloud security docs.
- Advanced: CloudGoat scenarios, then remediate them.

## Resources
| Resource | Level | Priority | Cost | What it is | You will be able to |
|---|---|---|---|---|---|
| [Microsoft Learn: Security](https://learn.microsoft.com/training/) | Beginner | Essential | Free | Learning paths covering security, identity and compliance fundamentals. | Explain core cloud security and identity concepts. |
| [AWS Skill Builder: Security learning](https://skillbuilder.aws) | Beginner to Intermediate | Essential | Free + paid (check which courses are free) | AWS security courses and learning plans. | Explain IAM, encryption and logging on AWS. |
| [Checkov documentation](https://www.checkov.io) | Intermediate | Essential | Free | Open-source scanner for Terraform, CloudFormation, Kubernetes and more. | Find and fix misconfigurations before deployment. |
| [Prowler documentation](https://docs.prowler.com) | Intermediate | Essential | Free (open source) | Auditing tool for AWS, Azure, GCP and Kubernetes. | Audit an account against benchmarks and prioritize findings. |
| [Google Cloud security documentation](https://cloud.google.com/docs/security) | Intermediate | Supplementary | Free | Official reference for GCP security features. | Apply IAM, logging and network controls on Google Cloud. |
| [OWASP Kubernetes Top 10](https://owasp.org/www-project-kubernetes-top-ten/) | Intermediate | Supplementary | Free | Ranked Kubernetes risks. | Recognize common cluster misconfigurations. |
| [CloudGoat](https://github.com/RhinoSecurityLabs/cloudgoat) | Intermediate to Advanced | Essential | Free tool, cloud costs apply | Deploys vulnerable-by-design AWS scenarios. | Exploit IAM attack paths, then fix them. |

## Certifications
AWS Security Specialty, Azure SC-900 then AZ-500, Google Professional Cloud Security Engineer. Verify current exams.

## Project
Take the Terraform VPC from the [cloud networking project](../networking/2-specialties/cloud-networking.md), scan it with Checkov, fix the findings, then audit with Prowler. Write a short before/after note.
