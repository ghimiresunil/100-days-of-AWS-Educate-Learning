## 1. What are AWS Analytics Services?
It is a service offered by Amazon that helps in processing and providing insights to data by analysing it. Amazon Elastic Search is one of the service in the analytics section

### 1.1. Amazon Elastic Search
Amazon ElasticSearch Service is a managed service that makes it easy to deploy, operate, and scale ElasticSearch in the AWS Cloud. It is the popular open source search and analytics engine(service).

It is:
* Easily configurable with clean set of UI options
* Monitoring is really good, which it rich set of parameters, which can be used to configure autoscaling (not directly with AWS, but custom at-least)
* Scaling takes a bit of time, depending on the size of the cluster, so, it is always better over-size and then reduce as per needs
* The amount of data you can query, depends on the size of instance, but I remember the size of http request payload to be restrictive at 100 MB, for even the biggest of instances. This will restrict how much data you can push into ES. Hence, it’s always good practice to be very choosy on items to be indexed.
* Backups are automated, although, we have no direct control over the backup data. We’d have to contact AWS support for any restoration. It would have been great, if we are given more control, like they do with RDS snapshots
* The main thing I found, to be problematic for many is the authentication, which either using IAM user based or Public IP based. AWS ES does not support x-pack, so there is no way to use it for monitoring, authentication, granular access (read only access for kibana dashboards etc.) However, there does seem to be a way to use AWS Cognito as a basic authentication mechanism but with no granular access control

#### 1.1.1. Leading use cases for Elastic Search
* Time Series Analytics and Log application
* Real-time application Monitoring
* Operational Intelligence
* Click stream analytics

#### 1.1.2. Amazon Elasticsearch Version\
Currently, this Amazon Elasticsearch Service supports Elasticsearch versions 5.5, 5.3, 5.1, 2.3, and 1.5.

#### 1.1.3. AWS ElasticSearch Architecture
You will get the idea of several services going to be provided by AWS Elasticsearch by just seeing the architecture of AWS Elasticsearch. Amazon Elasticsearch domain is surely deployed by the AWS CloudFormation template. This can be either hardware, software, or data exposed to Amazon Elasticsearch Service endpoints.
![aws-elasticsearch](https://user-images.githubusercontent.com/40186859/176345002-dd0c1565-1b66-4da0-9037-a4aa51dddd71.png)<br>
In this AWS Elasticsearch architecture, you see the Elastic Load balancing whose main objective is to distribute the traffic to proxy servers and enable the automatic recovery to maintain the instance availability. Elastic Load Balancing uses highly available designs here to achieve this objective. The above template easily launches three Amazon EC2 instances. These are separately Availability zones of Amazon VPC Network. Here, VPC means Virtual Private Cloud.


#### 1.1.4. Advantages of AWS Elasticsearch
* Used Easily
* Supports Open Source APIs and Tools
* Secure
* Highly Available
* Tightly Integrated with Other AWS Service
* Easily Scalable

#### 1.1.5. Limitation of AWS ElasticSearch
* It allows the users to launch their domain within a VPC or use a public endpoint. Although both actions are not allowed to be performed together in it.
* AWS Elasticsearch provides free tier only for 12 months; means it is not free. After 12 months of signup, you have to pay for using it.

#### 1.1.6. Pricing of AWS ElasticSearch
With the help of the AWS ElasticSearch Service, one can easily pay for the exact usage only. There are no certain commitments or no minimum fees or upfront commitments. The charge or else pricing will be as per the Amazon ElasticSearch Instance hours, Standard data transfer fees, and Amazon EBS storage.

One can easily get started with the free tier which probably delivers free usage of up to 750 hours per month with a single AZ t2.micro.elasticsearch or else t2.small.elasticsearch instance. It's AWS ElasticSearch pricing will also be for 10GB per month of optional Amazon EBS storage with the magnetic and general purpose.

#### 1.1.1.7. Getting started with AWS Elasticsearch services
* Signup for AWS account
  *  Signup with AWS to create a new account on it. Click here and hit on Create an AWS Account button at the top right corner
* Create an Amazon ES domain
  * Provide all required information here that is needed and click on the Continue button.
  * Next, provide the contact information and check the box by agreeing with terms and conditions and then click on Create Account and Continue button.
  * In this step, you have to save your debit/credit card information such as card number, expiration date, billing address, etc. for Payment Information. 
  <br> **Following are the detailed steps to create an Amazon ES domain.**
  * Define your domain
    * Login to your AWS account with your credentials.
    * To navigate on the Elasticsearch Service page, go to the Analytics section where click on Elasticsearch Service.
    * Click on Create a new domain button and then choose Development and testing.
    * Here, you need to select the Elasticsearch version and your preferred Deployment type. Elasticsearch 7.4.0 is the latest version, and we are also this version.
  * Configure your domain
    * Enter the domain name (e.g., aws_learning_books) which you are going to create and choose the Instance type from the drop-down list.
    * Use default value for Data nodes storage and 1 in number of instance
    * We choose small.elasticsearch in instance type, which is a free tier.
    * Just ignore the other fields and click on Next to move on Set up access page.
  * Set up access policy
    * To access this domain, we have to set up appropriate permission for it. Therefore, you have to set up access on this page.
    * For simplicity, we recommend you to select the public access domain. Although, you can restrict access to a VPC or an IAM role. A specific set of users can access your Elasticsearch cluster.
    * Leave the Amazon Cognito Authentication setting for now.
    * Under the Access policy, select a template for Set the domain access policy Choose Allow open access to the domain policy for this.
    * Ignore the encryption setting and leave it as default and click Next.
  * Review
    * Double-check your configuration and choose Confirm
    * A new domain (cluster) will take around 10-15 minutes to create and initialize. However, it can also take more time to initialize depending on the configuration.<br>
  Note: you get a message that "**_You have successfully created an Elasticsearch domain_**".  You will see the domain status set to **Active** and cluster health to **green**.    
* Upload data to Amazon ES domain for indexing
  * Using the command-line interface or programming language, we can upload the data to Amazon ES Service domain.
  * On Windows operating system, you can install curl to use it from the command prompt. However, we recommend you to use a tool like Cygwin. MacOS and Linux operating systems already come with pre-installed curl. So, you don't need to install curl on it. 
* Search document in an Amazon domain
  * On the browser, navigate to Kibana plugin for your Amazon ES domain. On the Amazon ES console, you will get the Kibana endpoint on your domain dashboard. The URL format will be like <br>
  ``` domain-endpoint/_plugin/kibana/ ``` 
  * Log in to the console using your master user name and password.
  * Here, it is must to configure atleast one index pattern to use the Kibana because these patterns are used by Kibana to identify which indices you want to analyze. As we have created aws_learning_books domain so, enter books for this tutorial and then choose Create.
  * Now, you will see various document field such as book_name, author, publisher, etc. shown by the Index Pattern For now, choose Discover to search your data.
  * Enter Mars in the search bar and press Enter. Note that when you search for phrase mars attacks, how the similarity score (_score) increases.
* Delete an Amazon ES domain <br>
  * Sign in to the Amazon Elasticsearch Service console using user name and password.
  * In the navigation page, select books domain under My domains
  * Now, select Action, and then Delete domain inside it.
  * At last, check the Delete Domain checkbox and choose Delete. <br>
**Note**: First of all, to getting started with AWS, we are required to create an account on AWS services.
 
#### 1.1.1.8. Things to remember:
* Amazon ElasticSearch service is a drop-in replacement for new and existing ElasticSearch workloads.
* Deploy, Manage, and Scale ElasticSearch more easily in the AWS cloud.
* Support for ElasticSearch 5.1 brings scripting, additional plugins and additional performance to Amazon ElasticSearch Service

#### 1.1.1.9. Search
* Application or website provides search capabilities over diverse documents
* Query API to support application search
