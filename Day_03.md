# Amazon Elastic MapReduce is the second service in the analytics section

| Previous Learning | Link |
| ----------------- | ---  |
| 1. AWS Analytics Services | [Notes](https://github.com/ghimiresunil/100-days-of-AWS-Educate-Learning/blob/main/Day_02.md) |
| 1.1. Amazon Elastic Search | [Notes](https://github.com/ghimiresunil/100-days-of-AWS-Educate-Learning/blob/main/Day_02.md) |

## 1.2 Amazon EMR
Amazon EMR can be beneficial to many companies who want to work on collecting and analyzing large sets of data. Data is king in much of the world around us today and knowing how to not only collect it, but sort through and understand it, is key. Amazon EMR allows companies to do just that. Whether your company is big or small, or has a lot of data to get through, Amazon EMR can provide the right solutions, and the right price, to get things done.
It provides these companies with managed framework using Hadoop, along with the elastic infrastructure of Amazon EC2 and Amazon S3. 

A cluster is the central components of Amazon EMR. A cluster is a collection of EC2 instances. An instance within a cluster is called a node. An Amazon EMR installs softwaare components for each node. Each node is assigned a role, known as nodeype.

**Note**: MapReduce is a software framework that allows developers to write programs that process massive amounts of unstructured data in parallel across a distributed cluster of processors or stand-alone computer. 

The following are the node types:
* Master node <br>
The master node manages the software components that distribute task along the other nodes of a cluster. It monitors and tracks the health of the cluster, as well as status of each task.

* Core node <br>
The core node manages the software components that process the tasks and stores data in HDFS. Multi-node clusters will at least have one core node.

* Task node <br>
Task nodes with software components process the task, but do not store data n HDFS

### 1.2.1. What do I need to build a cluster?
* Choose instances
* Choose your software
* Choose your access method

### 1.2.2. AWS EMR cluster has following cluster states
* STARTING – In this state, cluster provisions, starts, and configures EC2 instances
* BOOTSTRAPPING – In this state cluster is executing the Bootstrap process
* RUNNING – State in which cluster is currently being run
* WAITING – In this state cluster is currently active, but there are no steps to run
* TERMINATING - Shut down of cluster has started
* TERMINATED - The cluster is shut down without any error
* TERMINATED_WITH_ERRORS - The cluster is shut down with errors

### 1.2.3. Things that you can do with the help of Amazon EMR include:
* Real-time analytics: When working with this feature, the user can use and process any of the data they have in real-time. This helps them to gather up the data and see the results as soon as possible, rather than waiting days or weeks. In a world where things change overnight, this can be a critical benefit.
* Clickstream analysis: If you are interested in working with advertisements then this is a great feature found in Amazon EMR. For example, this product will use data from Clickstream before analyzing it to make useful and effective advertisements. This ensures your ads are more likely to reach the target audience and bring you sales than ever before.
* Log Analysis: Depending on the type of cloud you choose to use, log processing may be a critical component of your business. Amazon EMR makes it easier to do, whether you want to track mobile or web use, or both. This data can then be converted over into useful insights that your business can look over.
* Extract the Transform Load: This is a great tool to use if you need to quickly sort through and handle new data that is coming in. This is true even if the data set is very large.
* Helps with predictive analytics: Part of using all this big data is for companies to learn what their customers like and want, and use that to make predictions about the future. Amazon EMR provides the tools to look through the data and form these predictions as accurately as possible. In fact, it includes MLlib to provide your business with machine learning algorithms, or you can use some of your own favorite libraries.
* Genomics: Finally, Amazon EMR will often help with immense amounts of genomic data and can help with giant scientific information sets as quickly as possible. This is often a huge amount of data, more than most companies must face, and it's hard to find other platforms that can handle it. Amazon EMR will actually provide access to genomic data hosted for free when it is done through Amazon Web Services.

### 1.2.4. Benefits that a company will enjoy when choosing Amazon EMR
* Elastic: Thanks to the addition of Amazon Elastic MapReduce, any user has the ability to monitor all of the instances of data processing. You can even add in Amazon AutoScaling to modify how many instances happen automatically. You can do this manually too if you need to reduce costs.
* Economical: Compared to most other options, Amazon EMR is economical. In fact, you can complete a Hadoop cluster of 10-nodes for $0.15 an hour. This can save you 50% or more on your costs.
* Secure: All of Amazon’s sites and products have security in mind and Amazon EMR is no different. You can turn on the firewall to add more protection and control who has access to the cloud you use.
* Flexible: One thing that many businesses love about Amazon EMR is how flexible it is. You can install more applications, customize the cluster and do so much more with this feature.

### 1.2.5. The Amazon EMR File System
* Allow you to leverage Amazon S3 as a file system
* Streams data directly from Amazon S3
* Uses HDFS for intermediates
* Better read | write performances and error handling than open source components
* Consistent view - Consistency for read after write
* Support for encryption
* Fast listing of objects

### 1.2.6. HDFS vs EMRFS
HDFS and the EMR File System (EMRFS), which uses Amazon S3, are both compatible with Amazon EMR, but they're not interchangeable. HDFS is an implementation of the Hadoop FileSystem API, which models POSIX file system behavior. EMRFS is an object store, not a file system.

### 1.2.7. Pricing
The hourly rate depends on the instance type used. Hourly prices range from $0.011/hour to $0.27/hour and are charged in addition to the EC2 costs.
