AWS Well-Architected Framework network pillars 
- Reliability 
- Security 
- Performance Efficiency 
- Cost Optimization 

Foundations: Plan your network topology 
- Relability 
	- Best practice 
		- Ensure IP subnet allocation accounts for expansion and availability 

Infrastructure protection: Protecting networks
- Security 
	- Best practices 
		- Create network layers 
		- Implement inspection and protection 
		- Control traffic at all layers 

Selection: Network architecture selection 
- Performance Efficiency 
	- Best Practices
		- Understand how networking impacts performance 
		- Evaluate available networking features 
		- Choose network protocols to improve performance

Select the best pricing model 
- Cost Optimization 
	- Best practice 
		- Choose Regions based on cost 

Common anti-patterns and patterns
- Anti-pattern
	- Small VPC with small subnets 
	- Permissive security groups 
	- Direct access to databases 
	- AWS Region far from customers 
- Pattern 
	- Large VPCs with large public and private subnets 
	- Strict security groups layered by server usage 
	- No direct access to databases 
	- AWS Region close to customers 

Key takeaways 
- Ensure IP subnet allocation accounts for expansion and availability 
- Create network layers and control traffic at all layers
- Understand how networking impacts peformance 
- Choose network protocols to improve perfomance 
- Implement Regions based on cost providing low latency and strong data sovereignty 

