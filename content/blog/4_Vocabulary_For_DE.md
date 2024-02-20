---
title: "Vocabulary for Data Engineers"
description: "Terms used by Data Engineers"
dateString: June 2022
draft: false
weight: 106
cover:
    image: "/blog/Vocabulary_For_DE/img1.jpeg"
---
# Data Engineering
Data Engineering is one of the leading & emerging fields. The demand for Data engineers has risen in recent days. When you google what is data engineering? you can get thousands of answers but here I pointing out only three answers that I understood clearly and I hope that will make you get a clear understanding.

- **Data engineering** is the practice of designing and building systems for collecting, storing, and analyzing data at scale. 

- The key to understanding what data engineering lies in the “engineering” part. Engineers design and build things. “Data” engineers design and build pipelines that transform and transport data into a format wherein, by the time it reaches the Data Scientists or other end users, it is in a highly usable state.

- **Data engineering** is the complex task of making raw data usable to data scientists and groups within an organization. Data engineering encompasses numerous specialties of data science.

In this article, I will mention key terms used by data engineers regularly. I have tried my best to keep this as simple as possible and decided to compile it all in one place.

# Key Terms

### Data Lineage
Data lineage is a process of understanding how the data generated from the source and how it reaches the destination. Simply it answers the following questions.
- Where the data begins?
- What happens to it over time?
- Where it moves over time?
- Where it ends up?

##### Data Lineage Tools
01. Keboola
02. Dremio
03. Kylo
04. Octopai


### Data Pipeline
Sequences of processes/steps that copy, transform, load and analyze the data.

### DAG
Data pipelines are modeled as *Directed acyclic graphs*. DAG is a conceptual representation of a series of activities or in other words, a mathematical abstraction of a data pipeline.

### Data Warehouse
Exists on top of several databases and used for business intelligence.

##### Examples
01. Google BigQuery
02. Snowflake


### Apache Impala
Basically, to overcome the slowness of Hive queries, Cloudera offers a seperate tool is what we call Impala.
- Offers high-performance, low-latency SQL queries.
- Only available in Hadoop distribution.
- MPP (Massive Parallel Processing) query engine that executes on Hadoop platform.

### Apache Kafka
Open-source streaming platform.

### OLTP
*Online Transactional Processing* designed for transactional processing, typically follow data normalization rules.
- Transactional
- Real time fast processing
- Normalized
- Examples: Financial transactional systems, ATM Center

### OLAP
*Online Analytical Processing* models used for datawarehouse and datamart applications.
- Analytical
- Slow queries
- Denormalized
- Historical data
- Example: Recommendation Systems


### References
01. https://www.youtube.com/watch?v=xOn-DJbUi1w&t=61s

# That’s it!

Happy learning ..! Will update other terms in future!

