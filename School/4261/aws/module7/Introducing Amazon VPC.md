AWS physical infrastructure
- AWS Cloud infrastructure resides in data centers which contain thousands of servers built into racks. Every rack has network routers and switches to route traffic
- Data centers are grouped together in Availability Zones (AZs)
- AZs are connected with single digit millisecond latency network 
- AZs are grouped together in an AWS Region 
- Latency between AWS Regions is 10s of milliseconds

AWS account resource isolation 
- AWS Cloud
	- AWS Account
		- Region 
			- Availability Zone 1
				- EC2 instance 1
			- Availability Zone 2
				- EC2 instance 2
			- Availability Zone 3
				- EC2 instance 3
			- Default Amazon VPC 
				- Spread across the 3 AZs

Amazon Virtual Private Cloud 
- Programmatically defined, logically isolated virtual network similar to a traditional data center network 
- Belongs to one Region 
- Customizable to control traffic flow to and from the VPC
- Sized by a range of private IP addreses called a CIDR block 

Main route table 
- Amazon VPC 10.0.0.0/16
	- Availability zone
		- Subnet_A 10.0.0.0/20
			- EC2 instance A 
			- Private IP address: 10.0.0.5

Public Subnets
- A public subnet with an associated internet gateway allows direct access to the internet
- Every instance in a public subnet requires a private and a public IP address to gain internet access

Elastic IP address
- An Elastic IP address is a public, static address associated with an instance. An Elastic IP address can be transferred to a new Instance 

Private Subnets
- A private subnet does not have direct access to the internet 

NAP IP mapping
- When you don't want to expose a server IP address to other networks or the internet, it's useful to use a NAT device. The NAT device replaces the private IP of the request initiator with its own public IP 

Key takeaways
- An Amazon VPC is a programmatically defined, logically isolated virtual network 
- A public subnet with an internet gateway allows direct access to the internet
- A private subnet does not have direct access to the internet 
- A NAT gateway allows resources in a private subnet to connect to the internet 
- An Elastic IP address can be transferred to a new instance 

