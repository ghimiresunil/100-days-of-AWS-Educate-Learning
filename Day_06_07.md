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

### 2.2.1. Amazon Relational Database Service

**Amazon Relational Database (RDS)** refers to a cloud infrastructure allowing the creation and maintenance of relational databases. It also helps in management tasks like migration, backup, recovery, and patching. Futhermore, the RDS instance is employed to spice up your database query bandwidth.

#### Features of Amazon RDS:
* **Inexpensive**: As we only buy the consumed resources with no long-term commitment. So, it is inexpensive.
* **Scalable**: With aws management console or RDS specific API, we will increase or decrease the RDS requirements within minutes.
* **Backup**: Additionally, Amazon RDS backups everything within the database and also provides automatic timing backups.
* **Secure**: It also provides complete control over the network to access databases and related services.
* **Host replacement**: For reference, just in case of failure of RDS hardware, then it’ll get replaced automatically by amazon.

#### Benefits of AWS RDS
* **Reduced Administration Burden**: The database can be deployed easily from project creation to implementation through the use of RDS.
* **Cost-effective**: You just pay for what you use, and nothing more. No upfront payment requires, just the monthly usage payment.
* **Security**: Using AWS Key Management Service (KMS), you can create encryption keys for maintaining security and authorized access to your database.
* **High Availability and Durability**: The automated recovery feature of RDS enables point-in-time recovery for your database instance.
* **Scalability** – Moreover, it just takes a few minutes to scale your infrastructure up or down, and you can scale up to a maximum of 32 vCPUs and 244 GiB.
* **Free Tier** – Therefore, In addition to the above benefits AWS also gives you a free tier usage of Amazon RDS for 750 hours/month for 12 months.

#### Drawbacks of Amazon RDS
* **Lack of root access**. Because it is a managed service, users do not have root access to the server running RDS. RDS restricts access for certain procedures to those with advanced privileges.
* **Downtime**. Systems must go offline for some patching and scaling procedures. The timing on these processes varies. With scaling, compute resources need a few minutes downtime on average.

#### Database Engines That Are Managed By RDS

* **Amazon Aurora**: relational database engine built by amazon. That blends high-end commercial database speed and reliability with the flexibility and cost-effectiveness of an open-source database.
* **PostgreSQL**: open-source database management system that uses SQL to access the data.
* **SQL Server**: Relational Database Management System, which was developed by Microsoft in 2005. Amazon RDS for SQL Server makes it easy to set up, operate, and scale SQL Server deployments in the cloud. In addition, with Amazon RDS, you can deploy multiple editions of SQL Server.
* **Oracle**: Object-relational database management system that was developed by Oracle Inc.
* **MariaDB**: Community-developed fork of MySQL DBMS. The reason for its fork was the concern over the acquisition of Oracle over MySQL
* **My SQL**: World’s most popular open source relational database. Amazon RDS makes it easy to set up, operate, and scale MySQL deployments in the cloud. With Amazon RDS, you can deploy scalable MySQL servers in minutes with cost-efficient and resizable hardware capacity.

#### Cost Of Amazon Relational Database Service

In RDS, the Billing depends on the subsequent criteria:

* Instance Class – Pricing depends on the consumption class of DB Instance.
* Running Time – Pricing depends on the instance hour, like one instance running per hour.
* Storage – Bill is calculated on the basis of a storage capacity plan (mainly in GBs).
* I/O Requests – It includes the total no. of storage I/O requests made during a billing cycle.
* Backup Storage – there are no additional charges for backup storage upto 100% of the database, free just for active DB Instance.

Amazon RDS provides the subsequent purchasing options to enable you to optimize your costs as per your needs:

* **On-Demand Instances** – Pay by the hour for the DB instance hours that you simply use. Pricing depends on a per-hour basis, but bills are calculated right down to the second and show times in decimal form. Likewise, RDS usage is now billed in a second increment, with a minimum of 10 minutes.
* **Reserved Instances** – Reserve a DB instance for a one-year or three-year term and obtain a big discount compared to the on-demand DB instance pricing. With Reserved Instance usage, you’ll launch, delete, start, or stop multiple instances within an hour and obtain the Reserved Instance benefit for all of the instances.

#### Free-Tier Policy With Amazon

AWS has an amazing free tier policy so that the user can use the service first and then do the necessary. Similarly, it offers a free tier policy for AWS RDS, which includes the following benefits:

* 750 hours of Amazon RDS usage in single-AZ for db.t2.micro instance, every month for one year from signup.
* 20 GB of DataBase Storage: any combination of General Purpose (SSD) or Magnetic storage.
* 10 million IOs.
* 20GB of backup storage.

#### Amazon RDS use cases
* Online retailing
* Mobile and online gaming
* Travel applications
* Streaming applications
* Finance applications
