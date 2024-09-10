AWS runtime computer choices
- AWS offers different compute services to meet the needs of different use cases 
	- Virtual Machines 
		- EC2
			- secure and resizable virtual servers in the cloud that can be used to run workloads of different sizes
	- Containers
		- Elastic Conteiner Service (ECS)
			- Ran Docker container applications on AWS
		- Elastic Kubernetes Service (EKS)
			- Managed Kubernetes service that runs Kubernetes in the AWS cloud and on-premises data centers
	- Virtual Private Servers (VPS)
		- Lightsail
			- Provides developers with compute, storage, and networking capacity and capabilities to quickly deploy and manage websites and web applications in the cloud 
	- Platform as a Service (PaaS)
		- AWS Elastic Beanstalk
			- Solution that runs web applications and services that are developed in languages such as Java, .NET, PHP, Node.js, Python, Ruby, Go and Docker
	- Serverless
		- AWS Lambda
			- A serverless compute solution that runs Java, Go, Powershell, Node.js, C#, Python or Ruby Code 
		- AWS Fargate
			- A serverless compute platform for containers

Computer service category differentiators 
- Each service category offers different levels of infrastructure control and applications deployment speed 
	- VMs, containers and VSPs offer more infrastructure control and customization whereas Platform as a Service and serverless offer faster application depyloyments

Amazon EC2
- Provides VMs (servers) in the cloud
- Provisions servers in minutes
- Can automatically scale capacity up or down as needed
- Enables you to pay only for the capacity that you use 

Amazon EC2 Virtualization 
- An EC2 instance is a VM that runs on a physical host 
- Amazon EC2 instances run as virtual machines on host computers that are located in AWS Availablity Zones. Each VM runs an operating system, such as Amazon Linux or Microsoft Windows. 
- The VMs run on top of a hypervisor layer that's maintained by AWS

Amazon EC2 use cases 
- Complete control of your computing resources, including operating system and processor type.
- Options for optimizing your computer costs
	- On-Demand instances, Reserved Instances, and Spot Instances 
	- Savings Plans 
- Ability to run any type of workload 
	- Simple websites 
	- Enterprise applications
	- Generative artificial intelligence (generative AI) applications 

Steps for provisioning an EC2 instance
- Start with an Amazon Machine Image (AMI), which is the template that Amazon EC2 uses to launch and instance. 
- Select an Instance type. Instance types comprise varyting combinations of CPU, memory, storage and networking capacity 
- if you plant to connect to the instance SSH or Remote Desktop Protocol (RDP), you must specity a key pair 
- When you launch, specify network placement and addressing 
- Assign a new or existing security group to the instance 
- Specify the storage options for the instance 
- If using API calls you can attach a IAM role 
- Optionally specify user data when you launch 

Key takeaways
- Amazon EC2 enables you to run VMs in the cloud and easily scale capacity up or down as needed 
- You can use an EC2 instance when you need complete control of your computing resources and want to run any type of workload 
- When you launch and EC2 instance, you must choose an AMI and and instance type. Launching an instance involves specifying configuration parameters including network, security, storage, and user data settings 