# Amazon Kinesis is the third service in the analytics section

| Previous Learning | Link |
| ----------------- | ---  |
| 1. AWS Analytics Services | [Notes](https://github.com/ghimiresunil/100-days-of-AWS-Educate-Learning/blob/main/Day_02.md) |
| 1.1. Amazon Elastic Search | [Notes](https://github.com/ghimiresunil/100-days-of-AWS-Educate-Learning/blob/main/Day_02.md) |
| 1.2. Amazon Elastic MapReduce | [Notes](https://github.com/ghimiresunil/100-days-of-AWS-Educate-Learning/blob/main/Day_03.md) |

## 1.3. Amazon Kinesis

Before knowing about the Kinesis, question may arise in mind, what is streaming data?

### 1.3.1. Streaming Data

Data that is generated continously by thousands of data sources, which typically send in data records simulatneously, in small sizes(order of kilobytes).

For Example: Consider Uber engineering team to be using kinesis for customer analytics where they want to analyze customer trends.

They would using streaming data for all customers in a geographic zone to callibrate the usage and in cancellations by drivers/customers. This would be a typical case where kinesis would be used, other applications would be IoT sensor data, Social Network Data, Game Data, and Stock market data streaming and analysis.

### 1.3.2. Kinesis

Kinesis is an AWS Service for processing big data in real time. It is fully managed and runs your streaming applications without requiring you to manage any infrastructure based on business needs. Amazon Kinesis is scalable as it can handle any amount of data streaming data and process data with very low latencies.

Amazon Kinesis makes it easy to ingest real-time data such as audio, video, website clickstreams.

With AWS Kinesis, one can keep track of all the operational activities by analyzing the data and taking decisive actions instantly.

### 1.3.3. Why Amazon Kinesis?
* Real-time processing: It allows to collect & analyze information in real-time like stock trade prices otherwise we need to wait for data-out report.
* Easy to use: Using Amazon Kinesis, we can create a new stream, set its requirements, & start streaming data quickly.
* High throughput, elastic: It allows to collect & analyze information in real-time like stock trade prices otherwise we need to wait for data-out report.
* Integrate with other Amazon services: It can be integrated with Amazon Redshift, Amazon S3 & Amazon DynamoDB.
* Build kinesis applications: Amazon Kinesis provides the developers with client libraries that enable the design & operation of real-time data processing applications. Add the Amazon Kinesis Client Library to Java application & it will notify when new data is available for processing.
* Cost-efficient: Amazon Kinesis is economical for workloads of any scale. Pay as we go for the resources used & pay hourly for the throughput required.

### 1.3.4. Uses:
* Kinesis Data Streams can be used to collect log and events data from sources such as servers, desktops, and mobile devices.
* You can build kinesis applications to continously process the data, generate metrics, power live dashboard, and emit aggregated data into stores such as Amazon S3.

### 1.3.5. Core Service of Kinesis
* Kinesis Data Stream:
A Kinesis data stream is a set of shards. Each shard has a sequence of data records. Each data record has a sequence number that is assigned by Kinesis Data Streams.

  * Scalable and durable real-time data steaming service that can continuously capture Gigabytes of data per second from thousands of sources.
  * Continuously capture gigabytes of _data per second_ from hundreds of thousands of sources such as website clickstreams, data event streams, financial transactions, social media feeds, IT logs, and location-tracking events
  * The _collected data is available in milliseconds_ to enable real-time analytics use cases such as real-time dashboards, real-time anomaly detection, dynamic pricing, and more

* Kinesis Video Streams:
Kinesis Video Streams makes it easy to securely stream video from connected devices to AWS for analytics, machine learning (ML), and other processing. It durably stores, encrypts, and indexes video data streams, and allows access to data through easy-to-use APIs.
  * Securely stream videos from device to AWS for Analytics, ML and other processing
  * Automatically provisions and scales the infrastructure to ingest video data from millions of devices
  * Stores, Encrpts, and Indexes video data in your streams, and can be accessed using APIs.
  * Example - Live on YouTube, video calls etc..
  * Kinesis Video Streams can ingest data from edge devices, smartphones, security cameras, and other data sources such as RADARs, LIDARs, drones, satellites, dash cams, and depth-sensors.

* Kinesis Data Firehose:
Kinesis Data Firehose is the easiest way to load streaming data into data stores and analytics tools. It captures, transforms and loads streaming data.
  * Load streamaing data into data lakes, data stores, and analytics services
  * It can capture, transform, and deliver streaming data to Amazon S3, Amazon Redshift, Amazon Elasticsearch service generic HTTP endpoints, and service providers like Datadog, New Relic, MongoDB, and Splunk
  * it loads new data into your destinations within **60 seconds** after the data is sent to the service
  * Pay as you go model and its fullly AWS managed
  * Use-case-IOT Analytics, Clickstream Analytics, Log Analytics, Security Monitoring

* Kinesis Data Analytics:
Amazon Kinesis Data Analytics is the easiest way to process and analyze real-time, streaming data. One can use standard SQL queries to process Kinesis data streams
  * Amazon Kinesis Data Analytics is the easiest way to transform and analyze streaming data in real time with Apache Flink
  * Apache Flink is an open source framework and engine for processsing data streams


### 1.3.6. Differences between Kinesis Streams & Kinesis Firehose
* Kinesis stream is manually managed while Kinesis Firehose is fully automated managed.
* Kinesis stream sends the data to many services while Kinesis Firehose sends the data only to S3 or Redshift.
* Kinesis stream consists of an automatic retention window whose default time is 24 hours and can be extended to 7 days while Kinesis Firehose does not have automatic retention window.
* Kinesis streams send the data to consumers for analyzing and processing while kinesis firehose does not have to worry about consumers as kinesis firehose itself analyzes the data by using a lambda function.
