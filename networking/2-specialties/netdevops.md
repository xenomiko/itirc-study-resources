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
A Git repo where a pull request changes a virtual lab's config, a pipeline validates it (pyATS or Nornir checks), and Ansible or Nornir deploys it, with rollback.
