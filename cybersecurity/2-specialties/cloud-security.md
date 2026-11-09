# Cloud Security

**Role:** secures identities, workloads, data and configurations in AWS, Azure or GCP.
**Prerequisites:** [Cloud Networking](../../networking/2-specialties/cloud-networking.md) and [Fundamentals](../1-basics/fundamentals.md). Pick one cloud first.

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
- Compliance angle: see [GRC](grc.md) for frameworks and the CSA Cloud Controls Matrix.

**Cost warning:** use a dedicated sandbox account, set billing alerts before any lab, and destroy resources when finished. Never run vulnerable-by-design scenarios in an account with real data.

## Resources
| Resource | Level | Cost | What it is | You will be able to |
|---|---|---|---|---|
| [Microsoft Learn: Security](https://learn.microsoft.com/training/) | Beginner | Free | Learning paths covering security, identity and compliance fundamentals. | Explain core cloud security and identity concepts. |
| [AWS Skill Builder: Security learning](https://skillbuilder.aws) | Beginner to Intermediate | Free + paid | AWS security courses and learning plans. Check which courses are free. | Explain IAM, encryption and logging on AWS. |
| [Checkov documentation](https://www.checkov.io) | Intermediate | Free | Open-source scanner for Terraform, CloudFormation, Kubernetes and more. | Find and fix misconfigurations before deployment. |
| [Prowler documentation](https://docs.prowler.com) | Intermediate | Free (open source) | Auditing tool for AWS, Azure, GCP and Kubernetes. | Audit an account against benchmarks and prioritize findings. |
| [Google Cloud security documentation](https://cloud.google.com/docs/security) | Intermediate | Free | Supplementary: official reference for GCP security features. | Apply IAM, logging and network controls on Google Cloud. |
| [OWASP Kubernetes Top 10](https://owasp.org/www-project-kubernetes-top-ten/) | Intermediate | Free | Supplementary: ranked Kubernetes risks. | Recognize common cluster misconfigurations. |
| [CloudGoat](https://github.com/RhinoSecurityLabs/cloudgoat) | Intermediate to Advanced | Free tool, cloud costs apply | Deploys vulnerable-by-design AWS scenarios. | Exploit IAM attack paths, then fix them. |

## Certifications
AWS Security Specialty, Azure SC-900 then AZ-500, Google Professional Cloud Security Engineer. Verify current exams.

## Project

### Tutorial projects
Each project takes about a week (roughly 8 to 12 hours) and covers several skills from the list above. Do them in order, and keep each one in its own Git repo or folder. Use a sandbox account with billing alerts, and destroy resources when finished.

1. **Identity and logging baseline** (Beginner to Intermediate, ~1 week)
   - **Build:** least-privilege roles, MFA, audit logging to a protected bucket, and alerts for root or console logins.
   - **Practice:** IAM, logging, monitoring, shared responsibility.
   - **Done when:** an allowed action works, a denied one fails, and your own test login triggers an alert.
2. **Secure infrastructure pipeline** (Intermediate, ~1 week)
   - **Build:** Terraform for a small workload with Checkov running in GitHub Actions. Fix findings and keep a documented exception list.
   - **Practice:** IaC scanning, storage exposure, CI gating.
   - **Done when:** a pull request with an insecure change is blocked and a fixed one passes.
3. **Posture audit and attack path** (Intermediate to Advanced, ~1 week)
   - **Build:** audit the sandbox with Prowler, triage the top findings, then exploit one CloudGoat scenario and remediate it.
   - **Practice:** posture auditing, attack paths, remediation, prioritization.
   - **Done when:** the CloudGoat attack no longer works and the Prowler report shows the related finding closed.

### Final project
**Time:** 3 to 4 weeks. A secure account baseline in Terraform (logging, IAM roles, encrypted storage, private networking) with continuous checks and one deliberate misconfiguration found and fixed.

**Specific to this project:**
- CI gating with Checkov and a scheduled Prowler run that stores its report.
- Alert rules for risky events and an incident runbook for leaked credentials.
- A before and after risk report ranking findings by impact.
- Everything deployable and destroyable from code.

Also meets the [production-like bar](../../README.md#what-production-like-means).
