Two common patterns for seperating resource access
- First pattern is to define multiple VPCs in a single AWS account. If you prefer centralized information security management with minimum overhead, you can choose to use a single AWS account 
- The second patterns is to create multiple AWS accounts and define a VPC in each account. In practice, large and small organizations tend to create multiple accounts for their organization. For example, they might create individual accounts for various business units. They can also create seperate accounts for their development, test and production resources 

Advantages and challenges of multiple accounts 
- Advantages 
	- Isolation by business units or departments 
	- Isolation by environment 
	- Isolation of auditing and recovery data 
	- Separation of accounts for regulated workloads 
	- Ease of creating cost alerts for each business unit's consumption 
	- Cost savings
- Challenges 
	- Security management across accounts 
	- Manual processes involved in creating many new accounts 
	- Determination of which organization should be billed
	- Need for centralized governance to ensure compliance and consistency 

AWS Organization 
- Account management service that you can use to consolidate multiple AWS accounts into a centrally managed organization 
- Tier pricing discounts available 
- Includes account creating and management and consolidated biling capabilities 
- Supports centralized policy control over AWS services and API actions using service control policies (SCPs)

Organizations SCPs
- Offer central control over the maximum available permissions for all accounts in your organization 
- Enable control of which services are accessible to IAM users in member accounts 
- Define permissions that affect an entire account 
- Define guardrails, or set limits, on the actions that the account's administrator can delegate to the IAM users and roles in the affected accounts. IAM policies that are defined in individual accounts still apply 
- SCPs cannot be overridden by the local administrator 
- Best Practice
	- It's easier to define policies across multiple accounts in an SCP than to replicate these permissions settings into IAM policy documents in each account 

Examples of scenarios defined in SCPs
- Block service access or specific actions. For example, deny users from disabling AWS CloudTrail in all member accounts 
- Enforce the tagging of resources. For example, do not allow users to launch an Amazon Elastic Compute Cloud (Amazon EC2) Amazon Machine Image (AMI) unless it has a specific tag on it 
- Prevent member accounts from leaving the organization 

Comparing permission boundaries and SCPs 
- Permission boundary 
	- Applies to an IAM entity (user or role)
	- Defines the maximum permissions that the associated identity-based policies can grant to an entity 
	- Does not grant permissions 
	- Typically used to define scope which resources a user or role is allowed to access
	- Example 
		- Allow the IAM role developer to access EC2, S3, Cloudwatch.
	- Result
		- The developer role can only access EC2, S3 and CloudWatch regardless of other policies associated with their role 
- Organization SCP
	- Applies to all members of an organization or OU
	- Defines the maximum permissions for account members of an organization or organizational unit (OU)
	- Does not grant permissions 
	- Typically used to deny access to a set of resources
	- Example 
		- Deny access to Amazon Relational Database Service (RDS) to all members of the Internal IT OU
	- Result 
		- All members of the Internal IT OU will be denied access to Amazon RDS regardless of other policies associated with their identity 

AWS Control Tower
- AWS Control Tower facilitates the set up and governance of secure, multi-account AWS environment
- AWS Control Tower benefits include the following 
	- Automated set up of a new well-architected multi-account environment based on best practices blueprints 
	- Governance of AWS workloads with rules for security, operations and internal compliance 
	- Perscriptive guidance to govern your AWS enviroment at scale 

Key Takeaways:
- Most organizations choose to create multiple AWS accounts and define a VPC in each account 
- Multiple accounts allow for billing consolidation to help save money by grouping together with tiered pricing. It also enables organizations to cleanly seperate different types of resources while providing some security benefits 
- AWS Organizations allows you to considlate multiple AWS accounts into a centrally managed organization 
- SCPs allow you to set limits on permissions across an organization, while permissions boundaries let you set limits on IAM entities (users and roles)
- Users or groups can have multiple policies attached to them that grant different permissions. If a user isn't granted an explicit permission for an action and a resource the user doesn't have those permissions

