# NetDevOps

## What this role does
Treats the network as code: automates configuration, validation, and deployment with Python, Git, and CI/CD instead of typing commands device by device. Network engineers who can code are in strong demand.

## Prerequisites
Finish [CCNA](../1-basics/ccna.md). You need to understand the network before you automate it. Basic Linux and the command line are required.

## Skills to learn, in order
1. Python fundamentals
2. Git and GitHub workflows
3. Network automation libraries: Netmiko, NAPALM, Nornir
4. Ansible for network devices
5. APIs and data models: REST, NETCONF/RESTCONF, YANG, JSON/YAML
6. Source of truth and IaC: NetBox, Terraform, templating with Jinja2
7. CI/CD pipelines that test and deploy network changes

## Resources
| Resource | Type | Level | Free/Paid | Notes |
|---|---|---|---|---|
| [Automate the Boring Stuff with Python](https://automatetheboringstuff.com) | Online book | Beginner | Free | Best free start for Python if you're new to coding. |
| [Pro Git](https://git-scm.com/book) | Online book | Beginner | Free | The official Git book. |
| Kirk Byers, Python for Network Engineers | Free course | Intermediate | Free | Created by the author of Netmiko and NAPALM. Search for the current course page. |
| [Netmiko](https://github.com/ktbyers/netmiko) / [NAPALM](https://napalm.readthedocs.io) / [Nornir](https://nornir.readthedocs.io) | Libraries/docs | Intermediate | Free | The core Python toolkit. Read the docs and examples. |
| [Ansible documentation](https://docs.ansible.com) | Docs | Intermediate | Free | See the network automation guides. |
| [Cisco DevNet](https://developer.cisco.com) | Learning labs + sandboxes | Intermediate | Free | Free sandboxes with real and virtual devices. |
| [NetBox](https://github.com/netbox-community/netbox) | Tool | Intermediate | Free | The standard open source source-of-truth. Run it in a container. |
| [Containerlab](https://containerlab.dev) | Lab tool | Intermediate | Free | Build test topologies you can tear down and recreate from code. |
| Packet Pushers Network Automation Nerds | Podcast/community | Intermediate | Free | Practitioner discussions. |
| Jason Edelman et al., *Network Programmability and Automation* (O'Reilly) | Book | Intermediate | Paid | Solid overview of the field. |

## Certifications
Cisco's automation track (previously DevNet Associate, now under the CCNA Automation name as far as I know, so verify) and HashiCorp Terraform Associate. A strong GitHub portfolio matters more than either.

## Project to build
A Git repo where a pull request changes the intended config of a virtual lab network, a pipeline validates it, and Ansible or Nornir deploys it. Include rollback and a short README.
