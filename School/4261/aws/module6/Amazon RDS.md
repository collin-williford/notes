Amazon Relational Database Service 
- Amazon RDS
	- Is a managed relational database service to deploy and scale relational databases 
	- Supports multiple database engines 
	- Uses Amazon Elastic Block Store (Amazon EBS) volumes for database and log storage 

Benefits of Amazon RDS
- Lower administrative burden 
	- You don't need to provision your infrastructure or install and maintain database software 
- Highly scalable 
	- You can scale up or down the compute and memory resources powering your deployment 
- Available and Durable 
	- You can configure automated backups, database snapshots, and automatic host replacement 
- Secure and Compliant
	- You can isolate your database in your own virtual network 

Amazon RDS database architecture
- RDS facilitates the deployment and maintenance of relational databases in the cloud. It manages a specialized EC2 instance that provides computing capacity.
- Amazon RDS instances are isolated database environments that can contains multiple user-created databases. Each database contains your organization's data 
- The database engine allows for storing, sorting, and retrieving your data 

Architecture diagram of a database layer
- AWS Cloud
	- Virtual private cloud (VPC)
		- Public subnet 
			- Application EC2 instance
		- Private subnet
			- Amazaon RDS database instance 

Aurora 
- Is a rational database management system (RDBMS) build for the cloud with fully MySQL  and PostgreSQL compantability 
- Is managed by Amazon RDS 
- Provides high performance and availability at one-tenth of the cost 
- Delivers Multi-AZ deployments with Aurora Replicas 

Aurora database clusters 
- An Aurora database cluster includes one or more database instances and a cluster volume that manages the data for those database instances 
- An Aurora cluster volme is a virtual database storage volume that spans multiple Availability Zones, and each Availability Zone has a copy of the DB cluster data 

Aurora Serverless
- Is an on-demand auto scaling configuration for Aurora 
- Provides hands-off capacity management 
- Provides fine-grained scaling 
- Is suitable for the following:
	- Variable workloads 
	- New applications 
	- Development and testing 
	- Capacity planning 

Amazon RDS use case
- Banking transactions
	- suitable for online transaction processing (OLTP) transactions. OLTP stores and updates transactional data reliably and efficently in high volumes 

Amazon RDS EC2 instance types and sizing 
- General purpose (T4g, T3, M6g, M5)
- Memory-optimized (R6g, R5, X2g, X1E)

Amazon RDS security best practices 
- Run your DB instance in VPC for the greatest possible network access control 
- Use AWS identity and Access Management (IAM) policies to assign permissions for managing Amazon RDS resources 
- Use security groups to control connecting IP addresses and resources
- Use SSL or TLS connectinos with database instances running certain database engines 
- Encrypt database instances and snapshots at rest with an AWS key management service (AWS KMS) key 
- Use the security features of your database engine to control database access

Key Takeaways
- Amazon RDS is a managed relational database service that can deploy familiar database engines 
- Aurora is a managed relational database engine built for the cloud. Aurora Serverless provides support for Aurora on-demand auto scaling. 
- Amazon RDS provides a selection of instance types that are optimized to fit different relational database use cases
- Differences in performance, scalability, failover, storage, high availability, backup, and database versions will determine which relational database is the optimum selection 

