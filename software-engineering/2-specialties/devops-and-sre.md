# DevOps and SRE

**Role:** automates building, testing, deploying and running software, and keeps services reliable.
**Prerequisites:** [Programming basics](../1-basics/programming-basics.md), Linux (see [Linux Journey](../../cybersecurity/1-basics/fundamentals.md)) and [networking fundamentals](../../networking/1-basics/fundamentals.md).

## Skills, in order
1. Linux administration and shell scripting
2. Git workflows and CI/CD
3. Containers: Docker
4. Kubernetes
5. Infrastructure as code: Terraform, Ansible
6. Monitoring, logging and alerting
7. Incident response, SLOs and postmortems
8. Security in the pipeline

**Path at a glance:**
- Beginner: Missing Semester and Docker Get Started, then GitHub Actions docs.
- Intermediate: Kubernetes tutorials via Killercoda, [Terraform tutorials](../../networking/2-specialties/netdevops.md), Prometheus and Grafana docs.
- Advanced: Kubernetes the Hard Way, Argo CD and GitOps, SLO design, chaos experiments.

**Cost warning:** set billing alerts before any lab, use a sandbox account, and destroy resources when finished.

## Resources
| Resource | Level | Cost | What it is | You will be able to |
|---|---|---|---|---|
| [GitHub Actions documentation](https://docs.github.com/en/actions) | Beginner to Intermediate | Free (usage limits apply) | Official docs for CI/CD workflows. | Build pipelines that test, build and deploy on every push. |
| [Docker: Get started](https://docs.docker.com/get-started/) | Beginner | Free | Also in [data engineering](../../data-engineering/1-basics/fundamentals.md). | Containerize an app and run it with Compose. |
| [Kubernetes tutorials](https://kubernetes.io/docs/tutorials/) | Intermediate | Free | Official tutorials. Also listed in the [data platform roadmap](../../data-engineering/2-specialties/data-platform-engineer.md). | Deploy, scale and update workloads on a cluster. |
| [Killercoda](https://killercoda.com) | Beginner to Intermediate | Free + paid | Browser-based interactive labs for Kubernetes, Linux and more. Check which scenarios are free. | Practice Kubernetes tasks in a disposable cluster. |
| [Terraform tutorials](https://developer.hashicorp.com/terraform/tutorials) | Intermediate | Free | Official hands-on tutorials. | Describe infrastructure as code and apply it repeatably. |
| [Ansible documentation](https://docs.ansible.com) | Intermediate | Free | Also in [NetDevOps](../../networking/2-specialties/netdevops.md). | Configure servers with playbooks. |
| [Prometheus](https://prometheus.io/docs/) and [Grafana](https://grafana.com/docs/) docs | Intermediate | Free (open source) | Metrics collection, alerting and dashboards. | Instrument a service and alert on latency and errors. |
| [OpenTelemetry documentation](https://opentelemetry.io/docs/) | Intermediate to Advanced | Free | Also in [Backend Engineer](backend-engineer.md). | Collect traces and metrics across services. |
| [Argo CD documentation](https://argo-cd.readthedocs.io) | Advanced | Free | Official docs for GitOps deployment to Kubernetes. | Deploy from Git with automatic drift detection. |
| [Kubernetes the Hard Way](https://github.com/kelseyhightower/kubernetes-the-hard-way) | Advanced | Free | Step-by-step cluster bootstrapping guide. Needs a cloud account, so watch costs. | Understand each component a cluster is built from. |
| [Trivy documentation](https://trivy.dev/latest/docs/) | Intermediate | Free (open source) | Supplementary: scanner for container images, dependencies and IaC. See also Checkov in [cloud security](../../cybersecurity/2-specialties/cloud-security.md). | Add vulnerability scanning to a pipeline. |
| [DevOps Exercises](https://github.com/bregman-arie/devops-exercises) | Intermediate | Free | Supplementary: question bank across Linux, Kubernetes, CI and more. | Test your knowledge and find gaps. |

## Certifications
Certified Kubernetes Administrator (CKA), HashiCorp Terraform Associate, AWS Solutions Architect Associate. Verify current exams and prices.

## Project

### Tutorial projects
Each project takes about a week (roughly 8 to 12 hours) and covers several skills from the list above. Do them in order, and keep each one in its own Git repo or folder. Use a sandbox account, set billing alerts and destroy resources afterwards.

1. **Containers and CI/CD** (Beginner to Intermediate, ~1 week)
   - **Build:** a small app with a Dockerfile, a Compose setup and a GitHub Actions pipeline that tests, scans with Trivy, builds and pushes an image.
   - **Practice:** Linux, Git workflows, Docker, CI/CD, pipeline security.
   - **Done when:** a failing test or a vulnerable image blocks the pipeline.
2. **Infrastructure and Kubernetes** (Intermediate, ~1 week)
   - **Build:** Terraform for an environment and a Kubernetes deployment with config, secrets, scaling and a rolling update, using Killercoda or a local cluster.
   - **Practice:** Terraform, Kubernetes, configuration management.
   - **Done when:** you can scale, update and roll back the deployment without downtime.
3. **Observability and reliability** (Intermediate to Advanced, ~1 week)
   - **Build:** Prometheus and Grafana dashboards, an SLO with an alert, and a controlled failure experiment.
   - **Practice:** monitoring, alerting, SLOs, incident response.
   - **Done when:** the experiment fires your alert and you write a short postmortem.

### Final project
**Time:** 3 to 4 weeks. A GitOps platform for a small multi-service app: Terraform infrastructure, Kubernetes deployments through Argo CD, and staged environments.

**Specific to this project:**
- Pipeline that tests, scans, builds and promotes images from staging to production by pull request.
- SLO dashboards with an alert on error budget burn, and a tested rollback.
- Secrets handled outside Git and least-privilege access for the pipeline.
- An incident drill with a written postmortem, plus a cost note and teardown.

Also meets the [production-like bar](../../README.md#what-production-like-means).
