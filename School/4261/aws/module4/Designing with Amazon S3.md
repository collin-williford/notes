Amazon S3 default security configurations 
- S3 buckets and objects created are private and protected by default 
- S3 buckets have encryption configured by default
- Server-side encryption with Amazon S3 managed keys (SSE-S3) is the default encryption 
When use cases must share Amazon S3 data, do the following 
- Manage and control the data access 
- Follow the prinviple of least privilege 

Encrypting objects in Amazon S3
- Encryption encodes data with a secret key, which makes it unreadable without a key 
	- Server-side encryption 
		- Amazon S3 encrypts objects before it saves the objects to disk and decrypts the objects when you download them 
		- Enable this feature by selecting the default encryption option on the bucket 
	- Client-side encryption 
		- Encrypt data on the client side and upload the encrypted data to Amazon S3 
		- In this case, you manage the encryption process 

Amazon S3 tools for protecting buckets and objects 
- Block public Access feature 
	- Makes buckets inaccessible to the public 
- AWS Identity and Access Management (IAM) policies
	- Authenticates users by using IAM 
- Bucket policies 
	- Defines access based on specific written rules 
- Access control lists (ACLs) 
	- Sets rules for access to buckets and objects (bucket policies are the preferred method for controlling bucket access)
- Amazon S3 access points 
	- Configures access with names and permissions specific to each application 
- Preassigned URLs
	- Grants time-limited access to others with temporary URLs 
- AWS Trusted Advisor 
	- Provides a bucket permission check 

Three general approaches to configuring access 
- Option 1
	- By default all S3 buckets and the objects stored in them are private (protected). The only entities wiht access to a newly created, unmodified bucket are the account administrator and the AWS account root user. The resource owner can grant specific access permissions to others, but anyone without those permissions will not have access 
- Option 2
	- A case where Amazon S3 was configured to provide controlled access. user A was granted access to the objects in the bucket, but User B was denied access. Controlled access scenarios are common. THe bucket owner can configure these scenarios by using one or more of the tools or options for controlling access to Amazon S3 data discussed earlier 
- Option 3
	- An occasion where S3 security settings have been disabled and anyone can publicly access the objects stored in the bucket 

Considerations for choosing a Region 
- Data privacy laws and regulatory compliance 
	- Are there relevant Region data privacy laws?
	- Can customer data be stored outside the country?
	- Can you meet your governance obligation?
- Proximity of users to data
	- Small differences in latency can impact customer experience 
	- Choose the Region closest to your users
- Availability service and feature 
	- Not all AWS services are available in all Regions 
	- Services expand to new Regions regularly 
	- Use some services cross-Region but at increased latency 
- Cost-effectiveness
	- Costs vary by Region 
	- Some services such as Amazon S3 have costs for transferring data out 
	- Consider the cost-effectiveness of replicating the entire enviroment in another Region 

Amazon S3 Inventory 
- Use Amazon S3 Inventory to help manage your storage 
- Use it to audit and report on the replication and encryption status of your objects for business, compliance and regulatory needs 
- Speed up business workflows and big data jobs by using Amazon S3 inventory 
- Provide a scheduled alternative to the Amazon S3 synchronous List API operations 

Amazon S3 costs
- Pay for only what you use 
	- Gigabytes of objects stored (per month) with different pricing for each Region and each Storage class 
	- PUT, COPY, POST, LIST or lifecycle transition to move data into any Amazon S3 storage class
- No charge for data transferred 
	- Out the internet for the first 100 GB per month 
	- In from the internet 
	- Between S3 buckets or to any service in the same AWS Region 
	- From an S3 bucket to any AWS service or services within the same AWS Region as the S3 bucket 
	- Out to CloudFront 

Key takeaways 
- S3 buckets are private and can be accessed only by users who are explicitly granted access 
- SSE-S3 is the default encryption configuration for every bucket in Amazon S3 
- Considerations when choosing a Region include data privacy laws and regulatory compliance, proximity of users to data, availability service and features, and cost-effectiveness 
- Amazon costs are based on your object's size, the amount of time you stored the objects during teh month, and the storage class 