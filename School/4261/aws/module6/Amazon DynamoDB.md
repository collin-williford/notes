DynamoDB
- Is a fully managed, serverless, NoSQL database
- Supports key-value and document data models 
- Delivers millisecond performance and can automatically scale tables to adjust for capacity 
- Is used for developing applications, mission-critical workloads that prioritize speed, scalability and data durability 

DynamoDB use cases
- Develop software applications
	- Build internet-scale applications that support user-content metadata and caches that require high concurrency 
- Create media metadata stores
	- Scale throughput and concurrency for media and entertainment workloads, such as real-time video streaming and interactive content 
- Scale gaming platforms 
	- Build out your game platform with player data, session history, and leaderboards for millions of concurrent users 

DynamoDB Features
- Serverless performance with limitless scalability 
	- Secondary indexes provide flexibility on how to access your data
	- Amazon DynamoDB Streams is ideal for an event-driven architecture
	- Multi-Region, multi-active data replication with global tables 
- Built-in security and relability 
	- DynamoDB encrypts all customer data at rest by default 
	- Point-in-time recovery protects data from accidental operations 
	- DynamoDB allows fine-grained access control 

Amazon DynamoDB data structure 
- DynamoDB table 
	- DynamoDB table item 
		- table attributes 
			- Partition key
				- A composite primary key is composed of the partition key and the sort key 
				- A simple primary key is composed of one attribute known as the partition key 
			- Sort key 
			- Attribute list 
				- There can be zero or more additional attributes in an item 

Mult-region replication: Amazon DynamoDB global tables 
- Global tables provide a multi-region, multi-active database for fast local read and write performance for global applications

DynamoDB security best practices 
- Preventative 
	- Use IAM roles to authenticate access
	- Use IAM policies for DynamoDB base authorization 
	- Use IAM policy conditions for fine-grained access control
	- Ues a VPC endpoint and policies to access DynamoDB
- Detective
	- Use AWS CloudTrail to monitor AWS managed AWS KMS key usage 
	- Monitor DynamoDB operations by using CloudTrail
	- Monitor DynamoDB configuration with AWS Config
	- Monitor DynamoDB compliance with AWS Config rules 

Key Takeaways:
- DynamoDB is a fully managed, serverless, NoSQL database that supports key-value and document data models 
- DynamoDB offers global and local secondary indexes to provide flexibility on how to access your data 
- Global tables provide a multi-Region, multi-active database for fast performance for global applications
- DynamoDB encrypts all user data at rest stored in tables, indexes, and streams. Preventative and detective security best practices help ensure data protection 

