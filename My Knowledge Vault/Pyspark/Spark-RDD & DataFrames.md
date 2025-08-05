---
Created:
  - 2025-07-21
date modified: Thursday, July 31st 2025, 10:06:19 pm
aliases:
  - Spark dataframes
title: Spark-RDD & DataFrames
category: Data Engineering
tags:
  - pyspark
  - spark
  - interview/pyspark
  - DataEngineering
status: new
---
---
> "Translation is the paradigm, the exemplar of all writing. It is translation that demonstrates most vividly the yearning for transformation that underlies every act involving speech, that supremely human gift."
> <cite>— Harry Burchell Mathews</cite>

---

## Resilient Distributed Dataset(RDD)

RDD are the main logical data units in spark. They are distributed collection of objects, which are stored in memory or on disks of different machines on cluster.

- ***Resilience***: RDDs tract data lineage information (lineage Graph) to recover from failed state automatically. It is also known as fault tolerance.
- ***Distributed***: Data present in an RDD resides on multiple nodes. 
- ***Lazy Evaluation***: Data does not get loaded in an RDD even if you define it. 
- ***Immutability***: Data stored in an RDD is in the read-only mode. You cannot edit the data which is present in RDD. 
- ***In-Memory Computation***: An RDD stores any intermediate data that is generated in the RAM so that faster access can be provided.


## Spark Dataframes

- Higher-level abstractions than RDD. 
- Distributed collection of data organized into named columns (schema).
	- Like a table in a relational database.
- Simplifies data processing.
- Excellent for processing semi & structured data, such as CSV, JSON, Parquet, Avro and more.
- Support filters, aggregations, joins, etc.!
- It uses Spark Query Optimizer.



![[Pyspark DataStructure.excalidraw | 5000]]

## Spark Datasets

- Distributed collection of data.
- Higher abstraction on top of RDDs and DataFrames.

## When to use what? 

-  **RDD are better for low-level**. 
	- Unstructured data
	- No schema validation
- **DataFrames and Datasets are better for: **
	- Semi-structured data
	- Schema validation