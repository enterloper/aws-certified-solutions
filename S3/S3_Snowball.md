# Snowball

###Import/Export Disk 
#####(the *old* way of offline data transfer)
Aws Import/Export Disk accelerates moving large amounts of data into and out of the AWS cloud using portable storage devices for transport.
AWS Import/Export Disk transfers your data directly onto and off of storage devices using Amazon's high-speed internal network and bypassing the Internet.
##### Types of Snowballs:
* Snowball
* Snowball Edge
* Snowmobile

### What is Snowball?

Essentially, it's a way to transfer data without using the internet. It's a **GIANT** flashdrive.
Snowball is a petabyte-scale data transport solution that uses secure appliances to transfer large amounts of data into and out of AWS. Using Snowball addresses common challenges with large-scale data transfers including high network costs, long transfer times, and security concerns. Transferring data with Snowball is simple, fast, secure, and can be as little as one-fifth the cost of high-speed internet.

80TB snowball in all regions. 
Snowball uses multiple layers of security designed to protect your data including tamper-resistant enclosures, 256-bit encryption, and an industry-standard Trusted Platform Module (TPM) designed to ensure both security and full chain-of-custody of your data. 
Once the data transfer job has been processed and verified, AWS performs a software erasure of the Snowball appliance.

### What is Snowball Edge?

AWS Snowball Edge is a 100TB data transfer device with on-board storage and compute capabilities.
You can use Snowball Edge to move large amounts of data into and out of AWS, as a temporary storage tier for large local datasets,
or to support local workloads in remote or offline locations.

Snowball Edge connect to your existing applications and infrastructure using standard storage interfaces, which allows you to streamline the data transfer process and minimizing setup and intergration.
Snowball Edge can cluster together to form a local storage tier and process your data on-premises, helping ensure your applications continue to run even when they are not able to access the cloud.

### What is Snowmobile?

AWS Snowmobile is an Exabyte-scale data transfer service used to move extremely large amounts of data to AWS.
You can transfer up to 100PB per Snowmobile, a 45-foot long ruggedized shipping container, pulled by a semi-trailer truck.
Snowmobile makes it easy to move massive volumes of data to the cloud, including video libraries, image repositories, or even a complete data center migration.
Transferring data with Snowmobile is secure, fast and cost effective.

###Exam Tips:
* Understand what Snowball is
* Understand what Import Export is
* Snowball Can
    * Import to S3
    * Export from S3