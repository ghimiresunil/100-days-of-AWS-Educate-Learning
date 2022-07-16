| Previous Learning | Link |
| ----------------- | ---  |
| 1. AWS Analytics Services | [Notes](https://github.com/ghimiresunil/100-days-of-AWS-Educate-Learning/blob/main/Day_02.md) |
| 1.1. Amazon Elastic Search | [Notes](https://github.com/ghimiresunil/100-days-of-AWS-Educate-Learning/blob/main/Day_02.md) |
| 1.2. Amazon Elastic MapReduce | [Notes](https://github.com/ghimiresunil/100-days-of-AWS-Educate-Learning/blob/main/Day_03.md) |
| 1.3. Amazon Kinesis | [Notes](https://github.com/ghimiresunil/100-days-of-AWS-Educate-Learning/blob/main/Day_04.md) |
| 1.4. Amazon Athena | [Notes](https://github.com/ghimiresunil/100-days-of-AWS-Educate-Learning/blob/main/Day_05.md) |

# 2. Amazon Database Service

AWS offers purpose-built databases for all your application needs. 

## 2.1. Database Services

|  Database Type| Definition | Uses Cases | AWS Service |
| :--------------: | ---------- | ----------- | ----------- |
| Relational | Store data with predefined schemas and relationships between them. These databases are designed to support ACID transactions, and maintain referential integrity and strong data consistency | Traditional applications, enterprise resource planning (ERP), customer relationship management (CRM), ecommerce | - AWS Aurora <br> - AWS RDS <br> - AWS Redshift | 
| Key-value | optimized for common access patterns, typically to store and retrieve large volumes of data. These databases deliver quick response times, even in extreme volumes of concurrent requests | High-traffic web applications, ecommerce systems, gaming applications | - Amazon DynamoDB |
| In-memory | Used for applications that require real-time access to data. By storing data directly in memory, these databases deliver microsecond latency to applications for whom millisecond latency is not enough. | Caching, session management, gaming leaderboards, geospatial applications | - AWS ElasticCache <br>  - Amazon MemoryDB for Redis|
| Document | Designed to store semistructured data as JSON-like documents. These databases help developers build and update applications quickly. | Content management, catalogs, user profiles | -  Amazon DocumentDB (with MongoDB compatibility)|
| Wide Column | Type of NoSQL database. It uses tables, rows, and columns, but unlike a relational database, the names and format of the columns can vary from row to row in the same table. | High-scale industrial apps for equipment maintenance, fleet management, and route optimization | - Amazon Keyspaces|
|Graph | Used for for applications that need to navigate and query millions of relationships between highly connected graph datasets with millisecond latency at large scale | Fraud detection, social networking, recommendation engines | - Amazon Neptune | 
| Time series | Time-series databases efficiently collect, synthesize, and derive insights from data that changes over time and with queries spanning time intervals | Internet of Things (IoT) applications, DevOps, industrial telemetry | -  Amazon Timestream |
| Ledger | Provide a centralized and trusted authority to maintain a scalable, immutable, and cryptographically verifiable record of transactions for every application | Systems of record, supply chain, registrations, banking transactions | - Amazon Ledger Database Services (QLDB) | 

Note: You would most likely have a database service that you can use. 

## 2.2 Uses Cases 
* Move to managed databases
* Build modern apps with purpose-built databases
* Break free from legacy databases


