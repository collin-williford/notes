Amazon EC2 storage overview
- Amazon EBS (SSD-backed only)
	- Root Volume
	- Data Volumes for a single instance 
- Instance store
	- Root Volume
	- Data Volumes for a single instance 
- Amazon Elastic File System (Amazon EFS) \[Linux]
	- Data volues for data that is accessible from multiple Linux instances
- Amazon FSx for Windows File Server
	- Data volumes for data that is accessible from multiple Windows instances 

Instance store
- An instance store provides non-presistent storage to an instance. The data volume is stored on the same physical server where the instance runs 
- Characteristics
	- Temporary block-level storage
	- Uses HDD or SSD
	- Instance store data is lost when the instance is stopped or terminated
- Example use cases
	- Buffers
	- Cache 
	- Scratch data 

Amazon EBS
- Amazon EBS volumes provide network-attached persistent storage to an EC2 instance
- Characteristics
	- is persistent block-level storage
	- Can attach to any instance in the same Availability Zone
	- Uses HDD or SSD
	- Can be encrypted
	- Supports snapshots that are persistent to S3
	- Data persists independently from the life of the instance
- Example use cases
	- Stand-along database
	- General application data storage

Amazon EBS SSD-backed volume types
- Amazon EBS SSD-backed volumes are suited for use cases where the performance focus is on IOPS 
- Volume type
	- General purpose SSD (gp2)
		- Balances price and performance for a wide variety of workloads
		- Recommended for most workloads
		- Can be a boot volume 
	- Provisioned IOPS SSD (io1)
		- Highest-perforamcne SSD volume 
		- Good for mission-critical, low-latency or high-throughput workloads
		- Critical businesses application that require sustained IOPS performance 
		- Large database workloads
		- Transactional workloads
		- Can be a boot volume 

Amazon EBS HDD-backed volume types
- Amazon EBS HDD-backed volumes work well when the focus is on throughput 
- Volume type 
	- Throughput Optimized HDD (st1) 
		- Low-cost volume type 
		- Designed for frequenctly accessed, throughput-intensive workloads 
		- Streaming workloads
		- Big Data
		- Data warehouses
		- Log processing
		- Can't be a boot volume 
	- Cold HDD (sc1)
		- Lowest-cost HDD volume 
		- Designed for less frequently accessed workloads 
		- Throughput-oriented storage for large volumes of infrequently accessed data 
		- Use cases where the lowest storage cost is important 
		- Can't be a boot volume 

Amzaon EBS-optimized instances 
- Certain EC2 instance types can be EBS-optimized 
- Benefits 
	- It provides a dedicated network connection to attached EBS volumes 
	- It incrases I/O performance
	- Additional performance is acheived if using an Amazon EC2 Nitro System-based instance type 
- Usage 
	- For EBS-optimized instance types, optimization is enabled by default 
	- For other instances types that support it, optimization must be manually enabled 

Shared file system for EC2 instances 
- What if you have multiple instances that must use the same storage?
	- Amazon EFS and Amazon FSx for Windows File Server
		- Both satifty the requirement 

Amazon Elastic File System (Amazon EFS)
- Provides file system storage for Linux-based workloads 
- Fully managed elastic file system 
- Scales automatically up or down as files are added and removed 
- Petabytes of capactiy 
- Supports Network File System (NFS) protocols 
- Mounts the file system to the EC2 instance 
- Compatible with all Linux-based AMIs for Amazon EC2

Amazon EFS use cases
- Common workloads and applications examples for Amazon EFS include the following 
	- Home directories
	- File system for enterprise applications 
	- Application testing and development 
	- Database backups
	- Web serving and content management 
	- Media workflows 
	- Big data analytics 

Amazon FSx for Windows File Server
- Provides fully managed shared file system storage for Microsoft Windows EC2 instances 
- Native Microsoft Windows compatibility 
- New Technology File System (NTFS)
- Uses Native Server Message Block (SMB) protocol version 2.0 to 3.11 
- Distributed File System (DFS) Namespaces and DFS Replication 
- Integrates with Microsoft Active Directory and supports Windows access control lists (ACLs)
- Backed by high-performance SSD storage 

Amazon FSx for Windows File Server use cases
- Home directories 
- Lift-and-shift application workloads 
- Media and entertainment workflows 
- Data analytics 
- Web serving and content management 
- Software development enviroments 

Key takeaways 
- Storage options for EC2 instances include instance store, Amazon EBS, Amazon EFS, and Amazon FSx for Windows File Server
- For a root volume, use instance store or SSD-backed Amazon EBS
- For a data volume that serves only one instance, use instance store or Amazon EBS storage 
- For a data volume that serves multipe Linux instances, use Amazon EFS
- For a data volume that serves multiple Microsoft Windows instances, use Amazon FSx for Windows File Server 