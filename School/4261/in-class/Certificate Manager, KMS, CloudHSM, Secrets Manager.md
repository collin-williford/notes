Certificate Manager 
- Create, store and renew of TLS certificates 
- Single domain, multiple domains, wildcard characters 
- Integrated with services that need to use certificates 
	- Load balancer 
	- Web hosting 
	- CDN distribution 

Key Management Service (KMS)
- Managed service to enable encrypting customer data 
- Management services 
	- Key storage 
	- Auditing 
	- Encryption of data stored in other AWS services 
- KMS key 
	- KMS keys can never be exported 
		- CloudHSM allows export of keys 
	- Used by AWS services 
		- Lambda 
		- S3
		- EFS
		- EBS
		- SQS
	- Used by AWS services created it in the same region 
	- Both symmetric and asymmetric keys 
- Key requests are logged in CloudTrail for auditing 

Customer Managed KMS keys 
- KMS keys created by customers in your AWS account 
- Customer has full control (e.g.)
	- Maintaining key policies 
	- IAM policies to grant access 
	- Rotation 
	- Tags 

AWS CloudHSM
- Hardware Security Module 
	- Meet regulatory requirements to store encryption keys 
- Store and manage keys in tamper resistant hardware device 
- Customer manage keys 
	- Export keys 
	- Access control keys 
	- Use of keys 
- Manage CloudHSM
	- AWS CloudHSM API 
	- AWS CLI 

AWS Secrets Manager 
- Protects secrets needed to access applications 
	- Database credentials 
	- API keys
- Access secrets through Secrets Manager API 
- Built in secrets rotation with services 
	- RDS
	- Documentdb
	- Redshift 
- Extensible to other types of secrets 
- Fine grain permissions 
	- IAM 
- Secrets are encrypted at rest with KMS managed keys 
- Transmitted to your application using TLS 
- Does not cache secrets in persistent storage 
- Secrets accesses are log for auditing purposes 


