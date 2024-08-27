Authentication and authorization 
- Authentication 
	- Who is requesting access to the AWS account and the resources in it?
		- It's important to establish the identity of the requester through credentials 
		- The requester could be a person or an application 
- Authorization
	- After the requester has been authenticated, what should they be allowed to do?
		- Determine whether to allow or deny the request 

AWS Identity and Access Management (IAM)
- Controls individual and group access to your AWS resources 
- Integrates with other AWS services 
- Provides federated identity management 
- Supports multi-factor authentication (MFA)
- Allows granular permissions 

IAM terminology 
- IAM resource
	- User, group, role, policy and identity provicer objectes stored in IAM 
- IAM entity 
	- IAM resource objects that are used by AWS for authentication (users and roles)
- IAM identity 
	- IAM resouce objects that can be authorized in policies to perform actions and access resources (user, group or role)
- Principal 
	- Person or application that can sign in and make requests to AWS 

Using IAM to control access to AWS resources
- IAM user
	- A person or application that can authenticate with an AWS account 
- IAM group 
	- A collection of IAM users who are granted identical authorization 
- IAM role 
	- An identity that is used to grant a temporary set of permissions to make AWS service requests 
- IAM policy 
	- The document that defines which resources can be accessed and the level of access to each resource 

IAM credentials for authentication 
-  Sign into the AWS management console 
	- Credentials needed
		- Username and password
- Run commands from the AWS Command Line Interface (AWS CLI)
	- Credentials needed
		- AWS access key 
- Make programmatic calls to AWS 
	- Credentials needed
		- AWS access key 

Best practices to secure access 
- Follow the principle of least privilege 
- Enable Multifactor authentication (MFA)
- Require human users to access AWS by using temporary credentials 
- Rotate access keys for use cases that require long-term credentials 
- Use strong, complex passwords
- Secure local credentials 
- Use AWS Organizations
	- Use Organizations to consolidate multiple AWS accounts to manage billing, access control, and resources centrally 
- Enable AWS CloudTrail
	- By enabling CloudTrail, you can have a record of all the actions that are taken in an account, which makes it easier to identify possible security risks and comply with auditing requirements 
- Protect the root user 

Protecting the root user
- For daily tasks, create an administrative user in AWS IAM Identity Center (successor to AWS single sign-on)
- Only use the root user for tasks that other users cannot perform 

Setps to set up an admin user
- As the root user, create an admin user
- Use the admin user for daily tasks 
	- Log in as the root user. Set up MFA for the root user 
	- Create a new admin user (john) with permissions, add MFA, and download the programmatic keys 
	- Log out as the root user 
	- Log in as admin user 
	- Create additional user 
		- Each user has a seperate policy with permissions 

Best practices: IAM users and groups 
- You can attack an IAM policy to an IAM user, group, role or an combination of these resources 
- Attach IAM policies to IAM groups, then assign IAM users to these IAM groups

IAM roles 
- Characteristics
	- Provides temporary security credentials 
	- Isn't uniquely associated with one person 
	- Can be assumed by a person, application or service 
	- Is often used to delegate access 
- Common use cases 
	- Application that runs on Amazon Elastic Compute Cloud (Amazon EC2)
	- Cross-account access for an IAM user 
	- Mobile applications 

Three examples of using and IAM role 
- An IAM user in AWS accoutn 1 needs temporary access to an application that rusn on an EC2 incance. You first create an IAM policy with the necessary permissions. You then create an IAM role and attack the policy to the role. The IAM user can now asume the role and access the EC2 instance 
- An application that runs on an EC2 instance needs access to an S3 bucket. After you create an IAM role with the necessary permissions, you add the role to an instance profile and attach the profile to the instance. The application can then access the S3 bucket 
- An IAM user in AWS account 2 needs to access and S3 bucket in AWS account 1. You create a cross-account IAM role in account 1 that defines account 2 as a trusted entity. An IAM user in account 2 can then switch roles to the cross-account role and access the S3 bucket in account 1 

Key takeaways:
- Use the IAM service to configure fine-grained access control to AWS resources 
- The account root user has full access to all AWS account resources. Don't use the root user for day-to-day interactions 
- A best practice is to attach IAM policies to IAM groups and then assign IAM users to these IAM groups 
- An IAM role provides temporary security credentials. With a role you can define a set of permissions to access the resources that a user or service needs 