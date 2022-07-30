| Previous Learning | Link |
| ----------------- | ---  |
| 1. AWS Analytics Services | [Notes](https://github.com/ghimiresunil/100-days-of-AWS-Educate-Learning/blob/main/Day_02.md) |
| 1.1. Amazon Elastic Search | [Notes](https://github.com/ghimiresunil/100-days-of-AWS-Educate-Learning/blob/main/Day_02.md) |
| 1.2. Amazon Elastic MapReduce | [Notes](https://github.com/ghimiresunil/100-days-of-AWS-Educate-Learning/blob/main/Day_03.md) |
| 1.3. Amazon Kinesis | [Notes](https://github.com/ghimiresunil/100-days-of-AWS-Educate-Learning/blob/main/Day_04.md) |
| 1.4. Amazon Athena | [Notes](https://github.com/ghimiresunil/100-days-of-AWS-Educate-Learning/blob/main/Day_05.md) |
| 2. Amazon Database Service | [Notes](https://github.com/ghimiresunil/100-days-of-AWS-Educate-Learning/blob/main/Day_06_07.md)|
| 2.1. Database Services | [Notes](https://github.com/ghimiresunil/100-days-of-AWS-Educate-Learning/blob/main/Day_06_07.md)|
| 2.1. Use Cases | [Notes](https://github.com/ghimiresunil/100-days-of-AWS-Educate-Learning/blob/main/Day_06_07.md)|
| 2.2.1. Amazon Relational Database Service| [Notes](https://github.com/ghimiresunil/100-days-of-AWS-Educate-Learning/blob/main/Day_06_07.md)|
| 2.2.2. Amazon AWS Aurora| [Notes](https://github.com/ghimiresunil/100-days-of-AWS-Educate-Learning/blob/main/Day_08.md)|

# 2.2.3. AWS ElastiCache

- ElastiCache is a distributed in-memory cache environment in the AWS Cloud
- ElastiCache works with both the Redis and Memcached engines
- Amazon ElastiCache is a web service that makes it easy to deploy, operate, and scale on in-memory cache in the cloud. It is popular choice for real time use cases like caching, session, stores, gaming, real-time analytics, and queuing.
- Amazon ElastiCache offers fully managed Redis, voted the most loved database by developers in the stack-overflow 2020 survery and MemCached for your most demanding applications that require sub-millisecond reponse time.
- It improves the performance of web applications by allowing you to retrieve information from fast, managed in-memory cache instead of relying entirely on slower disk-based databases.
- It is used to improve latency and throughput for many read-heavy application workloads (such as social networking, gaming, media sharing, and Q&A portals) or compute intensive workloads (such as a recommendation engine).
- Caching improves application performance by storing critical pieces of data in memory for low latency access.
- Cached information may include the results of I/O-intensive database queries or the results of computationally-intensive calculations.

## 2.2.3.1. Types of ElastiCache

- Memcached
  - Memcached-compatible in-memory key-value store service which will be used as a cache.
  - Easy-to-use, high performance, in-memory data store. 
  - Used as a cache or session store
  - Used in real-time applications such as Web, Mobile Apps, Gaming, Ad-Tech, and E-Commerce
  - **Benefits of Memcached**
    - Sub-millisecond response times
    - Simplicity
    - Scalability
    - Community
  - **Following are the use cases of Memcached**
    - Caching
    - Session store
- Redis
  - Redis stands for Remote Dictionary Server.
  - Fast, open-source, and in-memory key-value data store
  - Its response time is in a millisecond, and also serves the millions of requests per second for real-time applications such as Gaming, AdTech, Financial services, Health care, and IoT.
  - Used for caching, session management, gaming, leaderboards, real-time analytics, geospatial, etc.
  - **Benefits of Redis**
    - In-memory data store
    - Flexible data structures
    - Simplicity
    - Replication and Persistence
    - High availability and scalability
    - Extensibility

#### 2.2.3.1.1. Differences between Memcached and Redis

| Basis for Comparison | Memcached | Redis|
| -------------------- | ---------- | ---- |
| Sub-millisecond latency | Its response time is in sub-millisecond as it stores the data in memory which reads the data more quickly than disk. | Its response time is in sub-millisecond as it stores the data in memory which read the data more quickly than disk.|
| Developer ease of use	| Its syntax is simple to understand and use.	| Its syntax is simple to understand and use.|
| Distributed architecture	| Its distributed architecture distributes the data across multiple nodes which allows to scale out more data when demand grows.	| Its distributed architecture distributes the data across multiple nodes which allows to scale out more data when demand grows.|
| Supports many different programming languages	| It supports languages such as C, C++, java, python, etc.	| It supports languages such as C, C++, java, python, etc.|
| Advanced data structure	| It does not support advanced data structures.	| It supports various advanced data structures such as sets, sorted set, hashes, bit arrays, etc.|
| Multithreaded Architecture	| It supports multithreaded architecture means that it has multiple processing cores. This allows you to handle multiple operations by scaling up the compute capacity.	 | It does not support multithreaded architecture.|
| Snapshots | It does not support the snapshots.	| Redis also keeps the data in a disk as a point-in-time backup to recover from the fault. |
| Replication | It does not replicate the data.	| It provides a primary replica architecture that replicates the data across multiple servers and scales the database reads.| 
| Transactions | It does not support transactions.	| It supports transactions that let to execute a group of commands.|
| Lua Scripting	 | It does not support Lua Scripting.	| It allows you to execute Lua Scripts which boost performance and simplify the application. |
| Geospatial support	| It does not provide Geospatial support.	| It has purpose-built commands that work with geospatial data, i.e, you can find the distance between two elements or finding all the elements within a given distance.|

## 2.2.3.2. Pricing

- With on-demand nodes you pay only for the resources you consume by the hour without any long-term commitments.
- With Reserved Nodes, you can make a low, one-time, up-front payment for each node you wish to reserve for a 1 or 3 year term. In return, you receive a significant discount off the ongoing hourly usage rate for the Node(s) you reserve.
- ElastiCache provides storage space for one snapshot free of charge for each active ElastiCache for Redis cluster. Additional backup storage is charged.
- EC2 Regional Data Transfer charges apply when transferring data between an EC2 instance and an ElastiCache Node in different Availability Zones of the same Region.
