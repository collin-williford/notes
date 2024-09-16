Amazon RDS Proxy
- Fully managed, highly available database proxy for Amazon RDS
- More scalable
	- Pools and shares database connections for improved application scaling 
- More resilient 
	- Reduces database failover times for Aurora and Amazon RDS databases by up to 66 percent for Amazon RDS Multi-AZ databases
- More secure
	- Enforces IAM authentication and stores credentials in AWS Secrets Manager 

Connection pooling: Improved scalability 
- RDS Proxy is located between the application and the database
- A large number of open connections to the database server exhausts database, memory and compute resources
- With RDS Proxy, the database receives fewer connections so it can work efficiently

Seamless and fast failover: Improved availability 
- Application connections are preserved 
- Transactions are queued during failovers
- RDS Proxy detects failovers and connects to standby database

Steamlined authentication: Improved application security 
- IAM <--> Amazon ECS application -> RDS Proxy Instance <--> Secrets Manager --> Aurora database instance 

Backing up data in Amazon RDS
- Use Case
	- Automated Backups
		- Restore a database instance to a specific point in time 
	- Database Snapshots
		- Back up a database instance in a known state, and then restore it to that specific state
- Backup Frequency 
	- Automated Backups
		- Daily during your backup window (transaction logs are captured every 5 minutes)
	- Database Snapshots 
		- User-initiated (as frequently as the user chooses)
- Retention Period 
	- Automated Backups 
		- The default is 7 days but it can be set to up to 35 days. The backups can be automatically deleted after any retention period 
	- Database Snapshots 
		- Kept until the user explicitly deletes it 
- Sharing with Other AWS Accounts 
	- Automated Backups 
		- Cannot be shared (needs to be copied to a manual snapshot first)
	- Database Snapshots 
		- Can be shared (shared snapshots can be copied by other AWS accounts)

Amazon RDS cross-region backups
- Region 
	- Virtual Private Cloud
		- Availability Zone 1
			- Private Subnet
				- Primary Database 
					- Amazon RDS
				- Snapshots
					- EBS volume 
				- Copy both to an S3 bucket controlled by Amazon RDS
- Region 
	- Cross-Region copy
	- Copy the bucket in the other region to this region 

Amazon RDS encryption for backups
- Amazon RDS can encrypt your RDS DB instances 
	- Data at rest by using AWS KMS 
	- Data in transit by using SSL/TLS
- Steps to back up an unencrypted database 
	- Take a snapshot of the existing unencrypted database instance 
	- Create a copy of the snapshot, and enable the encryption option 
	- Restore the encrypted snapshot to a new database instance 

Key Takeaways
- RDS Proxy is a fully managed, highly available database proxy for Amazon RDS
- By using a Multi-AZ approach, Amazon RDS synchronously replicates data to provide high availability. There is automatic failover to the standby instance 
- With read replicas, Amazon RDS asynchronously replicates data to provide high scalability. The standby instance can be manually promoted to stand alone 
- Amazon RDS provides different options for backing up and restoring database instances: automated backups and database snapshots. It offers encryption for data at rest and in transit 

