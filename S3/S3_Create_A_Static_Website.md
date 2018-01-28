# Create a static website with S3 Lab

### Notes
When creating a bucket, and using S3 with Route53 (so you can own your own domain name), the bucket name must be the same as your Top Level domain name.

**Example:** 
    
    bucketName: example
    domainName from Route53: www.example.com
    
Once a bucket is created, you can view the buckets properties by clicking on the bucket link.
There will be a 'card' that is title **Static Website Hosting**. If you click that card you will see an endpoint with a particular Endpoint.
 
You will see an Endpoint that has a specific format.
 
**Example:**
 
    Endpoint: http://examplebucketname.s3-website-us-east-1.amazonaws.com
    
