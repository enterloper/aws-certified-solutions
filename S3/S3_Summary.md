# S3 Summary 

S3 is Object based which allows you to upload **files**

Files can be from 0 bytes to 5 TB.

There is unlimited storage.

Files are stored in Buckets known as directories

S3 is a universal namespace, that is, names must be unique globally.

Format of an S3 Bucket Name: https://s3-eu-west-1.amazonaws.com/example

Any time you put a new object up to S3, it's immediately available for review once it's uploaded.
However, if you are modifying an existing Object, it may take time for AWS to apply the changes.
* Read after Write consistency for PUTS of new Objects.
* Eventual Consistency for overwrite PUTS and DELETES (can take some time to propagate)

#### S3 Storage Classes/Tiers
* S3 (durable, immediately available, frequently accessed)
* S3 - IA (durable, immediately available, infrequently accessed)
* S3 - Reduced Redundancy Storage (data that is easily reproducible, such as thumb nails etc)
* Glacier - Archived data, where you can wait 3 - 5 hours before accessing.


#### Remember the core fundamentals of S3:
* Key (name)
* Value (data)
* Version ID
* Metadata
* Access Control Lists
* Object based storage **only** (for files).
* **Not suitable to install an operating system on.**

#### S3-Versioning
* Stores all versions of an object (including all writes, even if you delete an object)
* Great backup tool
* Once enabled, versioning cannot be disabled, only suspended.
* Integrates with Lifecycle rules
* Versioning's MFA Delete capability, which uses multi-factor authentication, can be used to provide an additional layer of security.
* Cross Region Replication, requires versioning enabled on the source bucket.

#### S3
* Can be used in conjunction with versioning.
* Can be applied to current versions and previous versions
* Following actions can now be done:
    * Transition to the Standard - Infrequent Access Storage Class (128KB and 30 days after the creation date).
    * Archive to the Glacier Storage Class (30 days after IA, if relevant)
    * Permanently Delete
    
#### CloudFront 
* Edge Location - This is the location where content will be cached. This is separate to an AWS Region/AZ
* Origin - This is the origin of all the files that CDN will distribute. This can be either an S3 Bucket, an EC2 Instance, an Elastic Load Balancer or Route53.
* Distribution - This is the name given the CDN which consists of a collection of Edge Locations.
    * Web Distribution - Typically used for Websites.
    * RTMP - Used for Media Streaming.
* Edge Locations are not just READ only, you can write to them as well (put an object on to them).
* Objects are cached for the life of the TTL (Time to Live)

#### Securing your buckets
* By default, all newly created buckets are **PRIVATE**
* You can setup access control to your buckets using:
    * Bucket Policies
    * Access Control Lists
* S3 buckets can be configured to create access logs which log all requests made to the S3 bucket. This can be done to another bucket.

#### Encryption
* In Transit
    * SSL/TLS
* At Rest
    * Server Side Encryption
        * S3 Managed Keys - **SSE-S3** 
            * Each object is encrypted with a unique key employing strong multi-factor encryption.
              As an additional safeguard it encrypts the key itself with a master key that it regularly rotates. 
              This is AES-256 (Advanced Encryption Standard) which Amazon handles entirely.
        * AWS Key Management Service, Managed Keys - **SSE-KMS**
            * Very similar to **SSE-S3** but has additional benefits such as cost.
            * Allows for separate permissions for the use of an envelope. An envelope is essentially a key that protects your data's encryption key which provides additional protections against unauthorized access. 
            * Provides an audit trail which provides info on who used your encryption key and when
        * Server Side Encryption with Customer Provided Keys - **SSE-C**
            * Encryption Keys are managed by the users and Amazon S3 manages the actual encryption as it writes to the disk and decryption as users read the objects.
    * Client Side Encryption

#### Storage Gateway
* File Gateway - For flat files, stored directly on S3
* Volume Gateway 
    * Stored Volumes - Entire Dataset is stored on site and is asynchronously backed up to S3.
      (block-based storage for virtual machines, virtual hard disks, operating systems and databases)
    * Cached Volumes - Entire Dataset is stored on S3 and the most frequently accessed data is cached on site.
* Gateway Virtual Tape Library (VTL)
    * Used for backup and uses popular backup applications like NetBackup, Backup Exec, Veeam et cetera.
    * Make a virtual backup of servers and you store those virtual tapes off into S3 and use lifecycle management rules to archive them Glacier.

#### Snowball
##### Types:
* Snowball
    * Can import to S3
    * Export from S3 to a Snowball
* Snowball Edge
* Snowmobile
* Understand what Snowball is, as well as it's older version Import/Export

#### S3 Transfer Acceleration
You can speed up transfers to S3 using S3 Transfer Acceleration. 
This costs extra, and has the greatest impact on people who are in far away locations.

#### S3 Static Websites
* You can use S3 to host static websites
* Serverless
* Very cheap, scales automatically
* **STATIC** only, cannot host dynamic sites.

#### LAST FEW EXAM TIPS
* Write to S3 - HTTP 200 code for a successful write.
* You can load files to S3 much faster by enabling multipart upload.
* Read the S3 FAQ before taking the exam. **It comes up a lot!**