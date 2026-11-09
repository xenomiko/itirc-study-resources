# Offensive Security

**Role:** finds and safely demonstrates weaknesses in systems with authorization, then reports them.
**Prerequisites:** [Fundamentals](../1-basics/fundamentals.md) and [networking fundamentals](../../networking/1-basics/fundamentals.md). For web targets also see [Web Application Security](web-application-security.md).

## Skills, in order
1. Recon and scanning (Nmap)
2. Service enumeration
3. Exploitation with Metasploit and manual methods
4. Linux and Windows privilege escalation
5. Post-exploitation and basic Active Directory
6. Mapping findings to MITRE ATT&CK
7. Reporting

**Path at a glance:**
- Beginner: Kali docs and Nmap docs, then HTB Starting Point and TryHackMe Jr Penetration Tester.
- Intermediate: Metasploitable, HTB Academy modules, ATT&CK mapping.
- Advanced: privilege escalation references, retired HTB machines, cert prep.

**Safety:** test only systems you own or are authorized to test. Never expose Metasploitable to a real network.

## Resources
| Resource | Level | Cost | What it is | You will be able to |
|---|---|---|---|---|
| [Nmap Reference Guide](https://nmap.org/book/man.html) | Beginner | Free | Official reference for scan types, scripts and output. | Choose the right scan and interpret open ports and services. |
| [Hack The Box: Starting Point](https://www.hackthebox.com/starting-point) | Beginner | Free tier + paid | Guided machines in tiers with step-by-step questions. Higher tiers may need a subscription. | Enumerate and exploit simple targets end to end. |
| [TryHackMe: Jr Penetration Tester](https://tryhackme.com) | Beginner to Intermediate | Free tier + paid | Guided path through methodology, web, exploitation and privilege escalation. Much of it is premium. | Follow a full pentest workflow on practice targets. |
| [Metasploitable 2](https://docs.rapid7.com/metasploit/metasploitable-2/) | Beginner to Intermediate | Free | Intentionally vulnerable VM for legal local practice. | Scan, exploit and document attacks on a local target. |
| [Hack The Box Academy](https://academy.hackthebox.com) | Intermediate | Free tier + paid | Interactive modules on methodology and tools, with hands-on targets. Advanced modules may need paid access. | Apply enumeration and exploitation techniques in structured labs. |
| [MITRE ATT&CK](https://attack.mitre.org) | Intermediate | Free | Knowledge base of adversary tactics and techniques. | Describe attacks as ATT&CK techniques in reports and detections. |
| [GTFOBins](https://gtfobins.github.io) | Intermediate | Free | Supplementary: reference of Unix binaries usable for privilege escalation. | Find escalation paths from misconfigured binaries. |
| [LOLBAS](https://lolbas-project.github.io) | Intermediate to Advanced | Free | Supplementary: reference of living-off-the-land Windows binaries. | Recognize and use built-in Windows tools for execution and bypass. |

## Certifications
eJPT (entry), PNPT (practical), then OSCP. Verify current formats and prices.

## Project

### Tutorial projects
Each project takes about a week (roughly 8 to 12 hours) and covers several skills from the list above. Do them in order, and keep each one in its own Git repo or folder. Test only isolated machines you own.

1. **Recon and enumeration** (Beginner, ~1 week)
   - **Build:** an enumeration report for Metasploitable 2 and one more practice VM using Nmap scan types, service and version detection and script scans.
   - **Practice:** scanning, enumeration, note-taking, scope.
   - **Done when:** the report lists every service with evidence, likely weaknesses and the commands used.
2. **Exploitation methodology** (Beginner to Intermediate, ~1 week)
   - **Build:** three Starting Point machines plus two Metasploitable services, each exploited once with Metasploit and once manually.
   - **Practice:** exploitation, manual methods, tool trade-offs, write-ups.
   - **Done when:** each write-up could be followed by someone else to reproduce the foothold.
3. **Privilege escalation and post-exploitation** (Intermediate, ~1 week)
   - **Build:** Linux and Windows privilege escalation on practice machines with HTB Academy modules, using GTFOBins and LOLBAS, plus a pivot between two VMs.
   - **Practice:** privilege escalation, post-exploitation, pivoting, ATT&CK mapping.
   - **Done when:** each chain is mapped to ATT&CK techniques and lists the misconfiguration behind every step.

### Final project
**Time:** 3 to 4 weeks. An engagement-style penetration test of a small environment you build yourself (three to five VMs, including a vulnerable web app and a Windows or Linux server).

**Specific to this project:**
- Rules of engagement, scope and a test plan written before you start.
- Findings rated with CVSS, each with evidence, impact and a fix.
- An executive summary, a technical report and an ATT&CK mapping.
- Fix the top findings, retest, and show before and after results. Clean up everything you installed.

Also meets the [production-like bar](../../README.md#what-production-like-means).
