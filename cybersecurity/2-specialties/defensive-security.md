# Defensive Security (Blue Team, SOC, Incident Response)

**Role:** monitors, detects, investigates and responds to security incidents.
**Prerequisites:** [Fundamentals](../1-basics/fundamentals.md) and [Network Security](network-security.md).

## Skills, in order
1. Log sources and basic SIEM searching
2. Alert triage and escalation
3. Endpoint monitoring
4. Detection rules and ATT&CK coverage
5. Incident response lifecycle
6. Reporting and lessons learned

**Path at a glance:**
- Beginner: LetsDefend or Blue Team Labs Online for SOC-style practice, plus Splunk training.
- Intermediate: Wazuh lab, Security Onion, CyberDefenders challenges, Sigma rules.
- Advanced: Atomic Red Team to test your detections, Splunk BOTS datasets.
- Also use: [MITRE ATT&CK](https://attack.mitre.org) to organize detections and [Security Onion](../../networking/2-specialties/network-security.md) for network monitoring.

**Safety:** run Atomic Red Team tests and attack datasets only in a lab VM.

## Resources
| Resource | Level | Cost | What it is | You will be able to |
|---|---|---|---|---|
| [LetsDefend](https://letsdefend.io) | Beginner | Free tier + paid | Browser SOC simulator with alert queues and case management. | Triage alerts and write investigation notes like an analyst. |
| [Blue Team Labs Online](https://blueteamlabs.online) | Beginner to Intermediate | Free + paid | Challenges in investigation, forensics and threat intel. | Investigate incidents from logs and artifacts. |
| [Splunk training and security resources](https://www.splunk.com/en_us/training.html) | Beginner to Intermediate | Free + paid | Splunk's training catalog and security content. Check which courses are free. | Search, filter and visualize logs with SPL. |
| [Wazuh documentation](https://documentation.wazuh.com) | Intermediate | Free | Docs for an open-source security monitoring platform. Start with the quickstart. | Deploy a SIEM and endpoint agents and tune alerts. |
| [CyberDefenders](https://cyberdefenders.org) | Intermediate | Free + paid | Blue-team labs with real artifacts such as pcaps, logs and memory images. | Solve investigations and compare against walkthroughs. |
| [Sigma rules](https://github.com/SigmaHQ/sigma) | Intermediate | Free | Community detection rules in a vendor-neutral format. | Read, convert and write rules for your SIEM. |
| [Atomic Red Team](https://github.com/redcanaryco/atomic-red-team) | Intermediate to Advanced | Free | Supplementary: small tests mapped to ATT&CK techniques. | Verify whether your detections fire for a given technique. |
| [Splunk BOTS datasets](https://github.com/splunk/botsv3) | Advanced | Free | Supplementary: public Boss of the SOC datasets. Large downloads. | Hunt through realistic multi-stage attack data. |

## Certifications
CompTIA Security+, then CySA+ or Cisco CyberOps. Verify current versions.

## Project
Wazuh or Security Onion lab with two endpoints. Run three Atomic Red Team tests, write a Sigma rule for each, and document what was and wasn't detected.
