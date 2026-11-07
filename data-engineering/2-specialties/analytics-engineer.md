# Analytics Engineer

**Role:** turns raw data into clean, tested, documented tables and metrics that analysts and dashboards can trust.
**Prerequisites:** [SQL and databases](../1-basics/sql-and-databases.md), including window functions. Git from [fundamentals](../1-basics/fundamentals.md).

## Skills, in order
1. Advanced SQL: CTEs, window functions
2. Dimensional modeling: facts, dimensions, grain
3. dbt: models, sources, tests, docs
4. Layered design: staging, intermediate, marts
5. Incremental models and snapshots
6. Metrics and semantic layers
7. BI tools and stakeholder communication

**Path at a glance:**
- Beginner to intermediate: dbt Fundamentals, then the jaffle-shop sample project.
- Intermediate: Kimball techniques, dbt docs on testing and incremental models.
- Advanced: semantic layer docs, then CI for dbt projects.

## Resources
| Resource | Level | Cost | What it is | You will be able to |
|---|---|---|---|---|
| [dbt Learn](https://learn.getdbt.com) | Beginner to Intermediate | Free + paid (check which courses are free) | Official courses starting with dbt Fundamentals. | Build, test and document dbt models. |
| [dbt documentation](https://docs.getdbt.com) | Intermediate | Free | Official reference for models, tests, snapshots, incremental strategies and packages. | Choose the right materialization and write useful tests. |
| [dbt jaffle-shop](https://github.com/dbt-labs/jaffle-shop) | Beginner to Intermediate | Free | Official sample project you can run locally with DuckDB or Postgres. | Run a full dbt project and read its layered structure. |
| [Kimball dimensional modeling techniques](https://www.kimballgroup.com/data-warehouse-business-intelligence-resources/kimball-techniques/) | Intermediate | Free | Concise articles on star schemas, grain and slowly changing dimensions. | Design a star schema and explain its grain. |
| [dbt Semantic Layer and MetricFlow docs](https://docs.getdbt.com/docs/build/about-metricflow) | Advanced | Free docs (some features need a paid plan) | Docs on defining metrics once and reusing them. Check which features need a paid plan. | Define consistent business metrics in code. |
| [SQLMesh documentation](https://sqlmesh.readthedocs.io) | Intermediate to Advanced | Free (open source) | Supplementary: alternative transformation framework with virtual environments. | Compare approaches to versioned, testable transformations. |
| [Metabase documentation](https://www.metabase.com/docs/latest/) | Beginner to Intermediate | Free (open source) + paid cloud | Supplementary: self-hostable BI tool. | Build dashboards on top of your marts. |
| [Apache Superset documentation](https://superset.apache.org/docs/intro) | Intermediate | Free | Supplementary: another open-source BI option. | Build charts and dashboards and compare BI tools. |

## Certifications
dbt Analytics Engineering Certification (paid exam). Verify the current format and price.

## Project
dbt project on a public dataset with staging, intermediate and mart layers, a star schema, tests on keys and relationships, generated docs, an incremental model, and a Metabase dashboard. Add a GitHub Actions job that runs `dbt build` on pull requests.
