IAM 
- Global, not specific to a region, eventual consistency 
- IAM elements 
	- Principal 
		- Users
		- Roles 
		- Federated users
		-  applications 
		- services can assume roles 
	- Request
		- Console, 
		- CLI
		- SDK
		- API
	- Authenticated 
		- User login via console
		- API and CLI via access key and secret key 
	- Authorization 
		- Policies (in JSON), either user (identity based) or resource based 
		- If a single policy has a deny action IAM denies the request and stops evaulating (explicit deny)
		- By default all requests are denied (implicit deny). An explicit allow overrides the implicity deny. An explicit deny overrides any explicit allows. Root has implicit access to all 
	- Action 
	- Resource 

Secure Token Service (STS)
- Obtain short term access credential 
	- Minutes to hours 
	- Works like access keys 
- Common use cases 
	- Cross account access 
	- Federated user access (AD)
		- User SAML 2.0
		- Single sign-on 
	- Federated with OAUTH
		- E.g. Google, Facebook 

Cognito 
- Allows sign up and sign-in (AWS's version of google and facebook in terms of identity provider)
- Integrates with other web identity providers 
- User pool 
	- Registered users 
- Identity pool 
	- Grant access to AWS services via STS 

