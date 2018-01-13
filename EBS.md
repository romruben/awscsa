# AWS ASSOCIATED NOTES

## EBS

- Amazon EBS allows you to create storage volumes and attach them to Amazon EC2 instances. 

### Main Features

- Amazon EBS volumes are placed in a especific Availability Zone where they are automatically replicated to protect you from the failure of a single component.


### Main Concepts

#### EBS Volume Types

- SSD, General Purpose - GP2 (Up to 10k IOPS).
- SSD, Provisioned IOPS - IO1 (+ than 10k IOPS).
- HDD, Throughput Optimized - ST1 - frequently accessed workloads.
- HDD, Cold - SC1 - less frequently accessed data.
- HDD, Magnetic - Standard - cheap, infrequently accessed storage.

### Exam notes

- You cannot mount 1 EBS volume to multiple EC2 instances, instead use EFS.