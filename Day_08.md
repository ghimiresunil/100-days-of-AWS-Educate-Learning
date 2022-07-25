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

# 2.2.2 AWS Aurora
* It is a database engine developed in RDS.
* A fully managed relational database engine that's compatible with MySQL and PostgreSQL
* Aurora includes a high-performance storage subsystem. The underlying storage grows automatically as needed, up to 128 terabytes. The minimum storage is 10 GB.
* Aurora supports quick, efficient cloning operations
  * You can share your Amazon Aurora DB clusters with other AWS account for quick and efficient database cloning
* It is actually a spoke database engine developed by an Amazon.
* It was announced in re: invent 2014.
* It can run only on AWS infrastructure. It's not like a MySQL database that can be installed on a local device.
* It is a MySQL -compatible, relational database engine that combines the speed and availability of high-end commercial databases with the simplicity and cost-effectiveness of open source databases.
* It serves up to five times better performance than MySQL at a price one-tenth of that Commercial databases while delivering similar performance and availability.
* Aurora will keep your database up-to-date with the latest patches
* Aurora is fault-tolerant and self-healing

## AWS Aurora Features
* **High Performance and Scalability**
  * Up to 5x the throughput of MySQL and 3x the throughput of postgreSQL
  * Serverless Configuration
  * Push-button compute Scaling
  * Storage Auto-scaling
  * Low latency Read Replicas
  * Custom Database Endpoints
  * Parallel Query for Aurora MySQL
  * Diagnose and Resolve Performance Bottlenecks with Amazon DevOps Guru for RDS
* **High Availability and Durability**
  * Instance Monitoring and Repair
  * Multi-AZ Deployments with Aurora Replicas
  * Global Database
  * Fault-Tolerant and Self-Healing Storage
  * Automatic, Continuous, Incremental Backups and Point-n-Time Restore
  * Database Snapshots
  * Backtrack for Aurora MySQL
* **Highly Secure**
  * Network Isolation
  * Resource-level permissions
  * Encryption
  * Advanced Auditing
* **Fully Managed**
  * Easy to use
  * Monitoring and Metrics
  * Automatic Software Patching
  * DB Event Notifications
  * Fast Database Cloning
  * Database Start/Stop
* **Migration Support**
  * MySQL Database Migrations
  * PostgreSQL Database Migrations
  * Commericial Database Migrations
  * Babelfish for Aurora PostgreSQL
* **Cost-effectiveness**
  * Pay only for what you use
  * Optimize I/O costs
* **Developer Productivity**
  * Machine Learning
  * RDS Proxy Support

## 2.2.2.2 Drawnbacks of Amazon Aurora
* The source code is not available -- you can't see the code should you want/need/care to
* It's protocol compatible with mysql-5.6.10 - so if you need features in newer or older versions of mysql... you can't assume that Amazon will bring new MySQL features in a few months with a newer version of MySQL in RDS
* If, for whatever reason, you want to use MyISAM tables... you can't. Aurora only supports InnoDB
* You can't launch anything smaller than an r3.large with Aurora, so if you want smaller (cheaper) RDS databases, you'r back to MySQL

## 2.2.2.3 Advantage does Aurora have over RDS
RDS is the AWS managed database service. Within RDS you can specify MySQL, MariaDB, PostgreSQL, Oracle, Microsoft SQL Server or Aurora.

Oracle and Microsoft need licensing and MySQL, MariaDB& PostgreSQL are free of licensing costs (but they do have management costs).

Aurora is Amazon’s own DB and is much more scalable and redundant. It is 3 times faster than PostgreSQL and 5 times faster than MySQL and compatible with both of these database engines.

Because of this much better performance and ease of management, Aurora is charged for by Amazon.

So, if you are a start up, you can choose MySQL or PostgreSQL and pay nothing, but if you start to take off you can easily migrate to Aurora for better performance, availability and redundancy.
## 2.2.2.4 Usecases
* **Modernize enterprise applications**: Operate enterprise applications, such as customer relationship management (CRM), enterprise resource planning (ERP), supply chain, and billing applications, with high availability and performance.
* **Build SaaS applications**: Support reliable, high- performance, and multi-tenant Software-as a-Service (SaaS) applications with flexible instance and storage scaling.
* **Deploy globally distributed applications**: Develop internet-scale applications, such as mobile games, social media apps, and online services, that require multi-Region scalability and resilience.
* **Go serverless**: Hands-off capacity management, and pay only for capacity consumed with instantaneous and fine-grained scaling to save up to 90% of cost.

## 2.2.2.5. Pricing
* You are charged for DB instance hours, I/O requests, Backup storage and Data transfer.
* You can purchase On-Demand Instances and pay by the hour for the DB instance hours that you use, or Reserved Instances to reserve a DB instance for a one-year or three-year term and receive a significant discount compared to the on-demand DB instance pricing.
* Aurora PostgreSQL support for Kerberos and Microsoft Active Directory provides the benefits of single sign-on and centralized authentication of Aurora PostgreSQL database users. In addition to password-based and IAM-based authentication methods, you can also authenticate using AWS Managed Microsoft AD Service
