# Amazon Athena is the fourth service in the analytics section

| Previous Learning | Link |
| ----------------- | ---  |
| 1. AWS Analytics Services | [Notes](https://github.com/ghimiresunil/100-days-of-AWS-Educate-Learning/blob/main/Day_02.md) |
| 1.1. Amazon Elastic Search | [Notes](https://github.com/ghimiresunil/100-days-of-AWS-Educate-Learning/blob/main/Day_02.md) |
| 1.2. Amazon Elastic MapReduce | [Notes](https://github.com/ghimiresunil/100-days-of-AWS-Educate-Learning/blob/main/Day_03.md) |
| 1.3. Amazon Kinesis | [Notes](https://github.com/ghimiresunil/100-days-of-AWS-Educate-Learning/blob/main/Day_04.md) |

## 1.4 AWS Athena
Amazon Athena is an interactive quert service that makes it easy to analyze data directly in Amazon Simple Storage Service (Amazon S3) using standard SQL. With a few actions in the AWS Management Console, you can point Athena at your code store in Amazon A3 and begin using standard SQL to run ad-hoc quries and get results in seconds.

Athena is serverless, so there is no infrastructure to set up or manage, and you pay only for the queries you run. Athena scales Automatically--executing queries in parallel--so resuts are fast, even with large datasets and compplex.

_**Athena in nutshell is:**_
* Serverless Interactive Query Platform
* Works on the data stored in S3
* Uses standard SQL for querying data
* Supports Variety of platform
  * CSV
  * JSON
  * Avro
  * ORC (Columnar)
  * Parquet (Columnar)
* Only Pay for querying data

### 1.4.1. Difference Between Microsoft SQL Server And Amazon Athena

| Features | Microsoft SQL Server | Amazon Athena |
| -------- | -------------------- | ------------- |
|**DEFINITION**| Database management and analysis system | Interactive query service that makes data analysis easy|
|**USAGE**| Used for Data Management Language (DML), Data Control Language (DCL), Data Definition Language (DDL), and Transaction Control Language (TCL)  | Used for Data Manipulation Language (DML) operations on Database|
|**BENEFITS**| - Reliable and easy to use <br> - High performance <br> - Easy to maintain <br> - Easy server installation <br> - Multiple tools integration possible | - Easy to use <br> - High performance <br> - No maintenance is required <br> - No server configuration is required <br> - Multiple tools integration possible|
|**INTEGRATION**| - Sequlize <br> - SQLDep <br> - Presto | - Amazon S3 <br> - AWS Glue <br> - Presto|
|**LIMITATIONS**| - Limited RDS storage <br> - Limited instances <br> - Can not handle recursion| - No DDLs supported <br> - Works with external table only  <br> - Defined User Functions not supported|

### 1.4.2. How do I start working with Athena?
Log in to the AWS Management Console for Athena and create your schema by writing DDL statements on the console or by using a create table wizard. You can then start querying data using a built-in query editor. Athena queries data directly from Amazon S3 so there’s no loading required

### 1.4.3. How does Amazon Athena Works?
Amazon Athena works directly with data stored in S3 Athena uses Prestro, a distributed SQL engine to run queries. It also uses Apache Hive to create, drop, and alter **tables** and **partitions**. 

### 1.4.4. What is the cost of Amazon Athena?
it is priced per query $5.00(per TB) of data scanned depending on the region

### 1.4.5.  How do you access Amazon Athena?
Amazon Athena can be accessed via the AWS Management Console, an API, or an ODBC or JDBC driver. You can programmatically run queries, add tables or partitions using the ODBC or JDBC driver.

### 1.4.6. Pros of Athena

* **Easy Implementation**: Athena does not require installation, and it can also be accessed by the AWS CLI directly from the AWS console.
* **Serverless**: It is serverless, so the end-user does not need to worry about infrastructure, configuration, scaling, or failure. Athena takes care of everything herself
* **Pay Per Query**: Athena charges you only for the Query you run, i.e., the amount of data managed per Query. You can save a lot if you can compress them and format your dataset accordingly
* **Fast**: Athena is a very fast analysis tool. It can execute complex queries quickly by breaking them down into simpler queries and running them in parallel, then combining the results to give the desired output
* **Secure**: With the help of IAM policies and AWS identities, Athena gives you complete control over the data set. Since data is stored in S3 buckets, IAM policies can help you manage users' controls
* **Highly Available**: With the assurance of AWS, Athena is highly available, and the user can execute queries round the clock. As is AWS 99.999% available, so is Athena
* **Integration**: The best feature of Athena is that it can be integrated with AWS Glue. AWS Glue will help the user to build a better-integrated data repository. It helps you create better versions of data, better tables, views, etc
* **Flexibility**: Amazon Athena's open and versatile architecture doesn't limit you to any specific vendor, technology, or device. For example, you can work with a wide range of open-source file formats and freely switch between query engines without adjusting schemas.

### 1.4.7. Cons of AWS Athena

* **No Data Optimizatio**n: AWS Athena doesn't offer a lot of customization capabilities. The farthest you can go here is to optimize the queries - not the underlying data. Even when you try to replace Amazon S3 data using AWS Glue, you still need to be careful not to harm other services that access the same data.
* **Shared Resources**: According to Amazon's Service Level Agreement (SLA), all AWS Athena users worldwide share the same resource when running their queries. This multi-tenancy approach can trigger resource stress from time to time, leading to fluctuating query performance.
* **Reduction in data manipulation operations**: AWS Athena is just a query service, and you will find only one query engine here. It does not come with a built-in Data Manipulation Language (DML) interface for inserting, deleting, and updating data.
* **Requires data partitioning**: If you intend to run your SQL queries efficiently, you may want to partition the data sets stored in Amazon S3. The number of partitions you have to create will affect the speed and performance of your queries to a great extent. For example, every 500 partitions scanned will increase your query time by one second.
* **Lack of indices**: While indexing has always been a built-in provision in traditional databases, you do not get this privilege with AWS Athena. As such, you should expect challenges in operations such as consolidating large tables.
