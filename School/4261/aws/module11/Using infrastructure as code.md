IaC overview
- IaC is the process of writing a template that provisions and manages your cloud resources 
	- Human readable 
	- Machine consumable 

IaC benefits 
- Rapidly deploy complex environments with configuration consistency 
- Propagate a change to all stacks by modifying the template 
- Clean up by deleting the stack, which deletes all the resources created 
- The key benefits are reusability, repeatability, and maintainability 

Cloud Formation 
- Provides a simplified way to model, create and manage a collection of AWS resources
	- A collection of resources is called a CloudFormation stack 
	- There is no extra charge (pay for only the resources you create)
- Can create, update and delete stacks 
- Enables orderly and predictable provisioning and updating of resources
- Enables version control of AWS resource deployments 

AWS IaC services that use CloudFormation 
- AWS Elastic Beanstalk
	- A fully managed service that automatically launches an AWS environment with your uploaded application code
- AWS Quick Starts 
	- Automated reference architectures based on CloudFormation templates 
- AWS Serverless Application Model (AWS SAM)
	- An extension of CloudFormation with shorthand syntax for building common serverless infrastructure 
- AWS Amplify 
	- A development framework for full stack web and mobile apps that requires less coding and less knowledge of backend integrations 
- AWS Cloud Development Kit (AWS CDK)
	- An open source development framework to model and provision resources through CloudFormation by using familiar programming languages 

Key takeaways:
- IaC is the process of provisioning and managing your cloud resources by writing a template file 
- IaC rapidly deploys complex environments, you can build or update the same complex environments repeatedly 
- Choose an IaC solution based on your use case, relative balance of convenience and control, and the skills of your team 
- CloudFormation is an IaC service to help you create, update, and delete services and architectures 

