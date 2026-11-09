# Data Engineer

**Role:** builds and runs pipelines that ingest, clean, store and deliver data reliably.
**Prerequisites:** [Fundamentals](../1-basics/fundamentals.md) and [SQL and databases](../1-basics/sql-and-databases.md).

## Skills, in order
1. Python scripting and packaging
2. ETL vs ELT and incremental loading
3. File formats: CSV, JSON, Parquet
4. Orchestration: scheduling, retries, backfills
5. Ingestion from APIs and databases
6. Containers and CI/CD for pipelines
7. Monitoring, alerting and idempotent design

**Path at a glance:**
- Beginner to intermediate: Data Engineering Zoomcamp, then the Airflow tutorials.
- Intermediate: Astronomer Academy or Dagster University, dlt for ingestion.
- Advanced: Airflow best practices and company engineering blogs.

## Resources
| Resource | Level | Cost | What it is | You will be able to |
|---|---|---|---|---|
| [Data Engineering Zoomcamp](https://github.com/DataTalksClub/data-engineering-zoomcamp) | Beginner to Intermediate | Free | Free cohort-style course with videos, homework and a capstone project covering Docker, Terraform, orchestration, warehouses, dbt and streaming. Check the current cohort schedule. | Build an end-to-end pipeline from ingestion to dashboard. |
| [Apache Airflow documentation](https://airflow.apache.org/docs/) | Intermediate | Free | Official docs and tutorials for the most widely used orchestrator. Choose the docs for your installed version. | Write DAGs with scheduling, retries and backfills. |
| [Astronomer Academy](https://academy.astronomer.io) | Intermediate | Free + paid | Courses and learning paths on Airflow. Check which are free. | Use Airflow concepts and best practices in realistic pipelines. |
| [Dagster University](https://courses.dagster.io) | Intermediate | Free | Courses on asset-based orchestration with Dagster. | Model pipelines as data assets and test them locally. |
| [dlt documentation](https://dlthub.com/docs) | Intermediate | Free (open source) | Python library for loading data from APIs and databases into warehouses. | Write incremental, schema-aware loads in a few lines of Python. |
| [Airbyte documentation](https://docs.airbyte.com) | Intermediate | Free (open source) + paid cloud | Supplementary: connector-based ingestion platform you can self-host. | Sync data from common sources without writing custom code. |
| [Prefect documentation](https://docs.prefect.io) | Intermediate | Free (open source) + paid cloud | Supplementary: a Python-first workflow orchestrator. | Compare orchestrator styles and run flows with retries. |
| [Apache Parquet documentation](https://parquet.apache.org/docs/) | Intermediate | Free | Supplementary: reference for the standard columnar file format. | Explain why columnar formats save storage and speed up scans. |
| [Airflow best practices](https://airflow.apache.org/docs/apache-airflow/stable/best-practices.html) | Advanced | Free | Official guidance on DAG design, testing and performance. | Write DAGs that are idempotent, testable and efficient. |
| [Netflix](https://netflixtechblog.com) and [Uber](https://www.uber.com/blog/engineering/) engineering blogs | Advanced | Free | Supplementary: real production data platform case studies. | See how large systems are designed and the trade-offs behind them. |

## Certifications
Cloud vendor certifications are the most common (see [Data Platform Engineer](data-platform-engineer.md)). A strong public pipeline project matters more.

## Project

### Tutorial projects
Each project takes about a week (roughly 8 to 12 hours) and covers several skills from the list above. Do them in order, and keep each one in its own Git repo or folder.

1. **Batch ingestion** (Beginner to Intermediate, ~1 week)
   - **Build:** a script that pulls a public API, writes raw JSON and clean Parquet, and loads Postgres with upserts, all running in Docker Compose.
   - **Practice:** Python packaging, file formats, idempotent loads, containers, logging.
   - **Done when:** running it twice produces no duplicates and queries in DuckDB and Postgres agree.
2. **Orchestrated pipeline** (Intermediate, ~1 week)
   - **Build:** schedule project 1 in Airflow (or Dagster) with retries, a backfill, and incremental loading with dlt.
   - **Practice:** orchestration, backfills, incremental loads, ETL vs ELT.
   - **Done when:** a forced failure retries, and a backfill of two weeks fills the gaps without duplicates.
3. **Reliability and CI** (Intermediate, ~1 week)
   - **Build:** add unit tests, data checks, a Dockerfile and a GitHub Actions workflow, plus failure alerts.
   - **Practice:** testing, CI/CD, monitoring, alerting.
   - **Done when:** a bad change fails the build and a failed run sends an alert.

### Final project
**Time:** 3 to 4 weeks. A daily pipeline with raw, clean and serving layers over a public API, designed to survive schema changes and reruns.

**Specific to this project:**
- Raw data kept immutable, with replay and backfill supported.
- Schema change handling and a documented data contract for the output.
- Freshness and failure alerts, and a test with ten times the normal volume.
- A cost or storage note for running it for a year.

Also meets the [production-like bar](../../README.md#what-production-like-means).
