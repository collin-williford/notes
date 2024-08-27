Design trade-offs
- As you design a solution, think carefully about trade-offs so you can select an optimal approach 
	- Evaluate trade-offs so you can select an optimal approach 
	- Examples of trade-offs include the following 
		- Trace consistency, durability, and space for time and latency to deliver higher performance 
		- For new features, prioritize speed to market over cost 
	- Base design decisions on empirical data 

Implementing Scalability 
- Ensure that your architecture can handle changes in demand 
	- users rarely experience service interruption 
	- Amazon EC2 Auto Scaling is alerted and scales out 
	- New server is ready before capacity is reached 

Automating your enviroment 
- Automate the provisioning, termination and configuration of resources 
	- Application server crashes 
	- Amazon CloudWatch automatically detects the unhealthy instance 
	- Amazaon EC2 Auto Scaling automatically launches and configures an identical server 
	- An Alarm notifies the administrator 
	- CloudWatch automatically logs the action to a change management solution 

Using IaC (Infrastruction as Code)
- Provision your comuting infrastructure using code instead of manual processes 
	-  Rapidly deploy duplicate enviroments 
	- Reduce configuration errors from manual configuration 
	- propagate changes consistently to all stacks 

Treating resources as disposable 
- Take advantage of the dynamically provisioned nature of cloud computing 
	- Automate deployment of new resouces with identical configurations 
	- Stop resources that are not in use 
	- Test updates on new resources, and then replace old resources with updated ones 

Using loosely coupled components 
- Design architectures with independent components 
	- Best practice 
		- Web servers -> Elastic Load Balancing (ELB) -> Application Servers 
	- Anti-pattern 
		- Web servers -> application servers 

Designing services, not servers
- Use the breadth of AWS services. Don't limit your infrastructure to servers
	- When appropriate, consider using containers or a serverless solution 
	- Message queues can handle communication between applications
	- Static web assets can be stored off server, such as on Amazon Simple Storage Service (Amazon S3)
	- User authentication and user state storage can be handled by managed AWS services 

Choosing the right database solution 
- Match technology to the workload, not the other way around 
	- Read and write needs 
	- Total storage requirements 
	- Typical storage requirements 
	- Typical object size and nature of access to these objects
	- Durability reqirements 
	- Latency requirements 
	- Maximum concurrent users to support 
	- Nature of queries 
	- Required strength of integrity controls 

Avoiding single points of failure
- Assume everything fails. Then, design backwards
- Under Normal operations 
	- Application servers -> database server (primary) -> database server (secondary)
		- create a secondary (standby) database server and replicate the data
- Upon failure
	- Application servers -> database server (secondary)
		- If the main database server goes offline, the secondary server picks up the load 

Optimizing for cost
- Take advantage of the flexibiligy of AWS to increase your cost efficiency 
	- Are my resources the right size for the job?
	- Which metrics should I monitor?
	- How do I turn off resources that are not in use?
	- How often will I need to use this resource?
	- Can I replace any of my servers with managed services?

Using caching
- Minimize redundant data retrieval operations, improving performance and cost
- First request
	- User <--> internet <--> edge node <--> S3 bucket origin with dog.jpg
- Second and subsequent requests
	- User <--> internet <--> edge node with dog.jpg

Securing your entire infrastructure 
- Build security into every layer of your infrastructure 
	- Use managed services 
	- Log access of resources
	- Isolate parts of your infrastructure 
	- Encrypt data in transit and at rest 
	- Enforce access control granularly, using the principle of least privilege 
	- Use multi-factor authentication (MFA)
	- Automate your deployments to keep security consistent 

Key takeaways
- As you design solutions, evaluate trade-offs and base your decisions on empirical data
- Follow these best practices when builidng solutions on AWS
	- Implement scalability 
	- Automate your enviroment 
	- Treat resources as disposable 
	- use loosely-coupled components
	- Design services, not servers
	- Choose the right database solution 
	- Avoid single points of failure
	- Optimize for cost 
	- Use caching 
	- Secure your entire infrastructure 