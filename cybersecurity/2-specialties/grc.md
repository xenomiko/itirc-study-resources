# GRC (Governance, Risk and Compliance)

**Role:** defines security policy, assesses and tracks risk, maps controls to standards and regulations, and prepares organizations for audits.
**Prerequisites:** [Fundamentals](../1-basics/fundamentals.md). Helpful: [Defensive Security](defensive-security.md) for incident response context and [Cloud Security](cloud-security.md) for cloud compliance.

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
- Beginner: NIST CSF 2.0 and CIS Controls for the vocabulary, SANS policy templates to see real policies.
- Intermediate: NIST RMF and SP 800-53, then Lynis or OpenSCAP audits of your own VM, a CISO Assistant lab, and a CISA tabletop.
- Advanced: ComplianceAsCode and NIST OSCAL to automate compliance, FAIR to quantify risk.
- Also use: [MITRE ATT&CK](https://attack.mitre.org) to link controls to attacker techniques, and [Prowler](cloud-security.md) for compliance reports on cloud accounts.

**Safety:** run scanners and hardening tools only on VMs you own, and snapshot before applying any remediation.

## Resources
| Resource | Level | Cost | What it is | You will be able to |
|---|---|---|---|---|
| [NIST Cybersecurity Framework 2.0](https://www.nist.gov/cyberframework) | Beginner | Free | Official framework with a Govern function added, plus quick-start guides and reference tools. | Describe an organization's security program in CSF terms and build a simple profile. |
| [CIS Controls](https://www.cisecurity.org/controls) | Beginner | Free (registration may be needed) | Prioritized safeguards with implementation groups for small to large organizations. Check the current version. | Pick a sensible first set of controls for a small organization. |
| [SANS Information Security Policy Templates](https://www.sans.org/information-security-policy/) | Beginner | Free | Editable sample policies for common topics. | Draft and adapt acceptable-use, access and incident response policies. |
| [TryHackMe governance and risk rooms](https://tryhackme.com) | Beginner | Free tier + paid | Supplementary: search for governance, regulation and risk rooms. Availability changes, so check. | Practice GRC concepts in a guided browser environment. |
| [NIST Risk Management Framework](https://csrc.nist.gov/projects/risk-management) | Intermediate | Free | Official process for categorizing systems, selecting, implementing and assessing controls, and authorizing operation. | Walk a system through the RMF steps and document each one. |
| [NIST SP 800-53 control catalog](https://csrc.nist.gov/pubs/sp/800/53/r5/upd1/final) | Intermediate | Free | Detailed control families with companion assessment guidance. Use it as a reference, not a read-through. | Look up, interpret and select controls for a given risk. |
| [Lynis](https://cisofy.com/lynis/) | Intermediate | Free (paid enterprise edition) | Auditing tool for Linux and Unix hosts with hardening suggestions. | Scan your own VM, interpret findings and map them to CIS controls. |
| [OpenSCAP documentation](https://www.open-scap.org) | Intermediate | Free | Scanner and profiles for benchmark and policy checks on Linux. | Scan a VM against a hardening profile and produce a compliance report. |
| [CISO Assistant](https://github.com/intuitem/ciso-assistant-community) | Intermediate | Free (community edition) | Open-source GRC platform with risk registers and framework mapping. Run it locally in Docker. Check which features the community edition includes. | Build a risk register and map controls to several frameworks in a real tool. |
| [Eramba Community](https://www.eramba.org) | Intermediate | Free + paid | Supplementary: another self-hosted GRC platform. Compare it with CISO Assistant. | Track policies, risks, audits and exceptions in a GRC tool. |
| [CSA Cloud Controls Matrix](https://cloudsecurityalliance.org/research/cloud-controls-matrix) | Intermediate | Free | Supplementary: cloud control framework with mappings to other standards. | Assess a cloud provider or workload against a recognized control set. |
| [CISA Tabletop Exercise Packages](https://www.cisa.gov/resources-tools/services/cisa-tabletop-exercises-packages) | Intermediate | Free | Supplementary: ready-made incident scenarios with facilitator materials. | Run a tabletop exercise and write an after-action report. |
| [DISA STIGs](https://public.cyber.mil/stigs/) | Intermediate to Advanced | Free | Supplementary: detailed hardening guidance, often used with OpenSCAP. | Apply and verify a strict configuration baseline. |
| [ComplianceAsCode](https://github.com/ComplianceAsCode/content) | Advanced | Free | Supplementary: open-source project that generates benchmark content and remediations used by OpenSCAP. | Understand how compliance checks and fixes are written as code. |
| [NIST OSCAL](https://pages.nist.gov/OSCAL/) | Advanced | Free | Supplementary: machine-readable formats for controls, assessments and system security plans. | Represent control catalogs and assessment results as data. |
| [FAIR Institute resources](https://www.fairinstitute.org) | Advanced | Free + paid | Supplementary: introduces quantitative risk analysis. Training is paid. | Express risk in estimated financial terms rather than only high/medium/low. |

## Certifications
CompTIA Security+ first. Then ISACA CISA (audit), CISM (management) or CRISC (risk), or ISO 27001 Lead Implementer or Auditor (paid training). ISC2's entry-level Certified in Cybersecurity has had changing pricing and free-access offers, so check. Verify current requirements and prices.

## Project

### Tutorial projects
Each project takes about a week (roughly 8 to 12 hours) and covers several skills from the list above. Do them in order, and keep each one in its own Git repo or folder. Run scanners only on VMs you own.

1. **Governance foundation** (Beginner, ~1 week)
   - **Build:** a fictional 20-person company profile, a role list, a risk method and three policies adapted from the SANS templates.
   - **Practice:** governance basics, policy writing, roles.
   - **Done when:** each policy names an owner, scope, review date and the control it supports.
2. **Risk assessment** (Beginner to Intermediate, ~1 week)
   - **Build:** an asset inventory and a register of at least fifteen risks in CISO Assistant, each with a treatment plan.
   - **Practice:** assets, threats, likelihood, impact, treatment.
   - **Done when:** every risk has an owner, a rating and a decision to mitigate, accept, transfer or avoid.
3. **Control mapping and testing** (Intermediate, ~1 week)
   - **Build:** map CIS Controls (Implementation Group 1) to NIST CSF 2.0, scan a Linux VM with Lynis or OpenSCAP, fix three findings and rescan.
   - **Practice:** frameworks, gap analysis, technical control testing.
   - **Done when:** each finding maps to a control and the rescan shows the fixes.
4. **Incident readiness** (Intermediate, ~1 week)
   - **Build:** run a CISA tabletop scenario with at least two other people, and write an after-action report.
   - **Practice:** incident response, audit evidence, reporting.
   - **Done when:** the report lists gaps, owners and due dates.

### Final project
**Time:** 3 to 4 weeks. An audit-ready security program package for the fictional company, reviewed by a peer playing auditor.

**Specific to this project:**
- Scope, risk register, control mapping, policies and an evidence folder indexed by control.
- Technical scan results showing before and after remediation.
- Tabletop report, a short list of metrics, and a 90-day improvement roadmap.
- A mock audit: a peer finds at least five gaps and you track them to closure.

Also meets the [production-like bar](../../README.md#what-production-like-means).
