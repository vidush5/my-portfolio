---
title: "Delta Lake Demystified"
description: "Delta Lake"
dateString: July 2024
draft: false
weight: 106
cover:
    image: "/blog/DeltaLake/delta_lake.jpg"
---
# What is Delta Lake?

Delta Lake is an open-source storage framework that allows for the creation of a Lake House Architecture with computation engines such as Spark. Delta Lake enbles ACID transactions, scalable metadata management, and the unification of streaming and batch data processing. Delta Lake is fully compatible with Apache Spark APIs and runs on top of your existing data lake.  

- Delta Lake: Open-source storage layer.
- Delta Lake table format: Common format/structure from the Linux, used in Apache Spark.


### Benefits of Delta Lake
1. ACID transactions.
2. Versioning and time travel.
3. Audit History.
4. Updates on the data.

### Parquet format
- For storing the data, much smaller than CSV, and performing much faster. Also supporting nested data structure.
- Open-source format for storing data in a file.
- Optimized for big data processing & analytics.
- They are columnar storage format.
- Offers a great compression and encoding.

### Data Warehouses
#### Pros
- Great for BI applications.
- Have been around for decades.
- Reliable.
- Provide fast reads & writes of data.

#### Cons
- Limited support for ML workloads.
- Proprietary systems with only a SQL interface (Data out issues)
- Stale data (No streaming)
- Difficult to scale
- Tradionally only take in structured data.
- Vendor lock-in.
- Expensive to build, license and maintain.

### Data Lakes
#### Pros
- Supports ML
- Open formats and big ecosystem.
- Flexible - can hold structured & unstructured data.
- Organizations can collect data even if they're not certain what to do with it.
- Easy to scale.

#### Cons
- Poor support for BI
- Complex data quality problems.
- Difficult to navigate for some.
- Chance of lower query speeds.
- Hard to append data.
- Modifications to existing data are difficult.
- Mid way failed jobs.
- Realtime data.
- Handle large metadata.


### Lake House
- One unified platform for every use case.
- Adds reliability, performance, governance, and quality to existing data lakes.
- Based on open data format(parquet)
- Simplifies data engineering with a curated data lake approach.
- Separation of compute and storage.
- Infinite storage capacity.
- Leverage best aspects of a data warehouse.
- Low data gravity.
- High data throughput.
- No limits on data structure.
- Mix batch and streaming workloads.

# That’s it!

