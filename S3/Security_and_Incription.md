# Security and Encryption

### Securing your buckets
* By default, all newly created buckets are **PRIVATE**
* You can setup access control to your buckets using: 
    * Bucket Policies
    * Access Control Lists
* S3 buckets can be configured to create access logs which log all requests made to the S3 bucket. THis can be done to another bucket.

### Encryption
* In Transit; when you're sending information to and from the bucket.
* SSL/TLS using HTTPS
* At Rest, four different methods for encryption at rest.
* Server Side Encryption

#### Server Side Encryption
* S3 Managed Keys - **SSE-S3**: encrypted with a unique key employing strong Multi-factor encryption, master keys are rotated automatically by Amazon.
* AWS Key Management Service, Managed Keys - **SSE-KMS**: KMS stands for Key Management Service. Similar to SSE-S3. Main advantage is the use of an envelope key. Also provides an audit trail to see who is decrypting what and when.
* Server Side Encryption With Customer Provided Keys - **SSE-C**: Management of keys is performed by the developers.

#### Client Side Encryption