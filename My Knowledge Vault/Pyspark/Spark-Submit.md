---
title: Spark-Submit
Created:
  - 2025-08-01
date modified: Saturday, August 2nd 2025, 12:43:40 pm
aliases:
  - Job Submit
category: Data Engineering
tags:
  - spark
  - pyspark
  - interview/pyspark
  - DataEngineering
status: new
banner: abstract HD
---
---
> "The smallest flower is a thought, a life answering to some feature of the Great Whole, of whom they have a persistent intuition.
>"
> <cite>— Honore de Balzac</cite>

---

## What is spark submit?

The Spark Submit is a command-line tool that allows you to submit the Spark application to the cluster.

		--class                    Not Applicable for Pyspark
		--master                   yarn, local[3]
	    --deploy-mode              Client/Cluster
	    --conf                     spark.executor.memoryOverhead = 0.20
	    --driver-cores             2
	    --driver-memory            8G
	    --num-executor             4
	    --executor-cores           4
	    --executor-memory          16G

## Types of Deploy Mode

The Spark Submit allows you to submit the spark application to the cluster, and you can apply to run in one of the two modes.

##### Cluster Mode

In the cluster mode, Spark Submit will reach the YARN RM, requesting it to start the driver in an AM container. YARN will start your driver in the AM container on a worker node in the cluster. 

Then the driver will again request YARN to begin executor containers. So, the YARN will start executor containers and hand them over to the driver. So, in cluster mode, your driver is running in the AM container on a worker node in cluster. Your executors are also running in the executor containers on some worker nodes in cluster.

![[Spark_Submit.excalidraw | 1000]]

##### Client Mode

In the Client Mode, Spark Submit doesn’t go to the YARN resource manager for starting an AM container. Instead, the spark-submit command will start the driver JVM directly on the client machine. So, in this case, the spark driver is a JVM application running on your client machine. Now the driver will reach out to the YARN resource manager requesting executor containers. The YARN RM will start executor containers and hand them over to the driver. The driver will start executors in those containers to do the job.


## How do we choose the deploy mode?

You will almost always submit your application in cluster mode. It is unlikely that you submit your spark application in client mode. We have two clear advantages of running your application in cluster mode. 
1. The cluster mode allows you to submit the application and log off from the client machine, as the driver and executors run on the cluster. They have nothing active on your client’s machine. So, even if you log off from your client machine, the driver and executor will continue to run in the cluster. 
2. Your application runs faster in cluster mode because your driver is closer to the executors. The driver and executor communicate heavily, and you don’t get impacted by network latency, if they are close. 

The designed client mode is for interactive workloads. For example, Spark Shell runs your code in client mode. Similarly, Spark notebooks also use the client mode.