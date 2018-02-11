# Encrypted Root Device Volumes & Snapshots (Lab)

#### What is an AMI 
##### Amazon Machine Image

#### Snapshots of Root Device Volumes
* To create a snapshot of Amazon EBS volumes that serve as root devices, you should stop the instance before taking the snapshot.

#### Volumes versus Snapshots - Security
* Snapshots of encrypted volumes are encrypted automatically
* Volumes restored from encrypted snapshots are encrypted automatically
* You can share snapshots, but only if they are **unencrypted**.
    * These snapshots can be shared with other AWS accounts made public.
    