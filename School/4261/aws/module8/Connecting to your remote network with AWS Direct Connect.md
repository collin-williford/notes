AWS Direct Connect
- Is a dedicated, private, virtual local area network (VLAN) connection that extends on-premises network to include AWS resources 
- Provides a consistent network experience with predictable performance and increased bandwidth and throughput 

Direct Connect use cases
- Hybrid enviroments 
- Large datasets
- Predictable network performance 
- Security and compliance requirements 

Extend an on-premises network to AWS by using Direct Connect 
- Durrect Connect (DX) makes use of Direct Connect locations to extend your on-premises network to AWS by using industry-standard 802.1Q VLANs. By default, these locations are associated with an AWS Region. However, you can access any VPC or public AWS service in any Region (except China) from any supported Direct Connect location 

Direct Connect using Transit Gateway 
- You can also use Direct Connect to connect to a Transit Gateway instead of a virtual private gateway to simplify routing between the on-premises network and multiple VPCs. The transit gateway has a Transit Gateway Direct Connect attachment pointing to a Direct Connect gateway. You can use the Direct Connect gateway to connect to multiple Transit Gateways. The solution uses a transit virtual interface to communicate from the Direct Connect location to the Direct Connect gateway 

Key Takeaways:
- Direct Connect is a dedicated, private, VLAN connection that extends an on-premises network to include AWS resources
	- Use a private virtual interface to connect a Direct connect location to a virtual private gateway 
	- Use a public virtual interface to connect a Direct Connect location to supported AWS services 
	- Use a transit virtual interface to connect a Direct Connect location to a transit gateway throgh a Direct Connect gateway 
- Make your network highly available by using Direct connect as a primary connection and a VPN as a backup connection 
- Make your network highly resilient by connection from multiple on-premises networks to AWS by using multiple Direct Connect locations 

