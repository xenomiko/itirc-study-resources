# GRC (Governance, Risk and Compliance)

**Role:** defines security policy, assesses and tracks risk, maps controls to standards and regulations, and prepares organizations for audits.
**Prerequisites:** [Fundamentals](fundamentals.md). Helpful: [defensive security](defensive-security.md) for incident response context and [cloud security](cloud-security.md) for cloud compliance.
**Legal:** run scanners and hardening tools only on VMs you own. Snapshot before applying any remediation.
**Legend:** *Essential* = do these. *Supplementary* = extra practice or reference.

## Skills, in order
1. Governance basics: policies, standards, procedures, roles
2. Risk assessment: assets, threats, likelihood, impact, risk register
3. Frameworks: NIST CSF 2.0, CIS Controls, NIST SP 800-53
4. Control mapping and gap analysis
5. Technical control testing: configuration audits and benchmarks
6. Privacy and regulatory basics (GDPR and local data protection law)
7. Third-party and cloud risk
8. Audit evidence, reporting and tabletop exercises

**Path at a glance:**
- Beginner: NIST CSF 2.0 and CIS Controls to learn the vocabulary, SANS policy templates to see what real policies look like.
- Intermediate: NIST RMF and the SP 800-53 catalog, then Lynis or OpenSCAP audits of your own VM, a CISO Assistant or Eramba lab, CSA CCM and a CISA tabletop.
- Advanced: ComplianceAsCode and NIST OSCAL to automate compliance, FAIR to quantify risk.

**Also use:** [MITRE ATT&CK](https://attack.mitre.org) to link controls to attacker techniques, and [Prowler](cloud-security.md), which can report results against common compliance frameworks.

## Resources
| Resource | Level | Priority | Cost | What it is | You will be able to |
|---|---|---|---|---|---|
| [NIST Cybersecurity Framework 2.0](https://www.nist.gov/cyberframework) | Beginner | Essential | Free | Official framework with a Govern function added to the core functions, plus quick-start guides and reference tools. | Describe an organization's security program in CSF terms and build a simple profile. |
| [CIS Controls](https://www.cisecurity.org/controls) | Beginner | Essential | Free (registration may be needed) | Prioritized list of defensive safeguards with implementation groups for small to large organizations. Check the current version. | Pick a sensible first set of controls for a small organization. |
| [SANS Information Security Policy Templates](https://www.sans.org/information-security-policy/) | Beginner | Essential | Free | Editable sample policies for common topics. | Draft and adapt acceptable-use, access and incident response policies. |
| [TryHackMe governance and risk rooms](https://tryhackme.com) | Beginner | Supplementary | Free tier + paid | Search the site for governance, regulation and risk management rooms. Availability and which are free change, so check. | Practice GRC concepts in a guided browser environment. |
| [NIST Risk Management Framework](https://csrc.nist.gov/projects/risk-management) | Intermediate | Essential | Free | Official process for categorizing systems, selecting, implementing and assessing controls, and authorizing operation. | Walk a system through the RMF steps and document each one. |
| [NIST SP 800-53 control catalog](https://csrc.nist.gov/pubs/sp/800/53/r5/upd1/final) | Intermediate | Essential | Free | Detailed control families with the companion assessment guidance. Use it as a reference, not a read-through. | Look up, interpret and select controls for a given risk. |
| [Lynis](https://cisofy.com/lynis/) | Intermediate | Essential | Free (open source; paid enterprise edition) | Auditing tool for Linux and Unix hosts with hardening suggestions. | Scan your own VM, interpret findings and map them to CIS controls. |
| [OpenSCAP documentation](https://www.open-scap.org) | Intermediate | Essential | Free | Scanner and profiles for benchmark and policy checks on Linux. | Scan a VM against a hardening profile and produce a compliance report. |
| [CISO Assistant](https://github.com/intuitem/ciso-assistant-community) | Intermediate | Essential | Free (open-source community edition) | Open-source GRC platform with risk registers and framework mapping. Run it locally in Docker. Check which features are in the community edition. | Build a risk register and map controls to several frameworks in a real tool. |
| [Eramba Community](https://www.eramba.org) | Intermediate | Supplementary | Free community edition + paid | Another GRC platform you can self-host. Compare it with CISO Assistant. | Track policies, risks, audits and exceptions in a GRC tool. |
| [CSA Cloud Controls Matrix](https://cloudsecurityalliance.org/research/cloud-controls-matrix) | Intermediate | Supplementary | Free | Cloud-specific control framework with mappings to other standards. | Assess a cloud provider or workload against a recognized control set. |
| [CISA Tabletop Exercise Packages](https://www.cisa.gov/resources-tools/services/cisa-tabletop-exercises-packages) | Intermediate | Supplementary | Free | Ready-made incident scenarios with facilitator materials. | Run a tabletop exercise and write an after-action report. |
| [DISA STIGs](https://public.cyber.mil/stigs/) | Intermediate to Advanced | Supplementary | Free | Detailed hardening guidance, often used with scanners such as OpenSCAP. | Apply and verify a strict configuration baseline. |
| [ComplianceAsCode](https://github.com/ComplianceAsCode/content) | Advanced | Supplementary | Free | Open-source project that generates benchmark content and remediations used by OpenSCAP. | Understand how compliance checks and fixes are written as code. |
| [NIST OSCAL](https://pages.nist.gov/OSCAL/) | Advanced | Supplementary | Free | Machine-readable formats for controls, assessments and system security plans. | Represent control catalogs and assessment results as data. |
| [FAIR Institute resources](https://www.fairinstitute.org) | Advanced | Supplementary | Free resources + paid training | Introduces quantitative risk analysis. | Express risk in estimated financial terms rather than only high/medium/low. |

## Certifications
CompTIA Security+ first. Then ISACA CISA (audit), CISM (management) or CRISC (risk), or ISO 27001 Lead Implementer or Auditor (paid training). ISC2 has offered an entry-level Certified in Cybersecurity credential, but its pricing and free-access offers have changed, so check. Verify current requirements and prices for all of these.

## Project
Run a mock assessment for a fictional 20-person company:
1. List assets and build a risk register of at least 10 risks in CISO Assistant or a spreadsheet.
2. Select CIS Controls (Implementation Group 1) and map them to NIST CSF 2.0 functions.
3. Scan a Linux VM with Lynis or OpenSCAP, record the findings and map each to a control.
4. Fix three findings and rescan to show before and after.
5. Write three short policies from the SANS templates.
6. Run a CISA tabletop scenario and write a one-page after-action report.
