# AMI Types - EBS vs Instance Store

#### AMI: Amazon Machine Image
#### You can select your AMI based on:
* Region (See Regions and Availability Zones)
* Operating System
* Architecture (32-bit or 64-bit)
* Launch Permissions
* Storage for the Root Device (Root Device Volume)
    * Instance Store (Also known as EPHEMERAL STORAGE)
    * EBS Backed Volumes

### Notes and Exam Tips:
* With an instance store, you can only reboot or terminate the instance you can not stop the instance. 
 This is primary difference between EBS and Instance Store, you can stop EBS but not an Instance Store.
* All AMIs are categorized as either backed by **Amazon EBS** or backed by **instance store**
* **For EBS Volumes:** The root devie for an instance launched from the AMI is an Amazon EBS volume created from an Amazon EBS snapshot.
* **FOR Instance Store Volumes:** The root device for an instance launched from the AMI is an instance store volume created from a template stored in Amazon S3.
    * Because the root is an instance store volume stored on Amazon S3, instance store volumes may take longer to provision than an EBS volume or an instance backed by EBS.
* Instance Store Volumes are sometimes called Ephemeral Storage.
* Instance store volumes cannot be stopped. If the underlying host fails, you will lose your data.
* EBS backed instances can be stopped. You will **not** lose the data on this instance if it is stopped.
* You can reboot both, you will not lose your data.
* By default, both **ROOT** volumes will be deleted on termination, however with EBS volumes, you cna tell AWS to keep the root device volume.
