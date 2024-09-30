Amazon S3 endpoint considerations 
- Amazon S3 access point 
	- Interface VPC endpoints
		- Private IP addresses from VPC subnet 
	- Gateway VPC endpoint 
		- Amazon S3 public IP addresses
- On-premises
	- Interface
		- Allows access
	- Gateway 
		- Does not allow access
- Other AWS Region 
	- Inteface
		- Allows access
	- Gateway 
		- Does ot allow access
- Cost 
	- Interface
		- Billed
	- Gateway 
		- Not billed
- Bandwidth
	- Interface
		- Bandwidth of up to 10 Gbps per AZ, and automatically scales up to 100 Gbps 
	- Gateway 
		- No limit
- Packet size
	- Interface
		- Maximum packet size supported is 8500 bytes 
	- Gateway 
		- No limit 

Key takeaways
- VPC resources can access AWS managed services using VPC endpoints
- An interface VPC endpoint uses AWS PrivateLink to access AWS managed services. It incurs cost and has throughput limitations 
- A gateway VPC endpoint integrates directly with Amazon S3 and Amazon DynamoDB. It does not incur cost and has no through limitations 
- Gateway Load Balancer endpoints are used with Gateway Load Balancers to inspect traffic with security appliances



