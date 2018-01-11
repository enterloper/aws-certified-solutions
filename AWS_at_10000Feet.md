# The History of AWS
#### None of this will be on the exam.

"Invention requires two things: 
1. The ability to try a lot of experiments. 
2. Not having to live with the collateral damage of failed experiments.

## A Brief Time Line of AWS
* 2003 - Chris Pinkhan & Benjamin Black present a paper on what Amazon's own internal infrastructure should look like.
* The suggested selling it as a service and prepared a business case.
* 2004 - SQS officially launched 
* 2006 - AWS officially launched
* 2007 - Over 180,000 developers on the platform
* 2010 - All of Amazon.com moved to AWS
* 2012 - First re:Invent Conference
* 2013 - Certifications Launched
* 2014 - Committed to achieve 100% renewable energy usage for its global footprint
* 2015 - AWS breaks out its revenue: $6 billion per year and growing close to 90% year on year
* 2016 - Run rate of $13 billion
* 2017 - AWS re:Invent releases a host of Artificial Intelligent Services as well as Virtual Reality services.

# The 10,000 Foot Overview

## AWS Global Infrastructure
#### What is a Region? What is an Availabilty Zone?
* A Region is a geographical area. Each Region consists of 2 (or more) Availability Zones.
* An Availability Zone (AZ) is simply a Data Center. Always architect for failure by putting your resources in multiple AZs.
#### What is an Edge Location?
* Edge Locations are endpoints for AWS which are used for caching content. Typically this consists of CloudFront, Amazon's Content Delivery Network (CDN).
* There are more Edge Locations than Regions.

### EXAM TIPS
Understand the difference between a region, an Availability Zone (AZ) and an Edge Location.
* A Region is a physical location in the world which consists of two or more Availability Zones (AZs).
* An AZ is one or more discrete data centers, each with redundant power, networking and connectivity, housed in separate facilities.
* Edge Locations are endpoints for AWS which are used for caching content. Typically this consists of CloudFront, Amazon's Content Delivery Network (CDN).

### Compute  
* EC2 - Elastic Compute Cloud
* EC2 - Container Service
* Elastic Beanstalk - autoscaling groups, EC2 instances, etc.
* Lambda - provides control over when to execute a lambda function
* Lightsail - virtual private service, simply provisions a server
* Batch

### Storage
* S3 - buckets for storing files
* EFS - Elastic File System
* Glacier - data archival service - Cheap
* Snowball - 
* Storage Gateway - 

### Databases
* RDS - Relational Database Services - SQL/PostgreSQL
* DynamoDB - noSQL
* Elasticache - cache commonly queried things
* Red Shift - used primarily for data warehousing

### Migration
* AWS Migration Hub
* Application Discovery Service
* Database Migration Service
* Server Migration Service
* Snowball - used for moving very large data in the cloud

### Networking & Content Delivery
* VPC - Virtual Private cloud #### MUST KNOW THIS!
* CloudFront
* Route53
* API Gateway
* Direct Connect

### Developer Tools
* CodeStar - project managing a codebase
* CodeCommit - Stores code, essentially a source control
* CodeBuild - compiles code, runs test, and preps for deploy
* CodeDeploy - deployment service, automation
* CodePipeline - 
* X-Ray - used to debug and other things
* Cloud9 - develop code in the AWS console

### Management Tools
* CloudWatch
* CloudFormation - a way of scripting infrastructure, turns infrastructure into code
* CloudTrail - logs changes to the AWS environment
* Config - 
* OpsWorks - similar to Elastic Beanstalk but more robust, enables sys admins to configure and operate your web apps
* Service Catalog
* Systems Manager
* Trusted Advisor - provides advice with security, AWS services, and AWS environment
* Managed Services

### Media Services
* Elastic Transcoder - helps with media resizer for various platforms/machines
* Media Convert - files based media code converter allows you to broadcast at scale for multiscreen devices
* MediaLive - high quality video streams
* MediaPackage - prepares and protects videos
* MediaStore - low latency, good performance for storing media
* MediaTailor

### Machine Learning
* SageMaker - Deep Learning 
* Comprehend - Sentiment Analysis
* DeepLens - Artificially aware AWS camera
* Lex - powers amazon Alexa service
* Machine Learning - 
* Polly - takes text and turns it into speech
* Rekognition - upload a photo/video and it'll tell you what that picture/film is
* Amazon Translate - translates languages
* Amazon Transcribe - Automatic Speech Recognition

### Analytics
* Athena - 
* EMR - Elastic Map Reduce is used for processing large amounts of big data
* CloudSearch
* ElasticSearch Service
* Kinesis - ingests large amounts of data into AWS i.e. hashtags on twitter
* Kinesis Video Streams - 
* QuickSight
* Data Pipeline
* Glue - used for ETL (Extract, Transform, Load)

### Security & Identity & Compliance
* IAM - 
* Cognito - used for authentication
* GaurdDuty
* Inspector - generates reports on vulnerabilities
* Macie
* Certificate Manager
* CloudHSM - Hardware Security Modules
* Directory Service
* WAF - Web Application Firewall - i.e.stops SQL injections
* Shield - DDOS mitigation
* Artifact

### Mobile Services
* Mobile Hub
* Pinpoint - targeted push notifications
* AWS AppSync - updates data for web and mobile in real time
* Device Farm - test your app on real devices
* Mobile Analytics

### AR/VR
* Sumerian

### Application Integration
* Step Functions
* Amazon MQ
* SNS - notifications service
* SQS - decouple your infrastructure
* SWF - Simple Workflow

### Customer Engagement
* Connect - contact center as a service
* SES - Simple Email Service

### Business Productivity
* Alexa For Business
* Chime - video conferencing 
* Work Docs - safely and securely store documents
* WorkMail - use email through Amazon

### Desktop and App Streaming
* Workspaces - run the OS in the cloud and stream the environment to your device
* Appstream 2.0 - stream the actual application to your device

### Internet of Things
* iOT
* iOT Device Management
* Amazon FreeRTOS
* Greengrass

### GameDevelopment
* GameLift
