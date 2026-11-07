# Labs and Tools

**Cost warning:** set billing alerts before using any cloud account, prefer sandbox or free tiers, and delete resources when finished. Never load real or personal data into a practice account.

**Path at a glance:** Docker Compose on your laptop (beginner) → DuckDB and Postgres locally (beginner to intermediate) → BigQuery sandbox or a free lakehouse tier (intermediate) → a trial cloud account for platform work (advanced).

| Resource | Level | Cost | What it is | You will be able to |
|---|---|---|---|---|
| [Docker Compose](https://docs.docker.com/compose/) | Beginner | Free | Defines a local multi-container stack. See also [fundamentals](fundamentals.md). | Run Postgres, an orchestrator and a database UI locally. |
| [DuckDB](https://duckdb.org/docs/) | Beginner to Intermediate | Free | Embedded analytical SQL engine. | Query Parquet and CSV files and prototype transformations quickly. |
| [GitHub Codespaces](https://docs.github.com/en/codespaces) | Beginner | Free monthly quota + paid | Browser-based dev environment. Check the current free allowance. | Work through labs without installing anything locally. |
| [BigQuery sandbox](https://cloud.google.com/bigquery/docs/sandbox) | Intermediate | Free (with limits) | Use BigQuery without a billing account. Tables expire and limits apply. | Run warehouse-scale SQL and learn partitioning and clustering. |
| [Databricks Free Edition](https://www.databricks.com/learn/free-edition) | Intermediate | Free (with limits) | Free tier for notebooks and Spark. Check current limits and features. | Practice Spark and Delta tables without paying for a cluster. |
| [Snowflake Quickstarts](https://quickstarts.snowflake.com) | Intermediate | Free guides, trial account needed | Supplementary: guided hands-on labs. A trial account is time-limited, so check its terms. | Load, transform and share data in a cloud warehouse. |
| [Jupyter](https://jupyter.org/install) | Beginner | Free | Supplementary: notebooks for exploring data. | Prototype and document analysis steps interactively. |

**Practice by specialty:**
- Pipelines and orchestration: [Data Engineer](../2-specialties/data-engineer.md)
- dbt and modeling: [Analytics Engineer](../2-specialties/analytics-engineer.md)
- Spark and Kafka: [Streaming and Big Data](../2-specialties/streaming-and-big-data.md)
- Terraform and cloud: [Data Platform Engineer](../2-specialties/data-platform-engineer.md), plus the [Terraform tutorials](../../networking/2-specialties/cloud-networking.md)
- Testing and lineage: [DataOps and Data Quality](../2-specialties/dataops-and-data-quality.md)
