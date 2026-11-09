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

### Tutorial projects
Each project takes about a week (roughly 8 to 12 hours) and covers several skills from the list above. Do them in order, and keep each one in its own Git repo or folder. Use a pipeline from [Data Engineer](data-engineer.md) or [Analytics Engineer](analytics-engineer.md) as the base.

1. **Test layer** (Beginner to Intermediate, ~1 week)
   - **Build:** dbt tests and a Great Expectations suite covering completeness, validity, uniqueness and freshness, then break the data in five ways.
   - **Practice:** quality dimensions, pipeline testing, failure handling.
   - **Done when:** each of the five bad batches is caught by the intended check.
2. **Observability and alerts** (Intermediate, ~1 week)
   - **Build:** Soda freshness and volume checks, with alerts routed to a channel you can show working, and a simple results dashboard.
   - **Practice:** observability, anomaly alerts, alert design.
   - **Done when:** a late load and a volume drop both alert, and a normal run stays quiet.
3. **Lineage and catalog** (Intermediate to Advanced, ~1 week)
   - **Build:** emit OpenLineage events from your pipeline into DataHub or OpenMetadata running locally, and add owners and descriptions.
   - **Practice:** lineage, metadata, ownership, governance.
   - **Done when:** you can trace a dashboard column back to its source and name its owner.

### Final project
**Time:** 3 to 4 weeks. A data reliability layer for a full pipeline: contracts, tests, freshness targets, alerting, lineage and an incident process.

**Specific to this project:**
- A data contract for each output table, enforced in CI.
- Freshness and quality targets with a scorecard over time.
- An incident drill: inject a bad batch, detect it, trace impact with lineage, recover and write the postmortem.
- A runbook describing who is paged and what they do.

Also meets the [production-like bar](../../README.md#what-production-like-means).
