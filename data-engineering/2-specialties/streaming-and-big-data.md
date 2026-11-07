# Streaming and Big Data

**Role:** processes large datasets and real-time event streams with distributed engines.
**Prerequisites:** [Data Engineer](data-engineer.md), solid SQL, and Docker.

## Skills, in order
1. Distributed processing concepts: partitions, shuffles, skew
2. Spark: DataFrames, SQL, joins, tuning
3. Kafka: topics, partitions, consumer groups
4. Stream processing: windows, state, late data (Flink or Spark Structured Streaming)
5. Lakehouse table formats: Iceberg, Delta
6. Delivery semantics and exactly-once trade-offs
7. Cost and performance tuning

**Path at a glance:**
- Beginner to intermediate: Spark quick start in local mode, then Confluent Developer for Kafka.
- Intermediate: Flink docs and training, Iceberg or Delta docs.
- Advanced: Spark tuning, Kafka internals and the distributed systems lectures in [theory](../1-basics/theory.md).

**Cost warning:** run everything locally in Docker or on a free tier first. Shut down clusters and delete cloud resources when finished.

## Resources
| Resource | Level | Cost | What it is | You will be able to |
|---|---|---|---|---|
| [Apache Spark documentation](https://spark.apache.org/docs/latest/) | Beginner to Advanced | Free | Official quick start, SQL guide and tuning pages. Use PySpark in local mode first. | Transform data with DataFrames and tune joins and partitions. |
| [Databricks Free Edition](https://www.databricks.com/learn/free-edition) | Intermediate | Free (with limits) | Free environment for Spark notebooks. Also in [labs and tools](../1-basics/labs-and-tools.md). Check current limits. | Run Spark jobs and Delta tables without managing a cluster. |
| [Confluent Developer](https://developer.confluent.io) | Beginner to Intermediate | Free courses (cloud trial may be needed) | Tutorials and courses on Kafka concepts and client code. | Produce and consume events and explain partitions and consumer groups. |
| [Apache Kafka documentation](https://kafka.apache.org/documentation/) | Intermediate | Free | Official reference, including the quickstart you can run locally. | Run a local broker and design topics with sensible partitioning. |
| [Apache Flink documentation](https://nightlies.apache.org/flink/flink-docs-stable/) | Intermediate to Advanced | Free | Official docs and tutorials on streaming, windows and state. | Build stateful stream jobs with event-time windows. |
| [Apache Iceberg documentation](https://iceberg.apache.org/docs/latest/) | Intermediate | Free | Docs for an open table format with snapshots and schema evolution. | Explain how table formats add ACID and time travel to files. |
| [Delta Lake documentation](https://docs.delta.io) | Intermediate | Free | Supplementary: the other widely used open table format. | Compare Delta and Iceberg and pick one for a project. |
| [Redpanda University](https://university.redpanda.com) | Intermediate | Free | Supplementary: Kafka-compatible streaming courses. | See streaming concepts from a second vendor. |

## Certifications
Databricks Data Engineer Associate, Confluent Certified Developer for Apache Kafka. Verify current exams and prices.

## Project
Local streaming pipeline in Docker Compose: a producer writes events to Kafka, Spark or Flink computes windowed aggregates with late-data handling, and results land in Iceberg or Delta tables. Document the delivery guarantees you chose.
