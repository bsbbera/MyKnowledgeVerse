---
title: Spark-Jobs
Created:
  - 2025-07-31
date modified: Friday, August 1st 2025, 9:07:32 pm
aliases:
  - Spark Submit
  - Data Enginnering
category: Data Engineering
tags:
  - spark
  - pyspark
  - interview/pyspark
  - DataEngineering
status: new
banner: https://images.pexels.com/photos/3186949/pexels-photo-3186949.jpeg
---
---
> "I am not bothered by the fact that I am unknown. I am bothered when I do not know others.
>"
> <cite>— Confucius</cite>

---

## Stage, Shuffle, Tasks, Slots

1. Spark creates one job for each [[Spark-Actions and Transformations | Actions]].
2. This job may contain a series of multiple [[Spark-Actions and Transformations | Transformations]].. 
3. The Spark engine will optimize those transformations and creates a logical plan for the job. 
4. Then spark will break the logical plan at the end of every wide dependency and create two or more stages. 
5. If you do not have a wide dependency, your plan will be a single stage plan. 
6. But if you have N wide-dependencies, your plan should have N+1 stages. 
7. Data from one stage to another stage is shared using the shuffle/sort operation. 
8. Now each stage may be executed as one or more parallel tasks. 
9. The number of tasks in the stage is equal to the number of input partitions.


![[Spark Jobs.excalidraw|700]]

The task is the most critical concept for a Spark job and is the smallest unit of work in a Spark job. The Spark driver assigns these tasks to the executors and asks them to do the work. The executor needs the following things to perform the task. 
1. The task Code 
2. Data Partition 

So, the driver is responsible for assigning a task to the executor. The executor will ask for the code or API to be executed for the task. It will also ask for the data frame partition on which to execute the given code. The application driver facilitates both these things for the executor, and the executor performs the task. 

Now, let’s assume I have a driver and four executors. Each executor will have one JVM process. But I assigned 4 CPU cores to each executor. So, my Executor JVM can create four parallel threads and that’s the slot capacity of my executor. 

So, each executor can have four parallel threads, and we call them executor slots. The driver knows how many slots we have at each executor and it is going to assign tasks to fit in the executor slots. The last stage will send the result back to the driver over the network. The driver will collect data from all the tasks and present it to you.


#### Read Also
- [[Spark-Architecture]]
- [[Pyspark Interview questions]]