# Tech Roadmaps

Free-first learning roadmaps for four areas of tech. Each one goes from fundamentals to a specialty and prioritizes hands-on labs, official documentation, interactive courses and projects over passive reading.

## Roadmaps

| Roadmap | Start here | Specialties |
|---|---|---|
| [Networking](networking/README.md) | [Fundamentals](networking/1-basics/fundamentals.md) | [Infrastructure Engineer](networking/2-specialties/infrastructure-engineer.md), [NetDevOps](networking/2-specialties/netdevops.md), [Network Security](networking/2-specialties/network-security.md), [Cloud Networking](networking/2-specialties/cloud-networking.md) |
| [Cybersecurity](cybersecurity/README.md) | [Fundamentals](cybersecurity/1-basics/fundamentals.md) | [Offensive](cybersecurity/2-specialties/offensive-security.md), [Defensive](cybersecurity/2-specialties/defensive-security.md), [Web Application Security](cybersecurity/2-specialties/web-application-security.md), [Network Security](cybersecurity/2-specialties/network-security.md), [Cloud Security](cybersecurity/2-specialties/cloud-security.md), [Forensics and Malware](cybersecurity/2-specialties/forensics-and-malware.md), [GRC](cybersecurity/2-specialties/grc.md) |
| [Data Engineering](data-engineering/README.md) | [Fundamentals](data-engineering/1-basics/fundamentals.md) | [Data Engineer](data-engineering/2-specialties/data-engineer.md), [Analytics Engineer](data-engineering/2-specialties/analytics-engineer.md), [Streaming and Big Data](data-engineering/2-specialties/streaming-and-big-data.md), [Data Platform Engineer](data-engineering/2-specialties/data-platform-engineer.md), [DataOps and Data Quality](data-engineering/2-specialties/dataops-and-data-quality.md) |
| [Software Engineering](software-engineering/README.md) | [Programming basics](software-engineering/1-basics/programming-basics.md) | [Frontend](software-engineering/2-specialties/frontend-engineer.md), [Backend](software-engineering/2-specialties/backend-engineer.md), [Mobile](software-engineering/2-specialties/mobile-engineer.md), [DevOps and SRE](software-engineering/2-specialties/devops-and-sre.md), [AI Engineer](software-engineering/2-specialties/ai-engineer.md) |

## How every roadmap is laid out

1. **`1-basics/`**: what everyone in that field should learn first.
2. **`2-specialties/`**: one file per role, with the same sections each time:
   - Role and prerequisites
   - Skills, in order
   - Path at a glance (beginner, intermediate, advanced)
   - Resource table (Resource, Level, Cost, What it is, You will be able to)
   - Certifications
   - A portfolio project

Resources are essential unless their description starts with "Supplementary". Cost is marked Free, Free tier + paid, or Paid. Where a resource's free access varies, the table says to check.

## Where to start

- **New to tech:** [Programming basics](software-engineering/1-basics/programming-basics.md) and [Networking fundamentals](networking/1-basics/fundamentals.md) give you the base for everything else.
- **Security:** finish the [networking basics](networking/1-basics/fundamentals.md), then [cybersecurity fundamentals](cybersecurity/1-basics/fundamentals.md).
- **Data:** learn Python and SQL first, then [data engineering fundamentals](data-engineering/1-basics/fundamentals.md).
- **Building software or AI apps:** follow the [software engineering basics](software-engineering/README.md), then pick Backend, then [AI Engineer](software-engineering/2-specialties/ai-engineer.md).
- **Infrastructure and automation:** [NetDevOps](networking/2-specialties/netdevops.md) and [DevOps and SRE](software-engineering/2-specialties/devops-and-sre.md) overlap heavily, so do one first.

## Shared topics

To avoid duplicates, common topics live in one place and the other roadmaps link to them.

| Topic | Lives in |
|---|---|
| Python, Git, Ansible | [NetDevOps](networking/2-specialties/netdevops.md) |
| Linux, OWASP, MITRE ATT&CK | [Cybersecurity](cybersecurity/README.md) |
| Terraform and cloud basics | [Cloud Networking](networking/2-specialties/cloud-networking.md) |
| SQL, Docker and Compose | [Data Engineering basics](data-engineering/README.md) |
| Kubernetes, CI/CD, OpenTelemetry | [DevOps and SRE](software-engineering/2-specialties/devops-and-sre.md) |

## Safety and cost

- Only test systems you own or have written permission to test.
- Run malware, vulnerable VMs and attack datasets in isolated, snapshotted VMs with no shared folders.
- Set billing alerts before any cloud or API lab, use a sandbox account, and delete resources when finished.
- Keep API keys and secrets out of Git.

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md). Courses and tools change often, so corrections to links, prices, free tiers and exam versions are especially welcome.
