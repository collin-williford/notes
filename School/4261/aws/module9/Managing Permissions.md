Challenge of managing permissions 
- Assigning permissions directly to users is difficult to manage 
	- Initial configuration 
		- Each developer is given full access to Amazon Elastic Compute Cloud (Amazon EC2) through policies that are attached to individual users 
	- Additional access is needed
		- Each developer need access to Amazon Simple Storage Service (Amazon S3). To implement this change, an administrator needs to make three modifications, one for each AWS Identity and Access Management (IAM) user's policy 
	- The number of developers grows
		- This approach becomes hard to manage. Is there an easier way to manage multiple permissions and users?

Use IAM groups to attach permissions to multiple users
- Permissions in a group can be based on a job function 
- All users in the group inherit the permissions assigned to the group 

The Characteristics of an IAM group 
- You can add users to a group or remove them from a group 
- A user can belong to multiple groups 
- Groups cannot belong to other groups 
- Groups can be granted permissions by using access control policies
- groups do not have sercurity credentials and cannot access web services directly. They exist soley to make it easier to manage user permissions 

Example: Using IAM groups to reflect job role 
- If a new developer, Pat is hired, add them to the developers group. Pat will immediately inherit the same access that's granted to other developers
- If Ana takes on a new role of developer, do the following
	- Remove her from the test group 
	- Add her to the developers group
- Users can belong to more than one group, but groups cannot be nested
- Permissions in policies directly attached to a user (user policies) override permissions in group policies if they are more restrictive 

Challanges of scaling with role-based access control (RBAC)
- To setup RBAC with IAM, do the following
	- Create an IAM policy with the permissions for the job role. The policy lists the individual resources to be accessed 
	- Attach the policy to an IAM entity (user, group or role)
- To update policies when access to a new resource is needed, do the following:
	- Update the policy 
	- Modify multiple policies if the new resource is used by multiple roles or add access to multiple resources 

Using attribute-based access control (ABAC)
- ABAC
	- This authorization strategy defines permissions based on attributes 
	- Attributes are a key or a key-value pair
	- In AWS, these attributes are called tags
	- Tags can apply to IAM resources (users or roles) and AWS resources 
- Benefits 
	- It's more flexible than policies that require you to list each individual resource 
	- Grandular permissions are possible without a permissions update for every new user or resource 
	- It's a highly scalable approach to access control 
	- It's fully auditable 

Tagging in AWS 
- Tags are resource metadata consisting of key/value pair
- Tags can apply to resources across AWS accounts and IAM users or roles 
- Customers can create user-defined tags 
- Many different AWS API operations return tag keys and values 
- Tags have multiple practical uses like biling, filtered views, and access control 

Key Takeways:
- Use IAM groups to grand the same access rights to multiple users. Create groups that reflect job functions 
- Use ABAC rather than RBAC to scale permissions management 
- ABAC is an authorization strategy that defines permissions based on attributes. It simplifies access control management by combining permissions into a single policy 
- Attributes are key value pairs. AWS enables customers to assign attributes to their AWS resources and identities in the form of tags 

