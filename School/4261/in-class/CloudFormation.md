CloudFormation Best Practices 
- Use CloudFormation to make changes to your landscape rather than going directly into the resources 
- Make use of Change sets to identify potential trouble spots in your updates
- Use Stack Policies to explicitly protect sensitive portions of your stack 
- Use a version control system such as CodeCommit or Github to track changes to templates 
- AWS Serverless Application Model (SAM) is an extension of AWS CloudFormation that is used to package, test and deploy serverless applications 

Opsworks
- Managed instances of 
	- Chef
	- Puppet 
- AWS OPSWORKS for CHEF
	- Automation platform that enables devlopers and system administratiors to streamline the process of deploying, managing, and scaling infrastructure and applications (contrast to CloudFormation which is only for AWS infrastructure)
	- Cornerstone in the DevOps toolchain 
- AWS OPSWORKS for Puppet 
	- Similar function to Chef 
	- Most organizations choose either Chef or Puppet 
- AWS OPSWORKS Stacks 
	- AWS creation, uses chef architecture 

AWS Config 
- AWS resource inventory 
- Configuration history 
- AWS config vs CloudTrail 
	- AWS config
		- "What did my AWS resource look like?"
	- CloudTrail
		- "Who made an API call to modify this resource"
- Compliance auditing 
- Security analysis 
- Resource change Tracking 
- AWS config Rule 
	- Check desired conditions for violations 
		- Is backup enabled on RDS?
		- Are EBS volumes encrypted?

System Manager 
- Provies visibility and control of infrastructure on AWS 
- Operations performed through system manager 
	- Inventory: e.g. files, network configurations, windows services, registries, updates
	- Configuration compliance: scan for patch compliance and configuration inconsistencies 
	- Automation: automate common and repetitive IT operations 
	- Patch manager: deploy OS and software patches across large group of EC2 instances 
	- Parameter store: centralized store to manage configuration data, including passwords 

Devops tools 
- AWS Proton
	- Service Templates that define the AWS compute, storage, networking, and CI/CD infrastructure for applications
	- The organization's developers can then select an existing Service Teplate, specify a source code origin, and deploy a new application
	- Avoid mistakes by enforcing standards 
- Step function
	- Low-code platform through visual workflow interface to integrate Serverless components (lambda, DynamoDB, Fargate, etc.)
- Simple workflow (SWF)
	- Managing distributed and asynchronous task-based workflows 
- Datapipeline 
	- Orchestrate regular movement of large amounts of data
	- Output sent to S3, DynamoDB or EMR 
- AWS X-ray
	- Debugging tool for distributed application (EC2, ECS, Lambda, SQS, SNS etc.)
- Codepipeline
	- AWS CI/CD service for the building, testing, and deploying code changes 
- Codebuild
	- AWS CI/CD service for compling source code, run tests, produce deployable artifacts 
- Codedeploy
	- Automate software deployment to EC2, lambda, etc
- Codestar
	- Streamline the setup and management of development workflows, at project level (contrast with codepipeline, codebuild, and codedeploy)

Migration and Synchronization 
- Migration hub
	- Track the progress of application migrations across multiple AWS and partner solutions 
- Applicaiton discovery service 
	- Collects and presents configuration, usage, and behavior data from your servers to help you better understand your workloads
- Server Migration Service (SMS)
	- Automate, schedule, and track incremental replicaitons of live server volumes, making it easier for you to coordinate large-scale server migrations 
- Datasync 
	- Transfer service that simplifies, automates, and accelerates moving data between on-premises storage systems and AWS Storage services, as well as between AWS Storage services. Built in data encryption for security 
- Appsync 
	- Provides GraphQL APIs for web and mobile applications 
	- GraphQL provides a flexible and efficient wat to query, mutate, and subscribe to data, allowing clients to retrieve only the data they need in a single request 
	- Popular with web and mobile appliations 