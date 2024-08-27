IAM policies and permissions 
- Use policies to fine-tune the permissions that are granted to principals 
	- Two types of policies
		- Identity-based
			- Attach to an IAM user, group or role 
		- Resource-based
			- Attach to an AWS resource
- Define permissions in IAM policy documents 
	- The document is formatted in JSON 
	- The policy defines which resources and operations are allowed or denied 
	- Follow the principle of least privilege 
- The biggest difference is where they are applied 

Determining permissions at the time of request 
- When IAM determines whether an action is allowed, the service first checks for the existence of any applicable explicit denial policy. If an explicit denial doesn't exist, then IAM checks for any applicable explicit allow policy doesn't exist, IAM reverts to the default and denies access. This process is referred to as implicit deny. A user will be permitted to take the action only if the requested action is not explicitly denied and is explicitly allowed. 

Identity-based and resource-based policies
- Identity-based policies are attached to an IAM user, group or role. They indicate what that idnetity can do. 
	- For example, you could grant a user the ability to access a DynamoDB table 
- Resource-based policies are attached to a resource. They indicate what a specified user (or a group of users) is permitted to do with the resource. For example, you could use a resource-based policy to grant access to an S3 bucket or to grant cross-account access between two trusted AWS accounts 

Policies
- Example 1
	- An IAM user, Bob has an identity-based policy attached. The policy allows him to use the GET, PUT and LIST APIs for S3 bucket X. However, the resource-based policy for bucket X allows him to use GET and LIST, but denies the ability to use PUT. This means bob cannot PUT objects into bucket X, even though his identity-based policy allows it 
- Example 2:
	- Bob's identity-based policy allows the LIST action. The policy doesn't explicitly allow or deny the GET and PUT actions on bucket Y. The resource-based policy for bucket Y allows Bob to use GET and LIST, but doesn't specify the PUT action. Therefore, bob can read objects from the bucket, even though his identity-based policy doesn't explicitly allow it. 

Key takeaways:
- A policy defines permissions for the identity or resource that it's associated with 
- IAM provides two types of policies:
	- identity-based, which is attached to an IAM principal 
	- resource-based, which is attached to an AWS resource 
- Permissions in policies determine whether a request is allowed or denied 
- By default, all requests are denied. An explicit allow overrides the default deny; an explicit deny overrides any explicit allow 