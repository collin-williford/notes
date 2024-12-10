Choose containers over AWS Lambda functions 
- Longer than 15 minutes 
	- If a service runs longer than 15 minutes, it isn't suitable for Lambda functions 
- Memory intensive applications 
	- Workloads that use more than 10 GB of memory are not suitable for Lambda functions
- Migrating legacy containers 
	- Containers can ehlp migrate legacy applications running on-premises or on EC2 instances without refactoring or rearchitecting them 
- Cost 
	- Containers can be continously run at a fixed cost 
	- The price to run a Lambda function increases with the number of invocations, duration, and memory allocated 

Container Use Cases 
- Microservice applications 
- Scale machine learning models
- Batch processing 
- Standardize hybrid architecture applications 
- Migrate applications to the cloud 

Creating and deploying Docker containers 
- Dockerfile 
	- Build 
- Container Image
	- Upload 
- Container Repository 
	- Container Image 
		- Pull
- Container orchestration 
	- Compute platform 
		- Deployed containers 

AWS Container Services 
- Registry 
	- Amazon Elastic Container Registory (Amazon ECR)
- Orchestration 
	- Amazon Elastic Container Service (Amazon ECS)
	- Amazon Elastic Kubernetes Service (Amazon EKS)
- Compute Options
	- Amazon Elastic Compute Cloud (Amazon EC2)
	- AWS Fargate
	- AWS Lambda 

Benefits of AWS Fargate 
- No cluster or server management 
	- No server provisioning or maintenance 
	- No cluster packing optimization 
- Per second billing 
	- Only pay for what you use 
- Automatic Scaling 
	- Dynamically scale tasks based on CPU, memory or other metrics
- Suitable for teams new to containers 
	- AWS Fargate usage doesn't require comprehensive knowledge of container technology 

Choosing between Amazon ECS and Amazon EKS 
- Amazon ECS
	- Simplifies cluster creationand maintenance 
	- Automated scaling based on demand 
	- Amazon ECS toolset 
	- New to container cluster architecture 
- Amazon EKS 
	- Provides more control over cluster using a complex interface 
	- Manual configuration of autoscaling groups 
	- Kubernetes toolset 
	- Familiar with Kubernetes cluster architecture and control process 

Key takeaways:
- Choose a container solution instead of Lambda functions when an application requires resources exceeding Lambda service limits 
- Amazon ECR provides a container image repository service 
- Amazon ECS is a container orchestration service with AWS toolkit 
- Amazon EKS is a container orchestration service with Kubernetes toolkit 
- AWS Fargate manages serverless cluster nodes and can be deployed in Amazon ECS and Amazon EKS clusters 

