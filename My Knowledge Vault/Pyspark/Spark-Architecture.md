---
banner: https://quintagroup.com/services/service-images/apache-spark-python-pyspark.jpg
Created:
  - 2025-07-21T13:57:00
date modified: Friday, August 1st 2025, 8:50:33 pm
aliases:
  - pyspark
  - spark
title: Spark-Architecture
category: Data Engineering
tags:
  - pyspark
  - spark
  - interview/pyspark
  - DataEngineering
status: new
banner-radius: 0
banner-fade: -90
content-start: 306
banner-height: 290
---
---
> "A life spent making mistakes is not only more honorable but more useful than a life spent in doing nothing."
> <cite>— Bernard Shaw</cite>

---

## What is pyspark?

Apache Spark is written in Scala programming language. PySpark has been released in order to support the collaboration of Apache Spark and Python, it actually is a Python API for Spark. In addition, PySpark, helps you interface with Resilient Distributed Datasets (RDDs) in Apache Spark and Python programming language. This has been achieved by taking advantage of the Py4j library.

Py4J is a popular library which is integrated within PySpark and allows python to dynamically interface with JVM objects. PySpark features quite a few libraries for writing efficient programs. Furthermore, there are various external libraries that are also compatible. Here are some of them

![[pysparkArchitecture.png]]

## Main Components

There are majorly 5 components of a pyspark. 
#### 1. Spark Driver Program

- Its acts like a main method which will create spark context.
- The First method which will be created.
- Coordinates and executes Spark applications.
- Runs on master node. 
- Creates the execution plan.
- Distributes and coordinate tasks across worker nodes. 
- Tracks the progress and status of tasks. 
- It handles failures and retires for fault tolerance.

#### 2. Spark Context and Spark Session

- It is the entry point to spark core of spark application.
- It will connect our spark application with execution environment or cluster. 
- Interface for creating RDD’s and executing Spark operations. 
- It manages the distribution of tasks, resource allocation, and fault tolerance mechanisms. 
- Provides a unified programming API for various programming languages. E.g., Scala, java, python, and R. 
- Handles the configuration of Spark application properties and environment settings. 
- Controls the parallelism and data partitioning, optimizing data processing across multiple nodes in a cluster. 
- It enables the caching and persistence of intermediate data in memory or on disk.
- Integrates with various data sources, file systems, and third-party libraries (diverse formats). 
- Monitoring management for Spark applications, job progress, resource usage, and execution metrics.
- It creates job execution graphs, manages partitions, scheduling etc... 
- Before Spark 2.0.0 Spark context was used separately 
- After Spark 2.0.0 + Spark session does all the thing.

#### 3. Cluster Managers

- Used for managing Nodes and assigning tasks. 
- Responsible for acquiring resources for application. 
- Allows for efficient use of resources.

###### Type of Cluster Manager

**Standalone:** Built in for testing and developments.
**Apache Mesos:** General purpose able to run multiple applications frameworks on a shared resource pool.
**Hadoop YARN:** Part of Hadoop ecosystem to manage resources.
**Kubernetes:** Container Orchestration used for managing cluster.

#### 4. Executors

- Responsible for executing tasks.
- Through lifetime of the application.
- Own JVM process.
- Executing subset of tasks.
- More Executors -> parallelism -> better performance.

#### 5. Tasks

- The smallest unit of execution is known as Task.
- Each task will process one data partition.
- One task will be executing on one CPU core.
- One executor can run multiple tasks equal to the number of CPU cores.


## Clients

Spark clients Can be any machine from where we are sending our spark job for execution. Remote server, web interface like Data Stax, Hue.

## Resource Manager

- It will create one container and start Application Master Service in it. 
- Application master will request to resource manager for complete resource allocation or to start the required executors.
- Executors:
	- Virtual Entity which will have CPU, Memory, Network Bandwidth
	- Executors do the actual computation on partitioned data.
- The Resource Manager will create required number of executors for processing.
- Executors will start interacting with the Driver program to send the updates for Job progress and other meta data information.

