## RAID, Volumes & Snapshots
### What is RAID?
Redundant Array of Independent Disks. 
Input/Output performance on a single volume can be improved by using **RAID 0** to stripe multiple volumes together for on-instance redundancy.   
**RAID 1** can mirror two volumes together.

**RAID 0** - Mostly used in gaming pcs, **Striped**, No Redundancy, Good Performance
Use: When I/O is more important than fault tolerance; ie a heavily used database where data replication is already set up separately.
Pros:
    * I/O is distributed across the volumes in a stripe. 
    * If you add a volume, you get the straight addition of throughput.
    * Good performance
Cons:
    * Performance of the stripe is limited to the worst performing volume in the set.
    * Loss of a single volume results in a complete data loss for the array.
    * No redundancy
    
**RAID 1** - One disk mirrors another
Use: When fault tolerance is more important than I/O performance; ie a critical application.
Pros: 
    * All about redundancy.
    * Safer from the standpoint of data durability
Cons: 
    * Does not provide a write performance improvement; requires more Amazon EC2 to Amazon EBS bandwidth than non-RAID configurations because the data is written to multiple volumes simultaneously.

**RAID 5**
Pros: 
    * Good for reads
Cons: 
    * Bad for writes
    * AWS does not recommend ever putting RAID 5's on EBS due to the parity write operations of these RAID modes consume some of the IOPS available to your volumes.
    
**RAID 10** Striped & Mirrored, Good Redundancy, Good Performance

Taking a Snapshot of a RAID array:
* Stop the application from writing to disk
* Flush all caches to the disk

* How can we do the above?
    * Freeze the file system
    * Unmount the RAID Array
    * Shutting down the associated EC2 Instance
    