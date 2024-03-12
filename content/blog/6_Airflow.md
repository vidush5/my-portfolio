---
title: "Getting Started with Apache Airflow: An Introduction to Data Orchestration"
description: "Airflow for Data Engineers"
dateString: March 2024
draft: false
weight: 106
cover:
    image: "/blog/airflow/airflowweb.png"
---
# What is Airflow?
"A platform created by community to programmatically author, schedule and monitor workflows."

- It's a job scheduler that run your tasks by obligating their execution dependencies.
- Workflows are written as code in the form of Directed Acyclic Graphs (DAGs)
- DAGs can be more dynamic, manageable, testable and collaborative.

### Use Cases
1. Transferring data between tasks.
2. Performing backups.
3. Automating DevOps operations.
4. Machine learning jobs.
5. Recommendation Engines.

### Problems with Conventional Schedulers
- Error Handling.
- Changes not traceable.
- Execution Dependency.
- Transparency.
- Task status tracking.
- Processing historic data.

### Benefits of Airflow
- Dynamic: 
- Extensible: Airflow provides a number of operators, and executors which supports almost every type of task execution, also we can define our own operators, executors and extend the library so that it fits the level of abstraction that suits your environment.
- Scalable:
- Configurable: Airflow is its highly configurable. Not only DAG customizations, it allows you to configure its core settings through a file called airflow.cfg.


### Terms in Airflow
- DAG: A DAG is unidirectional, acyclic graph connecting the edges, where each node in the graph is a task, and edges define dependencies amongst tasks.
- Operators: An operator represents a single task in a workflow that helps to carry out your task, Operators determine what actually gets to be done when your DAG runs.

# Architecture of Airflow
1. Metadata (Default: SQLite, Production: MySQL, Postgres)
2. Scheduler: Trigger the task on worker nodes.
3. Web Server/UI: Flast web application talking to Metadata.
4. Worker + Executor: (Different types of Executors: Sequential, Local, Celery, Dask, Mesos, Kubernetes)

## Installation using Docker

### What is Docker?
Docker is a containerization platform for building applications based on containers. Docker containers are also referred to as 'light-weight VMs'.

Docker compose is a tool for defining and running multi container docker applications.

clone the below git hub repository to your local machine.
URL - https://github.com/puckel/docker-airflow

Commands order
1. To run the docker compose:
docker-compose -f .\docker-compose-LocalExecutor.yml up -d

2. To check the present images in the system:
docker images

3. To check the running containers:
docker ps








### References
01. Apache Airflow | A Real-Time & Hands-On Course on Airflow - Udemy Course

# That’s it!

Happy Airflowing ..!

