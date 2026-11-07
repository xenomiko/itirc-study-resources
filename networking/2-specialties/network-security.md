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
Segmented lab: OPNsense, three VLANs (users, servers, DMZ), WireGuard VPN, Suricata alerts. Replay a malware-traffic pcap through Suricata and document what was caught.
