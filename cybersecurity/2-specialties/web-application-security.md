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
Run Juice Shop locally, solve ten challenges, and write each up with root cause, proof and fix. Add an API test that demonstrates one object-level authorization flaw.
