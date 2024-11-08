AWS Account 
- Natural boundary for permissions, security, costs and workloads
- Using a multi-account environment is a recommended best-practice for cloud environments 
- But it can be difficult to manage large number of accounts 

AWS organizations
- Simplify account creation by programmatically creating new accounts using AWS CLI, SDK or API 
- Group accounts into organizational units (OUs) or groups of accounts that serve a single application or service 
- Apply tag policies to classify or track resources 
	- Attribute-based access control for users or application 
- Delegate responsiblities for supported AWS services to accounts so users can manage them on behalf of your organization 
- Centrally provide tools and access for your security team 
- Set up Amazno SSO to provide access to AWS accounts and resources using your active directory 
- Apply service control policies (SCPs) to users, accounts or OUs to control access resources, services and Regions within your organization 
- Active AWS CloudTrail across accounts which creates a log of all activity in your cloud environment that cannot be turned off or modified by member accounts 

Migrating Accounts 
- Accounts can be migrated between organizations 
- You must have root or IAM access to both the member and management accounts 
- AWS console 
- AWS API/CLI 

Service Control Policies (SCPs)
- Manage permissions in your organization 
- Offers central control over maximum available permissions for all accounts 
- Must be explicitly enabled in an organization that has all features enabled 
- SCP is not desigend to grant permissions but to set limits 

