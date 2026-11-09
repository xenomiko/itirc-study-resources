# Network Security

**Role:** protects networks with firewalls, VPNs, segmentation and monitoring, and detects attacks.
**Prerequisites:** [CCNA](../1-basics/ccna.md) or solid fundamentals plus Wireshark.

## Skills, in order
1. Security fundamentals and threat models
2. Firewalls and segmentation
3. VPNs: IPsec, WireGuard
4. Traffic analysis
5. IDS/IPS: Suricata, Zeek
6. Logging, SIEM, incident response basics
7. Hardening: 802.1X, port security, DHCP snooping

**Path at a glance:**
- Beginner: Professor Messer Security+, then the free TryHackMe traffic-analysis rooms.
- Intermediate: OPNsense lab, Suricata docs, Malware-Traffic-Analysis exercises.
- Advanced: Zeek docs, then Security Onion to run it all together.

**Safety:** malware pcaps and forensic files belong in an isolated VM with no shared folders.

## Resources
| Resource | Level | Cost | What it is | You will be able to |
|---|---|---|---|---|
| [Professor Messer Security+](https://www.professormesser.com) | Beginner | Free | Video course for the Security+ exam. | Cover the Security+ syllabus. |
| [TryHackMe: Network Security and Traffic Analysis](https://tryhackme.com/r/module/network-security-and-traffic-analysis) | Beginner to Intermediate | Free tier + paid | Guided modules. Traffic Analysis Essentials and Snort are free. The Wireshark: Traffic Analysis room is premium. | Spot scans and anomalies in traffic and write simple IDS alerts. |
| [OPNsense docs](https://docs.opnsense.org) | Intermediate | Free | Documentation for an open-source firewall and routing platform. Release 26.1 redesigned the firewall rules interface, so older tutorials show different screens. | Deploy a firewall in a VM with segmentation, VPN and IDS. |
| [Suricata docs](https://docs.suricata.io) | Intermediate | Free | User guide covering rules, rule management, IPS mode and a chapter on public pcap datasets. | Write and tune IDS rules and test them against sample traffic. |
| [Malware-Traffic-Analysis.net](https://www.malware-traffic-analysis.net/training-exercises.html) | Intermediate to Advanced | Free | Real-world traffic analysis exercises with pcaps and answers. Start with the most recent ones, since older ones reflect an outdated threat landscape. | Investigate an infection from a pcap and write up what happened. |
| [Fortinet Training Institute](https://training.fortinet.com) | Intermediate | Free | Entry-level NSE courses. | Understand firewall concepts through a major vendor's lens. |
| [Cisco CyberOps via NetAcad](https://www.netacad.com) | Intermediate | Free | Detection and response from the vendor side. | Follow a SOC-style detection and response workflow. |
| [TCM Security Academy](https://academy.tcm-sec.com) | Intermediate | Paid | Low-cost practical courses. | Apply security skills in hands-on scenarios. |
| [Zeek docs](https://docs.zeek.org) | Advanced | Free | Documentation for a network analysis framework. Choose the current or LTS docs to match your install. | Turn raw traffic into structured logs and hunt through them. |
| [Security Onion docs](https://docs.securityonion.net) | Advanced | Free (Pro edition is paid) | Docs for a free monitoring platform covering network and host visibility, intrusion detection and case management. It is resource-hungry, so size your VM generously. | Deploy a monitoring stack and triage alerts end to end. |

## Certifications
CompTIA Security+, then Cisco CyberOps, CCNP Security, or Fortinet NSE 4.

## Project

### Tutorial projects
Each project takes about a week (roughly 8 to 12 hours) and covers several skills from the list above. Do them in order, and keep each one in its own Git repo or folder.

1. **Traffic analysis case file** (Beginner, ~1 week)
   - **Build:** analyze three captures (a port scan, cleartext credentials, a beaconing host) using Wireshark and the TryHackMe traffic rooms, and write a case file for each.
   - **Practice:** protocols, display filters, baselines, writing findings.
   - **Done when:** each case file names the hosts, timeline, evidence packets and a recommended control.
2. **Segmented firewall** (Intermediate, ~1 week)
   - **Build:** an OPNsense VM with users, servers and DMZ networks, DHCP and DNS, NAT, default-deny rules and logging.
   - **Practice:** firewall policy, segmentation, NAT, logging.
   - **Done when:** a test table shows every allowed and blocked flow and the logs prove it.
3. **VPN and IDS** (Intermediate, ~1 week)
   - **Build:** add a WireGuard VPN and Suricata to the firewall, write custom rules and replay pcaps through it.
   - **Practice:** VPNs, IDS rules, tuning, false positives.
   - **Done when:** three custom rules fire on test traffic, and you tuned away at least one false positive.
4. **Detection pipeline** (Advanced, ~1 week)
   - **Build:** run Zeek on the lab traffic and send Suricata and Zeek output to Security Onion (or another log stack), then hunt through a recent Malware-Traffic-Analysis pcap in an isolated VM.
   - **Practice:** Zeek logs, hunting, alert triage.
   - **Done when:** your hunt write-up reconstructs the infection timeline from the logs.

### Final project
**Time:** 3 to 4 weeks. A secure small-office network: segmentation, VPN, IPS, hardened rules and central logging, defended against simulated attacks.

**Specific to this project:**
- Exported, versioned firewall and IDS configs, plus a tested restore from backup.
- Attack simulation from a separate attacker VM (scans and replayed malicious traffic), with a detection table showing what was caught.
- Alert runbook for three alert types and a one-page incident report for one simulated attack.
- A hardening checklist applied and verified.

Also meets the [production-like bar](../../README.md#what-production-like-means).
