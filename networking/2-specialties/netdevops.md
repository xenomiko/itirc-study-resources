# NetDevOps

**Role:** automates network config, validation and deployment with Python, Git and CI/CD.
**Prerequisites:** [CCNA](../1-basics/ccna.md), basic Linux.

## Skills, in order
1. Python, then Git/GitHub
2. Netmiko, NAPALM, Nornir
3. Ansible for network devices
4. APIs and data models: REST, NETCONF, YANG, JSON/YAML
5. Source of truth (NetBox) and Terraform
6. CI/CD for network changes

**Path at a glance:**
- Beginner: CS50P, then GitHub Skills.
- Intermediate: NetBox Zero to Hero, Nornir and NAPALM docs, DevNet Learning Labs.
- Advanced: pyATS for testing, Network as Code for declarative deployment.

## Resources
| Resource | Level | Cost | What it is | You will be able to |
|---|---|---|---|---|
| [CS50P: Intro to Python](https://cs50.harvard.edu/python/) | Beginner | Free | Harvard's Python course. | Write and debug Python programs. |
| [GitHub Skills](https://skills.github.com) | Beginner | Free | Interactive Git and GitHub courses. | Use branches, pull requests and basic workflows. |
| [NetBox Zero to Hero](https://netboxlabs.com/zero-to-hero/) | Beginner to Intermediate | Free | 12 hands-on modules with videos and sample data from NetBox Labs. The videos use NetBox 3.3.x, so some screens differ from current versions. | Model sites, devices, IPAM, cables and circuits, and drive them through the REST API. |
| [Kirk Byers: Python for Network Engineers](https://pynet.twb-tech.com) | Intermediate | Free + paid | Course by the creator of Netmiko and NAPALM. | Automate device access and config with Python. |
| [Nornir docs](https://nornir.readthedocs.io) with [NAPALM docs](https://napalm.readthedocs.io) | Intermediate | Free | Python automation framework with a tutorial, plus the multi-vendor library it commonly runs. | Run inventory-driven tasks across many devices and compare or deploy config. |
| [Cisco DevNet Learning Labs](https://developer.cisco.com/learning) | Intermediate | Free | Browser-based labs, modules and tracks. Needs a free account. | Practice APIs, Python, Ansible and model-driven programmability in guided labs. |
| [Ansible docs](https://docs.ansible.com) | Intermediate | Free | Official docs. See the network automation guides. | Write playbooks that configure network devices. |
| [HashiCorp Terraform tutorials](https://developer.hashicorp.com/terraform/tutorials) | Intermediate | Free | Official hands-on tutorials. | Describe infrastructure as code and apply it repeatably. |
| [David Bombal](https://www.youtube.com/@davidbombal) | Intermediate | Free | YouTube network automation videos. | See Python and Ansible applied to real gear. |
| [Network to Code blog](https://blog.networktocode.com) | Advanced | Free | Industry practices, NetBox and Nautobot content. | Learn how production automation platforms are designed. |
| [pyATS and Genie docs](https://developer.cisco.com/docs/pyats/) | Advanced | Free | Cisco's open-source test automation framework and device-output parsers. | Parse CLI output into structured data and write pre- and post-change checks. |
| [Network as Code](https://netascode.cisco.com) | Advanced | Free (support is a paid subscription) | Open-source YAML data models plus Terraform modules for Cisco IOS-XE, NX-OS, SD-WAN, Catalyst Center and Secure Firewall. | Describe device state in YAML, keep it in Git and deploy with Terraform. |

**Browse more:** [Awesome Network Automation](https://github.com/networktocode/awesome-network-automation) is a large curated index for discovering tools.

## Certifications
Cisco's automation certification track and HashiCorp Terraform Associate. A strong GitHub portfolio matters more.

## Project

### Tutorial projects
Each project takes about a week (roughly 8 to 12 hours) and covers several skills from the list above. Do them in order, and keep each one in its own Git repo or folder.

1. **Inventory-driven collector** (Beginner, ~1 week)
   - **Build:** a Python CLI that reads a YAML inventory, collects `show` output from lab devices with Netmiko, parses it to JSON and writes a CSV report.
   - **Practice:** Python packaging, Netmiko, YAML/JSON, Git, unit tests.
   - **Done when:** it runs from a clean virtual environment against three devices and has tests for the parser.
2. **Config management with Ansible** (Intermediate, ~1 week)
   - **Build:** Ansible roles with Jinja2 templates for a baseline (NTP, syslog, users, banners), check mode, automatic backups committed to Git and Ansible Vault for secrets.
   - **Practice:** Ansible, templating, idempotency, secrets handling.
   - **Done when:** a second run changes nothing and a manual change on a device is detected by check mode.
3. **Source of truth** (Intermediate, ~1 week)
   - **Build:** model your lab in NetBox (follow Zero to Hero), then generate device configs from its REST API and deploy them with Nornir and NAPALM.
   - **Practice:** NetBox, REST APIs, Nornir, NAPALM, config diff and replace.
   - **Done when:** editing a value in NetBox and rerunning produces a reviewed diff and a successful deployment.
4. **Validation and CI** (Advanced, ~1 week)
   - **Build:** pre- and post-change checks with pyATS or Nornir, run by GitHub Actions on every pull request, with lint and template-render tests.
   - **Practice:** pyATS, CI/CD, testing, rollback.
   - **Done when:** a deliberately bad change is blocked by the pipeline.

### Final project
**Time:** 3 to 4 weeks. A network-as-code platform for a virtual lab: a pull request changes data, CI renders and validates configs, and a deployment job applies them with automatic rollback.

**Specific to this project:**
- NetBox or YAML data as the single source of truth, with schema checks on the data.
- Staged pipeline: lint, render, deploy to a staging lab, run post-change checks, then promote.
- Nightly drift detection that opens an issue when a device differs from the source of truth.
- A postmortem for a bad change you introduced on purpose, showing how the pipeline caught or missed it.

Also meets the [production-like bar](../../README.md#what-production-like-means).
