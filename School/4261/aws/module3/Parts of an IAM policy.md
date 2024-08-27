IAM policy document structure 
- Version 
	- Version of the policy language that you want to use 
- Statement 
	- Defines what is allowed or denied based on conditions 
- Effect 
	- Allow or deny 
- Principal 
	- For a resource-based policy, the account, user, role or federated user to allow or deny access to 
	- For an identity-based policy, the principal is implied as the user or role that the policy is attached to 
- Action 
	- Action is allowed or denied 
	- Example: "Action": "s3:GetObject"
- Resource 
	- Resource or resources that the action applies to 
	- Example: "Resource:" "arn:aws:sqs:us-west-2:12345678012:queue1"
	- (ARN = AWS resource name)
- Condition 
	- Conditions that must be met for the rule to apply 

Key takeaways:
- IAM policies are stored as JSON documents. Each statement includes information about a single permission 
- Key elements of an IAM policy statement include the effect, action and resources. Together, these elements determine policy permissions 