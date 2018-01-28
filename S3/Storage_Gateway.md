# Storage Gateway 
AWS Storage Gateway is a service that connects an on-premises software application with cloud-based storage to provide seamless and secure integration between an organization/s on-premise IT environment and AWS's storage infratstructure.
The service enables you to securely store data to the AWS cloud for scalable and cost-effective storage.

AWS Storage Gateway's software appliance is available for download as a virtual machine (VM) image that you install on a host in your **on-site** data center.
Storage Gateway supports either VMware ESXi or Microsoft Hyper-V. Once you've installed your gateway and associated it with your AWS account through the activation process, you can use the AWS Management Console to create the storage gateway option that is right for you.

### Four Types of Storage Gateways
* File Gateway (NFS) - where you store flat files in S3 (word files, PDFs, pictures...)
* Volume Gateway (iSCSI) - where you store Operating Systems, or a VM, or a Virtual Disk using **block-based storage**.
 This is done in two types.
    * Stored Volumes - where you have an entire copy of the data set on site (on premise)
    * Cached Volumes - where you store most recently accessed data on premise and the rest of the data is held on Amazon.
* Tape Gateway (VTL) - a backup/archiving solution, allows you to create virtual tapes and send them to S3 and then eventually Glacier.

### File Gateway
Files are stored as objects in your S3 buckets, accessed through a Network File System (NFS) mount point.
Ownership, permissions, and timestamps are durably stored in S3 in the user-metadata of the object associated with the file.
Once objects are transferred to S3, they can be managed as native S3 objects and bucket policies such as versioning, lifecycle management, and cross-region replication apply directly to objects stored in your bucket.

### Volume Gateway
The volume interface presents your applications with disk volumes using the iSCSI block protocol. 
Since it's block-based, that means you can store Operating Systems on it, SQL-Server, Databases etc. It's basically a **virtual hard disk**
Data written to these volumes (hard disks) can be asynchronously backed up as point-in-time snapshots of your volumes, and stored in teh cloud as Amazon EBS snapshots.
Snapshots are incremental backups that capture only changed blocks. All snapshot storage is also compressed to minimize your storage charges.
Imagine Volume Gateways as "Virtual Hard Disks" that sit on premises and are backed up to Amazon.

### Stored Volumes
Stored Volumes let you store your primary data locally, while asynchronously backing up that data to AWS.
Stored volumes provide your on-premises applications with low-latency access to their entire data sets, while providing durable, off-site backups.
You can create storage volumes and mount them as iSCSI devices from your on-premises application servers. 
Data written to your stored volumes is stored on your on-premises storage hardware. 
This data is asynchronously backed up to Amazon Simple Storage Service (S3) in the form of Amazon Elastic Block Store (Amazon EBS)
snapshots. 1GB - 16 TB in size for Stored Volumes.

### Cached Volumes
Cached volumes let you use Amazon Simple Storage Service (S3) as your primary data storage while retaining frequently accessed data locally in your storage gateway.
Cached volumes minimize the need to scale your on-premises storage infrastructure, while still providing your applications with low-latency access to their frequently accessed data.
You can create storage volumes up to 32 TiB (tebibyte - 1024^4 bytes) in size and attach to them as iSCSI devices from your on-premises application servers.
Your gateway stores data that you write to these volumes in Amazon S3 and retains recently read data in your on-premises storage gateway's cache and upload buffer storage.
1Gb - 32TB in size for Cached Volumes.

You're not keeping full copy on premises, only retains recently read data on premises

### Tape Gateway
Tape Gateway offers a durable, cost-effective solution to archive your data in the AWS Cloud. 
The VTL interface it provides lets you leverage your existing tape-based backup application infrastructure to store data on virtual tape cartridges that you create on your tape gateway.
Each tape Gateway is pre-configured with a media changer and tape drives, which are available to your existing client backup applications as iSCSI devices.
You add tape cartridges as you need to archive your data. Supported by NetBackup, Backup Exec, Veeam etc.

### Exam Tips
* File gateway - For flat files only, stored directly on S3. **NO** files are stored on premises.
* Volume Gateway - block-based storage using the iSCSI protocol. Two routes to choose from depending on need:
    * Stored Volumes - Entire data set is stored on premises and is asynchronously backed up to S3.
    * Cached Volumes - Entire data set is stored on S3 and **only the most frequently accessed data is cached on premises**.
* Gateway Virtual Tape Library (VTL) - Used for backup and uses popular backup applications like NetBackup, Backup Exec, Veeam, et cetera.
