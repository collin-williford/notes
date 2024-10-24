The need for reactive architectures 
- Applications need to handle large amounts of data with sub-second response times while having close to 100 percent uptime 
	- Elastic 
	- Responsive
	- Resilient 
	- Message-driven 

Achieve elasticity with scaling 
- Elasticity is the ability of infrastructure to expand and contract as capacity requirements change 
- Scaling is the ability to increase or decrease the compute capacity of your application
	- Vertical scaling replaces a resource with a different-sized resource 
	- Horizontal scaling adds or removes resources available to the application 

Amazon EC2 Auto Scaling 
- Manages a logical collection of Amazon Elastic Compute Cloud (Amazon EC2) instances called an Amazon EC2 Auto Scaling group across Availablity Zones 
- Launches or retires EC2 instances configured by launch templates 
- Resizes based on events from scaling policies, load balancer health check notifications, or scheduler actions 
- Integrates with Elastic Load balancing (ELB) to send new instances registrations and recieve health notifications 
- Balances the number of instances across Availablity Zones 

Amazon EC2 Auto Scaling group components 
- Capacity 
	- Minimum instances 
	- Maximum instances 
	- Desired instances 
- Launch template 
	- EC2 instance configuration 
	- Amazon Machine Image (AMI) ID 
	- Version 
- Load Balancer 
	- Receives load balancer health checks 
	- Registers new instances with load balancer 
- Scaling mechanisms 
	- Schedule action 
	- Dynamic scaling policies 
	- Perdictive scaling policy 

Amazon EC2 Auto Scaling mechanisms 
- Schedule actions 
	- Scale based on a date and time 
	- Are for predictable workloads 
- Dynamic policies 
	- Scale based on traked metrics 
	- Are for moderately spiky workloads 
- Predictive policy 
	- Scales based on previous traffic patterns with machine learning 
	- Is for workload traffic that can be predicted with a pattern 

More AWS scaling options 
- AWS Auto Scaling 
	- Use a scaling plan to configure auto scaling for multiple resources 
	- Scale multiple AWS services 
		- Amazon Aurora 
		- Amazon EC2 Auto Scaling 
		- Amazon Elastic Container Service (ECS)
		- Amazon DynamoDB 
- AWS Application Auto Scaling 
	- Scale multiple resouces with target tracking, step scaling, or scheduled scaling 
	- Scale multiple AWS services:
		- AWS Auto Scaling services 
		- AWS Lambda functions 
		- Amazon SageMaker 
		- Amazon ElastiCache for Redis 

Key takeaways:
- With Amazon EC2 Auto Scaling, you can create a group to manage a logical collection of EC2 instances, called an Amazon EC2 Auto Scaling group 
- A group has capacity settings that specify the minimum, maximum and desired number of instances required to run an application 
- Group size can be scaled in and out with schedule actions, dynamic policies and predictive policies 
- To scale more services than EC2 instances, use AWS Auto Scaling or Application Auto Scaling 

