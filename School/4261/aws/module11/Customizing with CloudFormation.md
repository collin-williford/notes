How CloudFormation works 
- Template 
	- Define your resources in a template, or use a prebuild template 
- AWS CloudFormation 
	- Upload the template to CloudFormation, or point to a template in an Amazon Simple Storage Service (Amazon S3) bucket. 
- Stack 
	- Run a create stack action. Resoruces are created across multiple services in your AWS account as a running environment 
- Amazon Route 53, Auto Scaling, ELB, EC2
- Stack 
	- The stack retains control of the resources that are created. You can later update stack, detect drift or delete stack 

Scoping and Organizing templates
- Frontend services 
	- Web interfaces, mobile access, and analytics dashboard 
- Backend services
	- Search, payments, reviews, and recommendations 
- Shared services 
	- Customer relationship management (CRM) databases, common monitoring, alarms, subnets, and security groups 
- Network 
	- VPCs, internet gateways, virtual private networks, NAT devices 
- Security 
	- AWS Identity and Access Management (IAM) policies, users, groups, and roles 

Key takeaways:
- CloudFormaiton is an IaC service that you can use to model, create, and manage a collection of AWS resources 
- CloudFormation IaC is defined in templates that are authored in JSON or YAML
- A stack is what you create when you use a template to create AWS resources 
- Actions that are available on an existing stack include update stack, detect drift, and delete stack 



