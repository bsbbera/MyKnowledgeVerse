---
title: Spark-Memory Management
Created:
  - 2025-08-02
date modified: Tuesday, August 5th 2025, 11:47:30 pm
aliases: 
category: 
tags: 
status: new
banner:
---
---
> "Knowledge rests not upon truth alone, but upon error also.
>"
> <cite>— Carl Jung</cite>

---

## Memory Allocation

Assume you submitted a spark application in a YARN cluster. The YARN RM will allocate an application master (AM) container and start the driver JVM in the container. The driver will start with some memory allocation which you requested.



![[sparkMA.excalidraw|2000]]