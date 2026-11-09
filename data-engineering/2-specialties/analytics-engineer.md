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

### Tutorial projects
Each project takes about a week (roughly 8 to 12 hours) and covers several skills from the list above. Do them in order, and keep each one in its own Git repo or folder.

1. **Staging and testing** (Beginner to Intermediate, ~1 week)
   - **Build:** run jaffle-shop, then start your own dbt project on a public dataset with sources, staging models and tests.
   - **Practice:** dbt basics, sources, naming, key and null tests.
   - **Done when:** `dbt build` passes and every staging model has a key test.
2. **Dimensional model** (Intermediate, ~1 week)
   - **Build:** an intermediate layer and a star schema with one fact and at least two dimensions, with generated docs.
   - **Practice:** grain, facts and dimensions, layered design, documentation.
   - **Done when:** the grain of every fact table is stated in its docs and relationship tests pass.
3. **Incremental models and BI** (Intermediate, ~1 week)
   - **Build:** an incremental model, a snapshot for a changing dimension and a Metabase dashboard on the marts.
   - **Practice:** incremental strategies, snapshots, BI tools, stakeholder communication.
   - **Done when:** new data appends without a full rebuild and the dashboard reads only from marts.

### Final project
**Time:** 3 to 4 weeks. A production-style dbt project that a team could take over, with metrics defined once and a dashboard on top.

**Specific to this project:**
- Documented conventions (naming, layering, testing) and a data dictionary.
- Metric definitions in code through the semantic layer or clearly documented models.
- GitHub Actions that run `dbt build` on pull requests, and a published docs site.
- A change log showing one breaking change handled safely.

Also meets the [production-like bar](../../README.md#what-production-like-means).
