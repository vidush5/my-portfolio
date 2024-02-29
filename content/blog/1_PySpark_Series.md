---
title: "Pyspark Learnings"
description: "PySpark Concepts"
dateString: Feb 2024
draft: false
weight: 106
cover:
    image: "/blog/Pyspark/pyspark_png.png"
---
# PySpark | RDD, Dataframe, Dataset 
In Apache Spark, RDD, DataFrame & Dataset are three different APIs provided to work with distributed data. Users can able to select different APIs based on their requirement.

## Similarities
1. Fault Tolerant
2. Distributed in Nature
3. In-Memory parallel processing
4. Immutable
5. Lazy evaluation

## Differences

| RDD           | DataFrame     | Dataset       |
|---------------|---------------|---------------|
| Fundamental Data Structure | Distributed collection of data organized in a named columns | Best of RDD + Best of Dataframe |
| Need to program How & What to do | Need to program What to do | Need to program What to do |
| Strong type safety | Less type safety | Strong type safety |
| No optimization | Catalyst optimizer | Optimization |
| Supports Java, Scala, Python & R | Supports Java, Scala, Python & R | Supports Scala, Java |
| No schema | Schema structured | Schema structured |
| Suitable for low-level operations & when fine-grained control over data processing is required | Suitable for structured data processing, SQL queries, & data exploration tasks | Suitable when type safety & performance optimizations are required |


# PySpark | Transformation & Action

***Transformation*** : Which transform data from one form to another. Used to define the sequence of operations to be performed. A new dataframe will be created after transformation.Ex: Filter, Union, groupby

- Narrow Transformation: Each partition of an RDD contributes to generating only one partition in the resulting RDD. Common narrow transformations include map(), filter(), and union().

- Wide Transformation: Each input partition of an RDD is used to compute multiple output partitions of the resulting RDD. Ex : groupByKey(), reduceByKey(), and sortByKey().


***Action***: Actions are operations that trigger the execution of the transformation & returns the result to the driver program. Ex: Count, Collect, Save

***Lazy Evaluation*** : Transformations will not execute until an action is called.

***DAG***: The DAG is a directed graph because the transformations are executed in a specific order, and it is acyclic because there are no cycles or loops in the graph.


# PySpark | On-Heap vs Off-Heap

***On-Heap Memory***: In worker node, memory which is controlled by executor. (Controlled by JVM process). We have 04 parts,

- Reserved Memory: Reserved by Spark for internal purposes.

- User Memory: For storing the data-structures created & managed by the user's code.

- Execution Memory: JVM heap space used by data-structures during shuffle operations (Joins & Aggregations)

- Storage Memory: JVM heap space reserved for cached data

***Off-Heap Memory***: In worker node, memory which is not controlled by executor. (Controlled by OS)

# DataBricks: Cluster Deployment

## Cluster Types

Two types of cluster in Databricks.

- All-Purpose Clusters / Interactive: Mainly used to analyze data interactively using databricks notebooks. Can able to manually stop & restart. Multiple users can share these clusters to do collaborative interactive analysis.

- Job Clusters: Databricks job scheduler creates these clusters when we run a job on a new job cluster. Mainly consider for running fast & robust automated tasks. Create automatically when we run the job in the new job cluster and terminate the cluster once the job ends. Cnnot be restarted.

There are three modes of clusters that databricks supports, based on the cluster usage.

- Standard clusters: Suitable for single user
- High concurrent clusters
- Single node clusters: Runs the job only on driver node & no worker nodes are provisioned.







