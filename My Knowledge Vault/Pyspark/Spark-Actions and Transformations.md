---
Created:
  - 2025-07-21
date modified: Monday, July 21st 2025, 10:39:21 pm
aliases:
  - Actions
  - Transformations
  - pyspark
title: Spark-Actions and Transformations
category: Data Engineering
tags:
  - spark
  - pyspark
  - DataEngineering
  - interview/pyspark
status: new
---
> "Don't judge each day by the harvest you reap but by the seeds you plant."
> <cite>— Robert Stevenson</cite>

---

## Transformations

It is a function that produces a _new RDD_ from _Existing RDD_. It takes RDD as an input and generates new RDD as an output. There is two type of Transformations

#### Narrow Transformation

"Narrow Transformation" refers to an operation on a dataset where each input partition contributes only to a small number of output partitions. Narrow transformations do not require shuffling or reorganizing of data across partitions because the operation can be applied locally within each partition.

- Map()
- Flatmap()
- Filer()
- Union()
- Sample()


<div class="image-row large" style="max-width: 1200px;">
  <figure>
    <img src="asset/Narraow Transformations.png">
    <figcaption>Narraow Transformations</figcaption>
  </figure>
    <figure>
    <img src="asset/Wide Transformations.png">
    <figcaption>Wide Transformations</figcaption>
  </figure>
</div>

#### Wide Transformations

"Wide Transformation" involves operations on data that may require shuffling and redistribution of data across partitions. Unlike narrow transformations, which can be applied independently within each partition, wide transformations involve operations that require coordination and communication among partitions to produce the result. All the elements that are required to compute the records in a single partition may live in many partitions of the parent RDD.

- Reduce by key
- Group by key
- Join
- Cartesian join
- Repartition
- Coalesce

## Actions

Actions are operations that trigger the execution of the computation plan defined by transformations on distributed datasets (RDDs, DataFrames, or Datasets). Actions instruct Spark to perform computations and return results either to the driver program or to external storage systems. Action is one way of sending data from the executor to the driver. 

- Count()
- Collect()
- Take(n)
- Top()
- Reduce()
- Aggregate()
- Foreach()