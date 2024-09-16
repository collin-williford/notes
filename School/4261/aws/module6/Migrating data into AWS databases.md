AWS DMS
- Is a managed migration and replication service 
- Helps move existing database and analytics workloads to and within AWS 
- Supports most widely used commerical and opern source databases
- Replicates data on demand or on a schedule to replicate changes from a source 

AWS DMS Homogeneous migration 
- On-premises data center 
	- On-premises MySQL database
		- to AWS DMS replication task via Secure endpoint 
- AWS Cloud
	- AWS DMS
		- EC2 Instance with profile 
			- AWS DMS replication task via Secure endpoint 
	- task to Aamazon RDS MySQL database 

Tools for heterogeneous database migrations 
- Database discovery tool
	- AWS DMS Fleet Advisor 
		- Automatically inventoryies and assesses on-premises database and analytics server fleet 
- Schema conversion tools 
	- AWS Schema Conversion Tool (AWS SCT)
		- Converts your score schema and SQL code into an equivalent target schema and SQL code 
	- AWS DMS Schema Conversion 
		- Is a centrally managed service for schema assessment and conversion available within AWS DMS workflows 

AWS DMS heterogeneous migration with AWS SCT
- Same as w/ AWS SCT but from On-prem database to AWS SCT then direct to AWS DMS replication task 

AWS DMS replicates data from a database into a data lake 
- On-premises data center 
	- Database (Student information system)
- AWS Cloud 
	- AWS DMS
		- AWS DMS replication task 
	- S3 raw data bucket 
- Database -> secure endpoint -> AWS DMS replicaiton task -> target endpoint -> S3 raw data bucket 

Key takeaways 
- AWS DMS is a managed migration and replication service that helps you move your databases and analytics workloads to AWS quickly and securely 
- You can migrate between source and target endpoints that use the same database engine (homogenous migration) and migrate between source and target endpoints that use different database engines (heterogenous migration)
- AWS SCT and AWS DMS Schema Conversion are tools for schema and code conversion 

