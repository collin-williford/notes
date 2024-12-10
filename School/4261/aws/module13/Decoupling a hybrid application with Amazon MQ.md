Amazon MQ
- Is a fully managed message broker service 
- Facilitates the setup, operation and management of an Apache ActiveMQ or RabbitMQ message broker in the AWS Cloud 
- Provides a queue and topic-based solution for loosely coupling applications 
- Enables software applications and components to communicate by using various programming languages, operating systems, and formal messaging protocols 

Amazon MQ use case: Hybrid cloud environment 
- Corporate data center 
	- Message producer 
- --> Message --> 
- AWS Cloud 
	- --> Amazon MQ broker 
		- --> 
			- Message consumer 
	- <--> Amazon EBS

Choosing the right solution for decoupling 
- Amazon SQS 
	- Applicability 
		- Cloud-centered applications 
	- Messaging model 
		- Producer-consumer 
	- Programming API 
		- Amazon SQS API 
	- Pricing Model 
		- Pay per request 
- Amazon SNS 
	- Applicability 
		- Cloud-native applications 
	- Messaging Model 
		- Publisher-Subscriber 
	- Programming API 
		- Amazon SNS API 
	- Pricing Model 
		- Pay per request 
- Amazon MQ 
	- Applicability 
		- Hybrid applications 
		- Message broker migration 
	- Messaging model 
		- Producer-Consumer 
		- Publisher-Subscriber 
	- Programming API 
		- Industry standard message broker APIs
	- Pricing Model 
		- Pay per hour 
		- Pay per GB 

Key takeaways:
- Amazon MQ is a managed service that you can use to set up and operate Apache ActiveMQ and RabbitMQ message brokers in the cloud
- Amazon MQ is compatible with open standard messaging APIs and protocols 
- You can use Amazon MQ to integrate on-premises and cloud environments in a loosely copuled manner 
- You can also use Amazon MQ to migrate your on-premises open source message brokers to the AWS Cloud 

