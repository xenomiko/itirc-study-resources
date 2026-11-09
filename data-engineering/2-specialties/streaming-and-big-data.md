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

### Tutorial projects
Each project takes about a week (roughly 8 to 12 hours) and covers several skills from the list above. Do them in order, and keep each one in its own Git repo or folder. Run everything locally first.

1. **Spark batch processing** (Beginner to Intermediate, ~1 week)
   - **Build:** a PySpark job over a multi-gigabyte public dataset with joins, aggregates and partitioned Parquet output, tuned using the Spark UI.
   - **Practice:** DataFrames, shuffles, skew, partitioning, tuning.
   - **Done when:** you record timings before and after fixing one skew or shuffle problem.
2. **Event streaming with Kafka** (Intermediate, ~1 week)
   - **Build:** a local Kafka broker in Docker, an event generator, producers and consumer groups on a three-partition topic, with replay.
   - **Practice:** topics, partitions, keys, consumer groups, offsets.
   - **Done when:** you can show which consumer reads each partition and replay events from an earlier offset.
3. **Stream processing and tables** (Intermediate to Advanced, ~1 week)
   - **Build:** windowed aggregates with late-data handling in Flink or Spark Structured Streaming, writing to Iceberg or Delta.
   - **Practice:** windows, state, late data, table formats.
   - **Done when:** a time-travel query returns an earlier table version and late events are counted correctly.

### Final project
**Time:** 3 to 4 weeks. A real-time analytics pipeline with a configurable event generator, a streaming job and lakehouse tables, tested under load and restarts.

**Specific to this project:**
- Documented delivery guarantees and what happens on duplicate or late events.
- Checkpointing with a restart test that proves no data loss.
- A consumer lag and throughput dashboard with at least one alert.
- Table maintenance (compaction or cleanup) and a load test at several event rates.

Also meets the [production-like bar](../../README.md#what-production-like-means).
