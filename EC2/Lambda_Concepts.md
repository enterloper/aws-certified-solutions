# Lambda

### What is Lambda?
AWS Lambda is a compute service where you can upload your code and create a Lambda function. 
AWS Lambda takes care of provisioning and managing the servers that you use to run the code.
You don't have to worry about operating systems, patching, scaling, etc. 
You can use Lambda in the following ways:

- As an event-driven compute service where AWS Lambda runs your code in response to events.
These events could be changes to data in an Amazon S3 bucket or an Amazon DynamoDB table.
- As a compute service to run your code in response to HTTP requests using Amazon API Gateway or API calls made using AWS SDKs.

### What languages are supported?
- Node.js
- Java
- Python
- C# 

### How is Lambda Priced?
- Number of requests
    - First 1 million requests are free. $0.20 per 1 million requests thereafter.
- Duration
    - Duration is calculated from the time you code begins executing until it returns or otherwise terminates, rounded up to the nearest 100ms.
    The price depends on the amount of memory you allocate to your function. 
    You are charged $0.00001667 for every GB per second used.
    - The duration does have a maximum threshold of **five minutes**. 
   
### Why is Lambda cool?
- NO SERVERS
    - No maintainance needed
    - No devops needed
- Continuous Scaling
    - scales instantly
- Super super super cheap

### Exam Tips
- Lambda scales out (not up) automatically
- Lambda functions are independent, 1 event = 1 function
- Lambda is serverless
- Know what services are serverless
    - S3, APIGateway, DynamoDB, 
    -EC2 is **NOT** serverless because you're managing EC2 instances.
- Lambda functions can trigger other lambda function, 1 event can = x functions if functions trigger other functions.
    - This is one way to manage the duration threshold of five minutes previously mentioned.
- Architectures can get extremely complicated, **AWS X-ray** allows you to debug what is happening
- Lambda can do things globally, so you can use it to back up S3 buckets to other S3 buckets, etc.
- Know your triggers
