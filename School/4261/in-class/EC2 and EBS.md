Runtime access to EC2 configuration 
- Instance meta data is available at http://162.254.168.254/latest/meta-data/
	- Instance ID 
	- Instance type (t2micro)
	- AMI ID 
	- IP addresses 
- Instance user data is available at http://162.254.168.254/latest/user-data/
	- OS Initialization scripts 
	- Cloud initialization scripts 
	- Environment variables setup 
	- Container initialization 

IP addresses for EC2 
- Public IP 
	- Assigned when instance is active 
	- Stopping and restarting will result in a different public IP address 
- Private IP 
	- Assigned to all instances 
- Elastic IP 
	- Static IP address 

Elastic network interface 
- Virtual network card 
- Enhanced Network Adapter (ENA)
	- Faster connection 
- Elastic Fabric Adapter (EFA)
	- Highest connection 
	- OS bypass
	- High performance application such as ML 

Monitoring EC2
 - Cloudwatch monitors EC2 instance 
 - Create Cloudwatch alarm to take actions e.g. reboot EC2 instance 
 - Add CloudWatch agent to collect
	 - Additional system metric from EC2 
	- memory ussage 
- Logging and auditing (cloudtrail)
	- API calls to EC2 and EBS 

EBS and Instance Store 
- Both block storage devices 
- EBS can persist, Instance cannot, it does not have to be attached to an EC2
- Instance store is the fastest storage EC2 can have 
- Can attach multiple EBS instances to EC2
- Root EBS volumes are deleted upon EC2 termination by default 
	- Can be protected from deletion upon EC2 termination 
- Elastic EBS sizes can increase volume size dynamically 
- To migrate EBS across AZ's, first make a snapshot of the EBS, copy the snapshot and create EBS from a snapshot in another AZ (can chagne the size and type)

EBS types 
- General purpose SSD 
	- Up to 16,000 IOPS
	- Can be used as boot volume 
- SSD IO provisioned 
	- Up to 64,000 IOPS 
	- Can be used as boot volume 
- HDD throughput optimized 
	- Throughput intensize (not good for random access)
	- Lower cost 
	- Cannot be used as boot volume 
- HDD Cold 
	- Lowest cost 
	- Cannot be used as boot volume 

EBS snapshot 
- EBS are AZ specific 
- Snapshots are stored in S3 can be used to migrate EBS across AZ 
- Even though snapshots are taken incrementally, only the latest snapshot neeed to be retained to fully create the volume 
- To take a consistent snapshot, write must be paused. If that is not possible EBS must be first detached 

RAID 
- RAID 0
	- Data written on different disks 
	- Increases throughput but not redundancy 
- RAID 1
	- Mirroring data on different disks 
	- Increases redundancy but not throughput 
- RAID 10 
	- Combination of RAID 0 and 1

EBS encryption 
- Encryption is NOT enabled by default, it must be enabled 
	- Encryption is supported on all EBS types 
	- Encryption is available for most instance stores 
- Encryption can only be enabled at volume creation time 
- Snapshots of encrypted volumes are automatically encrypted 
- To encrypt and existing volume 
	- First create a snapsot of the volume 
	- Create an encrypted copy of the snapshot 
	- Create a volume based on the encrypted snapshot 

Monitoring EBS and instance store 
- Cloudwatch 
	- Bytes read/write 
	- Monitoring for EBS 
		- Basic: every 5 mins 
		- Detailed:  every minute 
- Cloudtrail 
	- API calls are logged 
	- Including those requests from console 

Data Lifecycle manager 
- Automates the creation, retention and deletion of EBS snapshots 
- Enforcing regular backups 
- Retain backups for compliance 
- Delete unnecessary snapshots to reduce costs 
