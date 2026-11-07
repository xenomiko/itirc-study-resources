# Network Security

## What this role does
Protects networks with firewalls, VPNs, segmentation, and monitoring, and detects and responds to attacks. It overlaps with the cybersecurity domain, so link between the two.

## Prerequisites
Finish [CCNA](../1-basics/ccna.md) or at least fundamentals, VLANs, routing, and Wireshark basics.

## Skills to learn, in order
1. Security fundamentals: CIA triad, common attacks, threat models
2. Firewalls and segmentation: stateful rules, DMZs, zero trust ideas
3. VPNs: IPsec, WireGuard, remote access
4. Traffic analysis with Wireshark
5. Intrusion detection: Suricata and Zeek
6. Monitoring and incident response basics (logs, SIEM)
7. Hardening: switches, routers, protocols (802.1X, port security, DHCP snooping)

## Resources
| Resource | Type | Level | Free/Paid | Notes |
|---|---|---|---|---|
| [Professor Messer Security+](https://www.professormesser.com) | Video course | Beginner | Free | The best free path to Security+. |
| [TryHackMe](https://tryhackme.com) | Guided labs | Beginner | Free tier + paid | Pre-Security, Network Security, and SOC learning paths. |
| [OPNsense](https://opnsense.org) | Firewall | Intermediate | Free | Run it in a VM to practice real firewall, VPN, and IDS setup. |
| [Suricata](https://suricata.io) | IDS/IPS | Intermediate | Free | Official docs include rule-writing guides. |
| [Zeek](https://zeek.org) | Network monitor | Advanced | Free | Powerful network visibility and logging. |
| [Security Onion](https://securityonionsolutions.com) | Distro | Advanced | Free | Detection and monitoring platform that bundles Suricata, Zeek, and more. |
| [Fortinet training](https://training.fortinet.com) | Vendor courses | Intermediate | Free | Entry-level NSE courses are free, so check current availability. |
| Chris Sanders, *Practical Packet Analysis* | Book | Intermediate | Paid | The best book on Wireshark. |
| Chris Sanders, *Applied Network Security Monitoring* | Book | Advanced | Paid | For people heading toward SOC or detection work. |

## Certifications
CompTIA Security+ first (the current code is SY0-701 as far as I know, so verify), then vendor tracks such as Cisco CyberOps Associate or CCNP Security, or Fortinet NSE 4.

## Project to build
A segmented home lab: OPNsense firewall, three VLANs (users, servers, DMZ), a WireGuard VPN, and Suricata alerting. Then run a scan from one segment and document what the firewall and IDS caught.
