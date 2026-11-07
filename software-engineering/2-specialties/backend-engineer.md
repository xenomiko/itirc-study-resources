# Backend Engineer

**Role:** builds the services, APIs and data layers behind applications, and keeps them correct, secure and fast.
**Prerequisites:** [Programming basics](../1-basics/programming-basics.md), [SQL and databases](../../data-engineering/1-basics/sql-and-databases.md) and Git.

## Skills, in order
1. One backend language and framework
2. HTTP and REST API design
3. Databases: modeling, queries, migrations
4. Authentication, authorization and secure coding
5. Testing: unit, integration, contract
6. Caching, queues and background jobs
7. Observability: logs, metrics, traces
8. System design and scaling trade-offs

**Path at a glance:**
- Beginner to intermediate: Full Stack Open, or the FastAPI, Django or Go tutorials, plus the Postgres tutorial.
- Intermediate: OpenAPI, OWASP API Security Top 10, Redis University, pytest or your language's test framework.
- Advanced: System Design Primer, OpenTelemetry, distributed systems lectures in [theory](../1-basics/theory.md).

## Resources
| Resource | Level | Cost | What it is | You will be able to |
|---|---|---|---|---|
| [FastAPI tutorial](https://fastapi.tiangolo.com/tutorial/) | Beginner to Intermediate | Free | Official step-by-step tutorial for Python APIs. | Build typed REST endpoints with validation and automatic docs. |
| [Django tutorial](https://docs.djangoproject.com/en/stable/intro/tutorial01/) | Beginner to Intermediate | Free | Official tutorial for a batteries-included Python framework. | Build a database-backed app with admin, auth and migrations. |
| [A Tour of Go](https://go.dev/tour/) | Beginner | Free | Interactive tour of Go, followed by the official tutorials. | Write Go services with goroutines and a standard library HTTP server. |
| [Full Stack Open](https://fullstackopen.com/en/) | Intermediate | Free | Also in [Frontend Engineer](frontend-engineer.md). Part 3 onward covers Node, Express, databases and testing. | Build and test a Node API with a database and authentication. |
| [OpenAPI Initiative documentation](https://learn.openapis.org) | Intermediate | Free | Official learning guide for describing HTTP APIs. | Write an API contract and generate docs from it. |
| [OWASP API Security Top 10](https://owasp.org/API-Security/) | Intermediate | Free | Also in [cybersecurity](../../cybersecurity/2-specialties/web-application-security.md). Check the current edition. | Prevent broken authorization and other common API flaws. |
| [Redis University](https://university.redis.io) | Intermediate | Free | Free courses on caching, data structures and Redis patterns. Check the current catalog. | Add caching and queues and reason about invalidation. |
| [pytest documentation](https://docs.pytest.org) | Intermediate | Free | Official docs for Python testing. Use your language's equivalent if you chose another stack. | Write fixtures, parametrized tests and integration tests. |
| [The Twelve-Factor App](https://12factor.net) | Intermediate | Free | Short web guide to building deployable services. | Configure and deploy services consistently across environments. |
| [OpenTelemetry documentation](https://opentelemetry.io/docs/) | Intermediate to Advanced | Free | Official docs for vendor-neutral traces, metrics and logs. | Instrument a service and follow a request across components. |
| [System Design Primer](https://github.com/donnemartin/system-design-primer) | Advanced | Free | Supplementary: large GitHub study guide on scalable design. Its Anki decks and diagrams are useful. | Discuss caching, sharding, queues and trade-offs on a design problem. |
| [Martin Fowler: Microservices](https://martinfowler.com/articles/microservices.html) | Advanced | Free | Supplementary: classic article on service boundaries and trade-offs. | Decide when to split a monolith and what it costs. |
| [ByteByteGo](https://bytebytego.com) | Intermediate to Advanced | Free + paid | Supplementary: illustrated system design explainers. Check which are free. | Revise common architectures visually. |

## Certifications
Cloud associate certifications (AWS Solutions Architect Associate, Azure AZ-204) are common. Verify current exams and prices.

## Project
REST API with authentication, a Postgres schema with migrations, an OpenAPI spec, caching, integration tests, structured logging and OpenTelemetry traces. Deploy it with Docker Compose and document one load test result.
