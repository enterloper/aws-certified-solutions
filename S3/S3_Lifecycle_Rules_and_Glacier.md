# S3 Lifecycle Rules and Glacier

### Lifecycle rules
Lifecycle rules will help you manage your storage costs by controlling the lifecycle of your objects. 
Create Lifecycle rules to automatically transition your objects to the Standard - Infrequent Access Storage Class, archive them to the Glacier Storage Class, and remove them after a specified time period. 
You can use Lifecycle rules to manage all versions of your objects. 
This includes both the Current and Previous versions.

### When shoud Lifecycle Configuration for Objects be used?
* If you are uploading periodic logs to your bucket, your application might need these logs for a week or a month after creation, and after that you might want to delete them.
  
* Some documents are frequently accessed for a limited period of time. After that, these documents are less frequently accessed. 
Over time, you might not need real-time access to these objects, but your organization or regulations might require you to archive them for a longer period and then optionally delete them later.
  
* You might also upload some types of data to Amazon S3 primarily for archival purposes, for example digital media archives, financial and healthcare records, raw genomics sequence data, long-term database backups, and data that must be retained for regulatory compliance.

### Exam Tips

* Can be used in conjunction with versioning.
* Can be applied to current versions and previous versions
* Following actions can now be done:
    * Transition to the Standard - Infrequent Access Storage Class (128Kb and 30 days after the creation date).
    * Archive to the Glacier Storage Class (30 days after Infrequent Access, if relevant).
    * Permanently Delete
* Glacier does **NOT** exist in Singapore and South America.
