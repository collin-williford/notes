Some terminologies 
- NAT Gateway (managed service) vs. NAT instance (you manage) 
	- Both provide NAT translation, must be in public subnet 
	- Egress traffic only 
- Egress-only internet gateway 
	- IPv6 only 
- VPN 
	- Customer Gateway: your side of the VPN 
	- Virtual private gateway: AWS side of the VPN 
- Internet gateway 
- VPC endpoint: Enables private connectivity to services hosted in AWS, from within your VPC without using an Internet Gateway, VPN, Network Address Translation (NAT) devices, or firewall proxies 

Default VPC vs. Non-Default VPC 
- Default VPC 
	- Pre-configured: 
		- When you create a default VPC, it comes with a main table pre-configured by AWS. This route table is set up to allow instances in the VPC to communicate with each other and to access the internet 
	- Internet Gateway:
		- The main route table in a default VPC includes a route that allows instances to access the internet via an Internet Gateway (IGW). This setup makes all the subnets in a dafault VPC public subnets by default 
	- Edit Restrictions 
		- While you can add routes to the default route table, the default routes cannot be deleted 
- Non-Default VPC 
	- Manual Configuration 
		- In a non-default VPC, the route tables must be manually configured. When you create a non-default VPC, it comes with a main route table, but it does not have any pre-configured routes for internet access. 
	- No Default Internet Gateway 
		- Non-default VPCs do not come with an Internet Gateway attached. You need to create and attach an IGW if you want your instances to access the internet, and then modify the modify the route table to include a route to the IGW 
	- Flexiblity 
		- you have flexibility with non-default VPCs to create complex network setups. you can create additional route tables for different subnets, defining public and private subnets based on weather or not they have routes to an IGW
	- Security 
		- Since non-default VPCss require manual setup, you have more control over the network access and security. This allows for more tailored configurations that align with specific security and architectural requirements 

Web Application Firewall (WAF)
- Protects web applications from common attacks 
- Rules (regex) match of 
	- HTTP headers, methods, query string, RUI, Body, query parameter values 
- Block suspicious requests 
- Tightly integrated with CloudFront and Load balancer 
- API based administration 

AWS Shield 
- DDOS prevention 
- AWS shield standard comes free with most AWS services 
- AWS Shield Advances provides extra protection 
