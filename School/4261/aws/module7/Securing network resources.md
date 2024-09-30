Security layers of defense 

Security groups and network ACL scope 
- Security groups protect resrouces in the same way an apartment door only lets in the apartment tenant using a key 
- Network ACLs protect subnets in the same way an apartment doorman only lets in tenants living in the building 

Network ACL 
- A network access control list (network ACL) is an optional layer of security for your subnet. It acts as a firewall for controlling traffic in an out of one or more subnets.

Comparing security groups and network ACLs
- Security groups
	- Operate at resource level 
	- Specify allow traffic rules only 
	- Rules are stateful
		- Response traffic is automatically allowed back through the security group 
	- All rules are evaluated 
	- In a new security group, no inbound traffic is allowed by default
	- In a new security group, all outbound traffic is allowed by default 
- Network ACLs
	- Operate at subnet level
	- Specify deny and allow traffic rules 
	- Rules are stateless
		- Response traffic is always evaluated against inbound or outbound rule set 
	- Rules are evaulated in number order and evaulation stops if a match is found 
	- In a new network ACL, all inbound traffic is allowed by default 
	- In a new network ACL, all outbound traffic is allowed by default 

AWS Network Firewall
- Network firewall and intrusion detection and prevention service for an Amazon VPC
- Adds an additional layer of security 
- Routes external VPC traffic through AWS Network Firewall to protect subnet resources 

Key Takeaways:
- Secure AWS infrastructure with multiple layers of defense 
- A security group in a VPC specifies which traffic is allowed to or from AWS resources. It is stateful 
- A newtwork ACL allows or denies specific inbound or outbound traffic at the subnet level. It is stateless
- Route external VPC traffic through AWS Network Firewall to add an additional layer of traffic security 
- Use a bastion host to administrate private subnet resources from an on-premises enviroment

