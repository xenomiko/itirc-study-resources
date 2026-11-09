# Data Platform Engineer

**Role:** designs and runs the cloud infrastructure behind warehouses and lakehouses, including security, cost and deployment automation.
**Prerequisites:** [Data Engineer](data-engineer.md) and [Cloud Networking](../../networking/2-specialties/cloud-networking.md). Pick one cloud first.

## Skills, in order
1. Cloud storage, IAM and networking basics
2. Warehouse concepts: partitioning, clustering, cost models
3. Lakehouse architecture and table formats
4. Infrastructure as code with Terraform
5. CI/CD for data code
6. Containers and Kubernetes basics
7. Security, access control and cost governance

**Path at a glance:**
- Beginner: the cloud fundamentals and Terraform tutorials in the [cloud networking roadmap](../../networking/2-specialties/cloud-networking.md).
- Intermediate: your chosen cloud's data engineering path and a vendor lakehouse course.
- Advanced: Kubernetes, GitHub Actions deployments and cost optimization.

**Cost warning:** set billing alerts before any lab, use a dedicated sandbox account, and destroy resources when finished.

## Resources
| Resource | Level | Cost | What it is | You will be able to |
|---|---|---|---|---|
| [Terraform tutorials](https://developer.hashicorp.com/terraform/tutorials) | Beginner to Intermediate | Free | Official hands-on tutorials. Also listed in the [networking roadmap](../../networking/2-specialties/netdevops.md). | Provision storage, warehouses and IAM from code. |
| [Google Cloud Skills Boost: Data Engineering](https://www.cloudskillsboost.google) | Intermediate | Free + paid (labs may use credits) | Learning paths for BigQuery, Dataflow and Pub/Sub. Check which are free. | Build and secure a warehouse pipeline on Google Cloud. |
| [AWS Skill Builder: Data Engineering](https://skillbuilder.aws) | Intermediate | Free + paid | Learning plans on Glue, S3, Redshift and Athena. Check which courses are free. | Design a lake and warehouse architecture on AWS. |
| [Microsoft Learn: Fabric data engineering](https://learn.microsoft.com/training/) | Intermediate | Free | Learning paths for Microsoft Fabric. Verify the current path names. | Build lakehouse pipelines on Microsoft Fabric. |
| [Databricks Academy](https://www.databricks.com/learn) | Intermediate | Free + paid | Self-paced lakehouse courses. Check which are free. | Operate a lakehouse with governance and jobs. |
| [Snowflake documentation and quickstarts](https://docs.snowflake.com) | Intermediate | Free docs, trial account needed | Warehouse docs plus [quickstarts](../1-basics/labs-and-tools.md). | Load data, manage roles and control warehouse cost. |
| [GitHub Actions documentation](https://docs.github.com/en/actions) | Intermediate | Free (usage limits apply) | Official docs for CI/CD workflows. | Test and deploy data code automatically. |
| [Kubernetes documentation](https://kubernetes.io/docs/tutorials/) | Intermediate to Advanced | Free | Supplementary: official tutorials, useful for running Airflow, Spark or Kafka. | Deploy and inspect a workload on a local cluster. |
| [Cloud cost tools: Infracost docs](https://www.infracost.io/docs/) | Advanced | Free (open source) + paid | Supplementary: shows cost estimates for Terraform changes. | Review the cost impact of an infrastructure change in a pull request. |

## Certifications
AWS Certified Data Engineer Associate, Google Professional Data Engineer, Microsoft Fabric Data Engineer Associate, SnowPro Core. Verify current exams, names and prices.

## Project

### Tutorial projects
Each project takes about a week (roughly 8 to 12 hours) and covers several skills from the list above. Do them in order, and keep each one in its own Git repo or folder. Set billing alerts first, use a sandbox account and destroy resources afterwards.

1. **Platform foundations** (Beginner to Intermediate, ~1 week)
   - **Build:** Terraform that creates a bucket, a warehouse dataset or schema and IAM roles, with variables, remote or local state and outputs.
   - **Practice:** cloud storage, IAM, Terraform, networking basics.
   - **Done when:** `apply` and `destroy` work from a clean checkout and the roles follow least privilege.
2. **Warehouse design and cost control** (Intermediate, ~1 week)
   - **Build:** load a large public dataset into the BigQuery sandbox (or a trial warehouse), compare partitioned and clustered tables, and set budgets and query limits.
   - **Practice:** partitioning, clustering, cost models, governance.
   - **Done when:** a table compares bytes scanned and cost across three layouts.
3. **CI/CD for infrastructure** (Intermediate, ~1 week)
   - **Build:** GitHub Actions that run `fmt`, `validate` and `plan` on pull requests and apply to dev after approval, with Infracost as an optional extra.
   - **Practice:** CI/CD, environments, approvals, cost review.
   - **Done when:** a pull request shows the plan, and a bad change is blocked.

### Final project
**Time:** 3 to 4 weeks. A multi-environment data platform (dev and prod) built from Terraform modules, with personas for engineers, analysts and a service account.

**Specific to this project:**
- Separate least-privilege roles per persona, with a test that proves what each can and cannot do.
- CI/CD with plan comments, gated apply and drift detection.
- Budgets, alerts, audit logging and a restore test for critical data.
- A diagram, cost note and a one-command teardown.

Also meets the [production-like bar](../../README.md#what-production-like-means).
