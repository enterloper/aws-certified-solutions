# S3 Cross Region Replication
### Exam Tips
* Versioning must be enabled on both the source and destination buckets.
* Regions must be unique
* Files in an existing bucket are not replicated automatically. All subsequent updated files will be replicated automatically.
    * Best practice for Cross Region Replication, create a source bucket, as well as a destination bucket, and make sure you've configured cross region replication to be turned on.
* You cannot replicate to multiple buckets or use daisy chaining (at this time).
* Delete markers are replicated.
* Deleting individual versions or delete markers will not be replicated.
* Understand what Cross Region Replication is at a high level.
