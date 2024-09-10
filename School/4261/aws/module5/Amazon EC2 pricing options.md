AWS Free Tier: Amazon EC2
- 12 months free
	- 750 hours per month of t4g.small instance dependent on region 
	- 750 hours per month of Linux, RHEL, or SLES t2.micro or t3.micro instance dependent on region 
	- 750 hours per month of Windows t2.micro or t3.micro instance dependent on reigon 

Amazon EC2 pricing models 
- Purchase models 
	- Emphasis on providing big savings through different use cases
- Capacity reserved models 
	- Emphasis is on providing reserved instances to guarantee that you have them when you need them 
- Dedicated models 
	- Emphasis is on providing dedicated hardware that will help you meet compliance and regulation requirements 

Amazon EC2 purchase models 
- On-Demand
	- Pay for compute capacity by the second or by the hour with no long-term commitments 
	- Recommended use cases
		- Spiky workloads 
		- Experimentation workloads 
- Reserved 
	- Make a 1-year or 3-year commitment and receive a significant discount off on-demand prices
	- Recommended use cases:
		- Commiteed workloads
		- Stead-state workloads
- Savings Plans 
	- Same discounts as Reserved Instances with more flexibility in exchange for a $/hour commitment 
	- Recommended use cases
			- All Amazon EC2 workloads
			- Amazon EC2 workloads that might need flexiblity with commited usage
- Amazon EC2 Spot 
	- Spare Amazon EC2 capacity at a substantial savings off the On-Demand Instance prices 
	- Recommended use cases
		- Fault-tolerant workloads
		- Flexible workloads 
		- Stateless workloads 

Amazon EC2 Capacity Reservations
- Capacity reservations let you reserve compute capacity for Amazon EC2 instances in a specific Availability Zone 
	- On-Demand Capacity Reservations
		- This guarantees that you always have access to EC2 capacity when you need it, for as long as you need it 
		- Recommended use cases
			- Workloads that need to meet regulatory requirements for high availabilty 
			- Workloads that require capacity assurance 
	- Amazon EC2 Capacity Blocks for ML 
		- Reserve GPU instances for a future date to run any of your machine learning workloads
		- Recommended use cases
			- Training and fine-turning ML models 
			- Running experiemnets and building prototyes 
			- Planning for future surges in demand for ML applications 

Amazon EC2 dedicated options 
- Amazon EC2 dedicated options provide EC2 instance capacity on physical servers that are dedicated for your use 
	- Dedicated Instances 
		- Per-instance billing 
		- Automatic instance placement 
		- Isolates the host that run your instances 
	- Dedicated Hosts
		- Per-host billing 
		- Visiblity of sockets, cores, and host ID 
		- Affinity between a host and an instance 
		- Targeted instance placement 
		- Add capacity by using an allocation request 
		- Lets you use your server-bound software licenses and address compliance requirements 

Amazon EC2 cost optimization guideline 
- To optimize the cost of Amazon EC2 instances, combine the available purchase options 

Key takeaways:
- Amazon EC2 pricing models include On-Demand instances, REserved Instances, Savings Plans, Spot Instances, and Dedicated Hosts 
- Per-second billing is available only for On-Demand Instances, Reserved Instances, and Spot Instances that run Amazon Linux or Ubuntu
- Use a combination of Reserved Instances, Savings Plans, On-Demand Instances, and Spot Instances to optimize Amazon EC2 compute costs


