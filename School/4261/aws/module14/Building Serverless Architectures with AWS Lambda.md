AWS Lambda 
- AWS Lambda lets you run code functions without provisioning or managing servers
- Lambda functions are configurable with runtime language, amount of memory, and timeout duration
- A function has a maximum duration of 15 minutes 
- Functions can be deployed as .zip files or container images 

Identifying Lambda serverless scenarios
- Synchronous processing 
	- Web apps
	- Web services 
	- Microservices 
	- Machine learning inferences 
- Asynchronous processing 
	- Scheduled events
	- Queued messages 
	- Image or video transformation
	- AWS service triggers 
- Streaming processing 
	- Streaming application 

Invoking a synchronous Lambda Function 
- External API request using API Gateway 
	- Browser Client <--> Amazon API Gateway  <--> AWS Lambda <--> AWS Lambda <--> AWS Service 
- External API request using Lambda function URL 
	- Browser client <--> AWS Lambda Service <--> AWS Lambda function <--> AWS service 

Lambda event source mappings for queues and streams 
- Amazon DynamoDB stream <--> AWS Lambda service --> Amazon SQS error queue 

Key takeaways:
- AWS Lambda is a service to run code functions without provisioning or managing servers
- A Lambda function can run inside a VPC owned by the AWS Lambda service or as Lambda@Edge in an Amazon CloudFront regional cache
- A Lambda function can be configured to connect to your VPC to access AWS services inside the VPC 
- A Lambda function can be invoked synchronously, asynchronously, and with event source mappings for queues and streams 
- Use Lambda layers to package code dependencies or custom runtimes to be re-used by all Lambda functions in the Region 

