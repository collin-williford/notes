Web app three-tier design in a VPC 
- VPC 
	- Web Tier
		- Web tier subnet 1
			- Web EC2 instances
		- Web tier subnet 2
			- Web EC2 instances
	- App tier
		- AZ1
			- App tier subnet 1 
				- App EC2 instances
		- AZ2
			- App tier subnet 2
				- App EC2 instances 
	- Data tier 
		- Data tier subnet 1 
			- Amazon RDS Multi-AZ primary database 
		- Data tier subnet 2
			- Amazon RDS Multi-AZ secondary database 

Benefits of AWS serverless 
- No server management 
- Pay-for-value services 
- Continuous scaling 
- Built-in high availability 
- Suitable for event-driven and microservice architectures 

AWS serverless services 
- Compute 
	- AWS Lambda and Lambda@Edge 
	- AWS Fargate 
- Authentication 
	- Amazon Cognito 
- Web hosting 
	- AWS Amplify 
- Content Delivery 
	- Amazon CloudFront 
- Application Integration 
	- Amazon API Gateway 
	- AWS AppSync 
	- Amazon Simple Notification Service (Amazon SNS)
	- Amazon Simple Queue Service (Amazon SQS)
	- Amazon EventBridge 
	- AWS Step Functions
- Data stores 
	- Amazon S3
	- Amazon Elastic File System (Amazon EFS)
	- Amazon DynamoDB
	- Amazon Neptune Serverless
	- Amazon Aurora Serverless
	- Amazon Redshift Serverless
	- Amazon OpenSearch Serverless

Key takeaways:
- AWS serverless services provide you the following benefits:
	- No server management 
	- Pay-for-value services 
	- Continuous scaling 
	- Built-in fault tolerance 
- Serverless services are suitable for event-driven and microservice architectures 

