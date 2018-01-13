# AWS ASSOCIATED NOTES

## EC2


- Amazon Elastic Compute Cloud (Amazon EC2) is a web service that provides resizable compute capacity in the cloud.


### Main Features



### Main Concepts

#### EC2 Options

- **_On Demand_**: allow you to pay a fixed rate by the hour (or by second) with no commitment.
	- Users that want the low cost and flexibility of EC2 without any up-front payment or long-term commitment.
	- Applications with short term, spiky, or unpredictable workloads that cannot be interrupted.
	- Applications being developed or tested on EC2 for first time.
- **_Reserved_**: provide you with a capacity reservation and offer a significant discount on the hourly change for an instance. 1 Year or 3 year terms.
	- Applications with steady state or predictable usage.
	- Applications that require reserved capacity.
	- Users able to make upfront payments to reduce their total computing costs even further.
		- Standard RI's (Up to 75% off on demand).
		-  Convertible RI's (Up to 54% off on demand) capability to change the attributes of the RI as long as the exchange results in the creation of Reserved Instances of equal or greater value.
		-  Scheduled RI's available to launch within the time windows you reserve. This option allows you to match your capacity reservation to a predictable recurring schedule that only requires a fraction of a day, a week or a month.

- **_Spot_**: enable you to bid whatever price you want for instance capacity, providing for even greater savings if your applications have flexible start and end times.
	- Applications that have flexible start and end times.
	- Applications that are only feasible at very low compute prices.
	- Users with urgent computing needs for large amounts of additional capacity.

- **_Dedicated Hosts_**: Physical EC2 server dedicated for your use. Dedicated Hosts can help you reduce costs by allowing you to use your existing server-bound software licenses.
	- 	Useful for regulatory requirements that may not support multitenant virtualization.
	-  Great for licensing which does not support multi-tenancy or cloud deployments.
	-  Can be purchased On-demand (hourly).
	-  Can be purchased as a Reservation for up to 70% off the On-Demand price.


#### EC2 Instance Types

![Instance Types](./images/ec2/instance_types.png

How to remember them (DR MC GIFT PX):

- **D** for Density.
- **R** for RAM.
- **M** main choice for general purpose apps.
- **C** for Compute.
- **G** for graphics.
- **I** for IOPS.
- **F** for FPGA.
- **T** cheap general purpose (think T2 Micro).
- **P** graphics (think PICS).
- **X** Extreme memory.


### Exam notes

- Know diffferences between: On demand, spot, reserved, dedicated hosts.
- With spot instances, if you terminate the instance, you pay for the hour.
- If AWS terminates the spot instance, you get the hour it was terminated in for free.
- Termination Protection in EC2 instances is turned off by default.
- On an EBS-backed instance, the default action is for the root EBS volume to be detected when the instance is terminated.
- EBS Root Volumes of your DEFAULT AMI's cannot be encrypted. You can also use a third party tool (such as bit locker etc) to encrypt the root volume, or this can be done when creating AMI's in the AWS console or using the API.
- Additional volumes can be encrypted.
- 1 instance can have multiple security groups.
- Any rule you make to a security group applies immediately.

- Security Groups:
	- All Inbound Traffic is blocked by default.
	- All Outbound Traffic is allowed by default.
	- Changes to Security Groups take effect immediately.
	- You can have any number of EC2 instances within a security group.
	- You can have multiple security groups attached to EC2 Instances.
	- Security Groups are STATEFUL. (If you create an inbound rule allowing traffic in, that traffic is automatically allowed back out again.
	- You cannotblock specific IP addresses using Security Groups, instead use Network Access Control Lists.
	- You can specify allow rules, but not deny rules.

- In order to move EBS volumes from one availability zone to another, you need to create a snapshot.
- In order to move an instance from one region to another:
	1. Create a snapshot
	2. Copy the snapshot to new region.
	3. Create an image of that snapshot.
