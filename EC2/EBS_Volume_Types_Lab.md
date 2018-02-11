# Upgrading EBS Volume Types Lab

Must have the EC2 instance and the EBS volumes in the same Availability Zones.

In console in sidebar under **Elastic Block Store** under **Volumes**

exam question Moving an Volume from one availibility zone to another: 
* create a snapshot
* create an image of the snapshot


## EXAM TIPS: Volumes & Snapshots
* Volumes exist on EBS:
    * Virtual Hard Disk
* Snapshots exist on S3
* Snapshots are point in time copies of Volumes
* Snapshots are incremental - this means that only the blocks that have changed since your last snapshot are moved to S3.
* If this is the first snapshot it will take a relatively long time to create.
* To create a snapshot for Amazon EBS volumes that serve as root devices, you should stop the instance before taking the snapshot.
* You **CAN** take a snap while the instance is running.
* You can create AMI's from both Volumes and Snapshots.
* You can change EBS volume sizes ont he fly, including changing the size and storage type.
* Volumes will **ALWAYS** be in the same availbility zone as the EC2 instance.
* To move an EC@ volume from one AZ/Region to anotehr, take a snap or an image of it, then copy it to the new AZ/Region.
* Snapshots of encrypted volumes are encrypted automatically.
* Volumes restored from encrypted snapshots are encrypted automatically.
* You can share snapshots, but only if they are unencrypted.
    * These snapshots can be shared with other AWS accounts or made public.
