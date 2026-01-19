# rt_analytics_mds
Create a streaming analytics data architecture on a modern data stack

STEPS:


* Flink does streaming ingestion + writes to Iceberg
* DuckDB reads Iceberg tables directly for analytics
* dbt defines transformations (facts → aggregates)
* dbt is triggered from Flink (not running inside the JVM, but orchestrated by Flink in a clean, realistic way)
