IAM 
- Global, not specific to a region, eventual consistency
- IAM elements
	- Principle
		- users, roles, federated users, applications. Services can assume roles 
	- Request
		- Console, CLI, SDK or API, 
		- Eg. CRUD, request context 
		- Eg. IP address, user agent, SSL status
	- Authenticated 
		- user login via console, API and CLI via access key and secret key 
	- Authorization 
		- Policies (in JSON), either user (identity based) or resource based
		- If a single policy has a deny action IAM denies the request and stops evaluating (explicit deny)
		- By default all requests are denied (implicit deny). An explicit allow overrides the implicit deny. An explicit deny overrides any explicit allows. Root ahs implicit access to all 
	- Action 
	- Resource 

Secure Token Service (STS)
- Obtain short term access credential 
	- Minutes to hours 
	- Works like access keys 
- Example scenario 
	- You have two AWS accounts: Account-A and Account-B. You want a user or an application in A to access resoruces in B, but you don't want to create and manage long-term IAM user credentials in B for this user/application 
		- Create an IAM role in B
		- Define a trust policy for this role that allows A to assume it 
		- The user/application in A calls the AssumeRole API operation of AWS STS 
		- AWS STS returns temporary security credentials (access key ID, secret access key, and a security key)
		- The user/application in A uses these temporary credentials to make requests to AWS resources in B
		- Once the credentials expire, they can no longer be used and a new request to AssumeRole needs to be made for continued access

Common use cases of STS
- Cross account access
- Federated user access (AD) 
	- User SAML 2.0
	- Single sign-on 
- Federation with OAUTH
	- E.g. Google, Facebook 

AWS Directory service 
- AWS Cognito 
	- Sign-up and sign-in functionality that scalues to millions of users and federated to public social media services 
	- Ex
		- Develop consumer apps or SaaS
- AWS directory service for Microsoft AD
	- AWS-managed full Microsoft AD running on Windows Server 2012 R2
	- Ex
		- Enterprises that want hosted Microsfot AD or you need LDAP for Linux apps 
- AD connector 
	- Allows on-premises users to log into AWS services with their existing AD credentials. Also allows EC2 instances to join AD domain 
	- Ex
		- Single sign-on for on-premises employees and for adding EC2 instances to the domain 
- Simple AD 
	- Low scale, lost cost AD implementation 
	- Ex
		- Simple user direcotry or you need LDAP compatibility 
- AWS Cloud Directory 
	- Cloud-native directory to share and control access to hierarchical data between applications 
	- Ex
		- Cloud applications that need hierarchical data with complex relationships 

Cognito 
- Allows sign up and sign-in 
	- AWS's version of google and facebook in term of identity provider
- Integrates with other web identity providers 
- User pool 
	- Registered users 
- Identity pool 
	- Grant access to AWS services via STS 

