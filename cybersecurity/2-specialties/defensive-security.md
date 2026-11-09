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

### Tutorial projects
Each project takes about a week (roughly 8 to 12 hours) and covers several skills from the list above. Do them in order, and keep each one in its own Git repo or folder. Run attack tests only in a lab VM.

1. **SOC analyst week** (Beginner, ~1 week)
   - **Build:** triage ten LetsDefend alerts with ticket-style notes, then write a triage playbook with escalation criteria.
   - **Practice:** alert triage, escalation, investigation notes, case management.
   - **Done when:** every alert has a verdict, evidence and a next step, and the playbook covers the alert types you saw.
2. **Log search and dashboards** (Beginner to Intermediate, ~1 week)
   - **Build:** ingest sample logs into Splunk, write searches for failed logins, rare processes and data transfers, and build a dashboard with one alert.
   - **Practice:** log sources, SPL, visualization, alerting.
   - **Done when:** each search has a documented purpose and a test showing it finds the event.
3. **Detection engineering** (Intermediate, ~1 week)
   - **Build:** a Wazuh lab with two endpoints, five Sigma-style detections for ATT&CK techniques, and Atomic Red Team tests for each.
   - **Practice:** Wazuh, Sigma, ATT&CK, testing detections.
   - **Done when:** a table shows each technique, the test run, whether it was detected and how you tuned it.
4. **Full investigation** (Intermediate, ~1 week)
   - **Build:** solve a CyberDefenders challenge end to end and write an incident report with timeline, indicators and containment advice.
   - **Practice:** investigation, incident response lifecycle, reporting.
   - **Done when:** the report can be handed to a manager with no extra explanation.

### Final project
**Time:** 3 to 4 weeks. A mini SOC: Wazuh or Security Onion monitoring three endpoints (Windows and Linux), with detections kept as code and a simulated incident handled from alert to report.

**Specific to this project:**
- Ten detections mapped to ATT&CK, stored in Git and tested by CI where possible, with a coverage matrix.
- True and false positive counts per rule, and what you changed to improve them.
- Three incident response playbooks and one simulated multi-stage attack with a timeline and report.
- Alert routing to a notification channel you can show working.

Also meets the [production-like bar](../../README.md#what-production-like-means).
