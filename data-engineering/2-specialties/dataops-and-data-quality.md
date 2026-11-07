# DataOps and Data Quality

**Role:** keeps data trustworthy with tests, monitoring, lineage, ownership and governance.
**Prerequisites:** [Data Engineer](data-engineer.md) or [Analytics Engineer](analytics-engineer.md). For privacy and compliance context see [GRC](../../cybersecurity/2-specialties/grc.md).

## Skills, in order
1. Data quality dimensions: completeness, validity, freshness, uniqueness
2. Testing in pipelines (dbt tests, expectations)
3. Data contracts and schema change management
4. Lineage and metadata catalogs
5. Observability: freshness, volume and anomaly alerts
6. Incident response for data issues
7. Governance basics: ownership, access, privacy

**Path at a glance:**
- Beginner: dbt tests and Great Expectations quickstart.
- Intermediate: Soda checks, OpenLineage, then a catalog such as DataHub or OpenMetadata.
- Advanced: data contracts and alert design.

## Resources
| Resource | Level | Cost | What it is | You will be able to |
|---|---|---|---|---|
| [dbt tests documentation](https://docs.getdbt.com/docs/build/data-tests) | Beginner | Free | Official docs for generic and singular tests. See [Analytics Engineer](analytics-engineer.md). | Add key, null and relationship tests to every model. |
| [Great Expectations documentation](https://docs.greatexpectations.io) | Beginner to Intermediate | Free (open source) + paid cloud | Docs for defining and running data validations. | Write expectations and run them inside a pipeline. |
| [Soda documentation](https://docs.soda.io) | Intermediate | Free (open source) + paid cloud | Docs for YAML-based data quality checks. | Define freshness and volume checks and alert on failures. |
| [OpenLineage documentation](https://openlineage.io/docs) | Intermediate | Free | Open standard for collecting lineage events from jobs. | Emit lineage from Airflow or Spark and trace a column back to its source. |
| [DataHub documentation](https://docs.datahub.com) | Intermediate to Advanced | Free (open source) + paid cloud | Docs for an open-source metadata platform. Verify the current docs site. | Run a catalog locally and ingest metadata from your warehouse. |
| [OpenMetadata documentation](https://docs.open-metadata.org) | Intermediate to Advanced | Free (open source) | Supplementary: alternative catalog with lineage and quality features. | Compare catalog tools and pick one for a project. |
| [Open Data Contract Standard (Bitol)](https://bitol.io) | Advanced | Free | Supplementary: open specification for data contracts. | Write a contract that states schema, owners and quality expectations. |
| [Prometheus](https://prometheus.io/docs/) and [Grafana](https://grafana.com/docs/) docs | Intermediate to Advanced | Free (open source) | Supplementary: metrics and dashboards you can reuse for pipeline monitoring. | Alert on pipeline duration, failures and freshness. |

## Certifications
DAMA CDMP (paid) for data management. Otherwise rely on a portfolio project. Verify current details.

## Project
Add quality and lineage to a pipeline from [Data Engineer](data-engineer.md): dbt or Great Expectations tests, a Soda freshness check, OpenLineage events into a local catalog, and a short runbook describing what happens when a check fails.
