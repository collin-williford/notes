Identity federation 
- A system of trust between two parties to authenticate users and convey information that's needed to authorize access to resources 
	- Identity provider (IdP) is responsible for user authentication 
	- Examples:
		- OpenID connect (OIDC) IdPs like Login with Amazon, Facebook, and Google 
		- Security Assertion Markup Language (SAML) IdPs like Shibboleth or Active Directory Federation Services 
	- Service provider (SP) is responsible for controlling access to its resources
	- Examples
		- AWS services 
		- Social media platforms 
		- Online bank 

AWS services that support identity federation 
- AWS Identity and Access Management (IAM)
- AWS IAM Identity Center (successor to AWS Single Sign-On)
- AWS Security Token Service (AWS STS)
- Amazon Cognito 

AWS IAM Identity Center
- Successor to AWS Single Sign-On
- Can create or connect identities once and manage access centrally across your AWS accounts 
- Provides a unified administration experience to define, customize, and assign fine-grained access 
- Provides a user portal to access all assigned AWS accounts or cloud applications 
- Use optionally in conjunction with IAM 

AWS Security Token Service (AWS STS)
- AWS STS is a web service (API) that enables you to request temporary, limited-privilege credentials 
- The credentials can be used by IAM users, federated users, or applications 

Identity federation to AWS with an identity broker
- User signs in wiht existing credentials for their IdP
	- Users sign in using an identity that is already known by an IdP (for example their Amazon.com ID or a corporate login)
- Identity broker acts as an intermediary between IdP and SP
	- The identity broker requests temporary credentials from AWS STS
- AWS STS generates temporary credentials dynamically 
	- The credentials last from a few minutes to several hours and are not recognized afer the credentials expire 
- Identity broker passes temporary credentials to application 
	- AWS STS returns the temporary credentials to the identity broker 
	- The identity broker passes them to the application for the user 

Amazon Cognito 
- A fully managed service that provides the following services and features 
	- Authentication, authorization and user management for web and mobile applications 
	- Federated identities for sign in with social identity providers (Amazon, Facebook, Google) or with SAML
	- User pools that maintain a directory with user profiles authentication tokens 
	- Identities and permissions assignment for users 

Amazon Cognito user pools features 
- Sign-up
	- Let users enter their information in your app and create a user profile that's native to your user pool.
	- Redirect users to a third-party IdP that they can authorize to pass their information to Amazon Cognito 
	- Create users based on a data source or schema 
- Sign-in
	- Use as a standalone user directory and IdP to your app 
- Federate third-part identities 
	- Let the user pool manage the overhead of handling the tokens that are returned from social sign-in through Facebook, Google, Amazon, and Apple, and from OIDC and SAML IdPs
- Hosted UI for sign-up and sign-in 
	- Present users with customized Amazon Cognito hosted web pages for sign-up, sign-in, multi-factor authentication (MFA), and password reset 
- Support for JWTs
	- Use JWT tokens to access server-side resources or exchange them for temporary AWS credentials to access other AWS services. JWT is an open standard that defines a compact, self-contained way to securely transmit information between parties as a JSON object 
- User pool groups 
	- Use groups to create collections of users to manage their permissions or to represent different types of users. For example, create seperate groups for users who are readers, contributors and editors of your website and app 

Key Takeaways:
- Identity federation is a system of trust between IdPs and SPs
- AWS IAM Identity Center provides a unified administration experience to define, customize and assign fine-grained permissions based on common job functions 
- AWS STS is a web service that provides temporary AWS credentials and allows an IAM user, federated user, or application to assume an IAM role 
- An Identiy broker facilitates federation when users already have identies outside of AWS, such as a corporate directory 
- Amazon Cognito is a fully managed service that provides authentication, authorization and user management for web and mobile applications. Users can sign in directory or thorugh a third party, such as Facebook, Amazon or Google 

