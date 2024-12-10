Designing for resiliency and recovery 
- Route 53 
	- Provides DNS-based load balancing 
	- Provides basic failover between endpoints or S3 websites 
- ELB 
	- Provides traffic distribution 
	- Makes recovery implementation straightforward 
- Amazon VPN 
	- Provides secure access to your on-premises network resources from your Amazon VPC through a VPN connection 
- AWS Direct Connect
	- Provides the dedicated network connection for fast, consistent data transfer between on-premises and AWS

Supporting Database Recovery 
- Amazon RDS 
	- Save a snapshot in a separate Region 
	- Use read replicas and Multi-AZ deployments
	- Retain automated backups 
- DynamoDB
	- Back up entire tables
	- Use point-in-time-recovery to restore tables 
	- Create backups
	- Use global tables to build a multi-Region, multi-active database 

Replicating and 