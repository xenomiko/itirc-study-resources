# Web Application Security

**Role:** finds and fixes vulnerabilities in web apps and APIs.
**Prerequisites:** [Fundamentals](../1-basics/fundamentals.md), including the OWASP Top 10.

## Skills, in order
1. HTTP, cookies, sessions
2. Injection: SQLi, XSS
3. Authentication and access control (IDOR)
4. CSRF, SSRF, file upload and XXE
5. API security
6. Secure coding fixes

**Path at a glance:**
- Beginner: Juice Shop or WebGoat alongside the first PortSwigger topics.
- Intermediate: API Security Top 10, HTB Academy web modules, PentesterLab.
- Advanced: PortSwigger advanced topics, then fix what you find using the OWASP Cheat Sheets.

**Safety:** run Juice Shop and WebGoat locally and bind them to localhost only.

## Resources
| Resource | Level | Cost | What it is | You will be able to |
|---|---|---|---|---|
| [PortSwigger Web Security Academy](https://portswigger.net/web-security) | Beginner to Advanced | Free | Topic-by-topic lessons with free labs and Burp Suite Community. | Find and exploit SQLi, XSS, CSRF, SSRF and more. |
| [OWASP Juice Shop](https://owasp.org/www-project-juice-shop/) | Beginner to Intermediate | Free | Intentionally insecure modern web app with a scoreboard. Run it locally in Docker. | Find vulnerabilities across the Top 10 in a realistic app. |
| [OWASP WebGoat](https://owasp.org/www-project-webgoat/) | Beginner to Intermediate | Free | Deliberately insecure Java app with guided lessons. | Learn each vulnerability class through in-app exercises. |
| [HTB Academy: Web Requests and Web Attacks](https://academy.hackthebox.com) | Beginner to Intermediate | Free tier + paid | Supplementary: modules on HTTP internals and common attack classes. Check module access. | Craft raw HTTP requests and exploit IDOR, verb tampering and XXE. |
| [OWASP API Security Top 10](https://owasp.org/API-Security/) | Intermediate | Free | Ranked API risks. Check the current edition. | Test for broken object-level authorization and other API flaws. |
| [PentesterLab](https://pentesterlab.com) | Intermediate to Advanced | Free + paid | Supplementary: exercise-based web security training with badges. | Exploit and understand vulnerabilities at code level. |

## Certifications
PortSwigger Burp Suite Certified Practitioner (paid exam) and eWPT. Verify current details.

## Project

### Tutorial projects
Each project takes about a week (roughly 8 to 12 hours) and covers several skills from the list above. Do them in order, and keep each one in its own Git repo or folder. Run targets on localhost only.

1. **Injection and sessions** (Beginner, ~1 week)
   - **Build:** complete about fifteen PortSwigger labs on SQL injection, XSS and session handling, and write each up.
   - **Practice:** HTTP, cookies, SQLi, XSS, Burp Community.
   - **Done when:** each write-up has root cause, proof and the fix you would make.
2. **Access control and APIs** (Intermediate, ~1 week)
   - **Build:** attack Juice Shop's authentication, IDOR and API flaws, then turn what you found into a Postman or script collection with two test users.
   - **Practice:** authentication, authorization, API Security Top 10, API testing.
   - **Done when:** your collection reproduces three object-level authorization flaws on demand.
3. **Break it, then fix it** (Intermediate, ~1 week)
   - **Build:** write a small web app (Flask or Express) with five planted flaws, exploit each, fix them using the OWASP Cheat Sheets and add regression tests.
   - **Practice:** secure coding, CSRF, file upload, input handling, testing.
   - **Done when:** every exploit now fails and a test proves it.

### Final project
**Time:** 3 to 4 weeks. A full security assessment and remediation of a realistic app (your own or Juice Shop run locally): test plan, findings, fixes in a patched copy and retest.

**Specific to this project:**
- A written test plan following the OWASP testing approach, with scope and out-of-scope items.
- At least fifteen findings rated with CVSS, each with proof, root cause and fix.
- Fixes implemented in a patched copy, with regression tests running in CI.
- A report with an executive summary and a retest section showing before and after.

Also meets the [production-like bar](../../README.md#what-production-like-means).
