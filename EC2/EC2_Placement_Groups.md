# EC2 Placement Groups
### What is a Placement Group?
A Placement Group is a logical grouping of instances within a single Availability Zone.
Using Placement Groups enables applications to participate in a low-latency, 10 Gbps network.
Placement groups are recommended for applications that benefit from low network latency, high network throughput, or both.

### Things to consider about Placement Groups:
* A Placement Group can't span multiple Availability Zones.
* The name you specify for a placement group must be unique with your AWS account.
* Only certain types of instances can be launched in a placement group (Compute Optimized, GPU, Memory Optimized, Storage Optimized)
* AWS recommend homogenous (same size, same family) instances within Placement Groups.
* You can't merge Placement Groups.
* You can't move an existing instance into a Placement Group. 
You can create an AMI from your existing instance, and then launch a new instance from the AMI into a Placement Group.