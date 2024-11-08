EFS 
- Data stored redundantly across multiple AZs
- Supports thousands of concurrent connections from EC2's from different AZs 
- Does not work with Windows
- Performance 
	- General purpose 
	- Max i/o 
- Throughput 
	- Bursting - through put scales with file system size 
	- Provisioned i/o
- Encryption 
	- Encryption key managed by KMS 
	- Encryption at rest 
	- Encryption on the move with TLS 

Other AWS file systems 
- FSx for Windows 
	- Fully managed file system works with Windows 
- FSx for Lustre 
	- High performance file systems for LINUX only 
	- For HPC, ML financial modeling 
	- Works natively with S3, access S3 objects as files 

Security Group 
- Reflect the role played by an instance of an AWS service (web server, database, EC2, etc)
- Add rules to control access to the instance at the network traffic level 
- Restrict access (only from a given source security group)
- Use Cloudtrail to track changes of security groups for audit trail 
- Act as a "virtual firewall"
- It is stateful 
- Security group chaining 

IAM Role 
- Identity based access 
- Can be assumed by either a user or an instance 
- Access managemtn from the perspective of a service instance 
- Operates at the API level opposed to network traffic 

Use Cases
- DB on EC2 
	- Ultimate control
	- Perferred DB on available on RDS 
- RDS 
	- Relational DB
	- OLTP
	- structured data
	- app needs RDBMS 
- DynamoDB 
	- unstructured data
	- name/value pair 
	- in-memory + persistence 
	- high i/o
	- dynamic scale 
- Redshift 
	- Data warehouse
	-  massive amount of data 
	- Primarily OLAP (Analysis workload)
- Neptune 
	- Relationship between objects a major portion of data value 
- Elasticache 
	- Fast temporary storage for small amounts of data 
	- high volatle data 
- S3 
	- BLOB 
	- static websites 
- Athena 
	- Serverless analysis tools using SQL over S3
- Glue 
	- Extract, Load, and Transform (ELT) service to perpare data for analytics 
- Opensearch 
	- Open source fork of elastisearch and kibana for visual analytics 

RDS capacity provisioning 
- General purpose (for most applications) SSD (gp2)
	- 3 IOPS per GB (min 20GB, max 64TB)
	- For 100GB, 300 IOPS
	- Max 16,000 IOPS (5,334 GB)
	- More complicated pricing is available 
- Provisioned IOPS SSD (io1)
	- Provision n IOPS 
	- Throughput = n / DB page size 
	- E.g.
		- MariaDB is 16KB
		- Oracle, PostgresSQL, and Microsoft SQL Server are 8KB 

Replication and Performance 
- Multi-AZ deployment does not increase performance 
- Multi-AZ deployment improves durability 
	- Failover is possible, but can take 1 to a few minutes 
	- AWS changes the DNS record 
- Read replicas increase performance 
- Aurora 
	- Up to 15 replicas (compared to 5 for MYSQL)
	- Automatic failover without data loss (within the same region)
	- Global database 
		- Span multiple regions 
		- Multi-region latency less than 1 second 
		- Aurora serverless 
			- On-demand, autoscaling 

RDS snapshots 
- Backup database in S3
- i/o suspende while taking the snapshot 
- Resourced database will always be a new RDS instance 

RDS Encryption 
- Encryption can be enabled when creating a database 
- Cannot add encryption to an existing unencrypted database 
	- Create a snapshot of the database 
	- Encrypt the snapshot 
	- Resource database from the encrypted snapshot, the new database will be encrypted 

DynamoDB 
- Serverless no-sql database 
- Autoscaling 
- DynamoDB Accelerator (DAX)
	- In-memory cache, for 10x performance increase 
- Global table 
	- Automatic replication across regions 
		- Supports strongly consistent reads only in a given region 
- DynamoDB Stream 
	- Captures time sequenced of item-level modifications to DynamoDB 
	- Store them in a log for 24 hours 
	- Often used as a trigger for lambda 

Keys in DynamoDB 
- Partition key (hash key) contains single value 
	- e.g. last name 
	- Does not have to be unique within the database 
- Primary key: must be unique within the database 
	- Single partition key (e.g. email)
	- Combination of partition key and sort key (e.g. last name and first name)
- DynamoDB distributes items according to partition key 
	- E.g. items with the same last name are stored together 
- Hot partition 
	- A lot of read and write happen within a given partition 
	- To avoid hot partition, make partition key as specific as possible 

DynamoDB Capacity provisioning 
- Auto scaling vs capacity reservatio n
- Reading capacity unit (RCU) per second 
	- 4KB per RCU for strong consistency read 
	- 8KB per RCU for eventual consistency read 
- Write capacity unit (WCU) per second 
	- 1KB for each WCU 

