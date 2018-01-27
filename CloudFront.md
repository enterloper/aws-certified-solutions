# CloudFront

### What is a CDN?
A Content Delivery Network (CDN) is a system  of distributed servers (network) that deliver webpages and other web content to a user based on the geographic locations of the user, the origin of the webpage and a content delivery server.

### CDN Key Terminology
* Edge Location - This si the location where content will be cached. This is separate to an AWS Region/AZ
* Origin - This is the origin of all the files that the CDN will distribute. This can be either an S3 Bucket, an EC2 Instance, an Elastic Load Balancer or Route53
* Distribution - This is the name given to the CDN which consists of a collection of Edge Locations.

### What is CloudFront
Amazon CloudFront can be used to deliver yoru entire website, including dynamic, static, streaming, and interactive content using a global network of edge locations.
Requests for your content are automatically routed to the nearest edge location, so content is delivered with the best possible performance.

Amazon CloudFront is optimized to work with other Amazon Web Services, like Simple Storage Service (S3), Elastic Compute Cloud (EC2), Elastic Load Balancing, and Route 53. 
CloudFront also works seamlessly with any non-AWS origin server, which stores the original, definite versions of your files.

### CDN Key Terminology
* Web Distribution - Typically used for Websites
* RTMP - Used for Media Streaming

### Exam Tips
* Edge Location - This is the location where content will be cached. This is separate to an AWS Region/AZ
* Orgin - this is the origin of all the files that the CDN will distribute. This can be either an S3 Bucket, an EC2 Instance, an Elastic Load Balancer or Route53
* Distribution - This is the name given the CDN which consists of a collection of Edge Locations.
    * Web Distribution - Typically used for Websites.
    * RTMP - used for Media Streaming.
* Edge location are not just READ only, you can write to them too (ie put an object on to them)
* Objects are cached for the life of the Time to Live (TTL).
* You can clear cached objects, but you will be charged.
