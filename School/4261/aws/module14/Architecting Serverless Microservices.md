Characteristics of a microservice 
- Autonomous 
	- Can be developed and deployed without affecting other microservices 
	- Scales independently 
	- Does not share code with other microservices 
	- Communicates over well-defined APIs
- Specialized 
	- Performs a single business function solving a specific problem 
	- Is owned by a small development team that chooses development tools 
	- Is stateless
	- Has its own data store 

Example: Breaking a monolithic application into microservices 
- Monolithic application 
	- Users, Topics, Messages
- Microservice application 
	- User service 
	- Topic Service
	- Message service 

Benefits of Microservices 
- Team agility 
- Reusable code 
- Flexible scaling 
- Technological freedom 
- Resilience 
- Simplified deployment 

Microservices serverless patterns on AWS 
- RESTful APIs
	- Amazon API Gateway <--> AWS Lambda <--> Serverless data store 
- Containers
	- Amazon API Gateway <--> Application Load Balancer <--> AWS Fargate <--> Serverless data store 
- Streaming 
	- Amazon Kinesis <--> AWS Lambda <--> Serverless data store 

Key takeaways:
- Microservice applications are composed of autonomous, specialized services 
- Microservices can form part of a three-tier architecture operating in the app and data tiers 

