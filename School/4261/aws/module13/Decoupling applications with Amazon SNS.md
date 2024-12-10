- Publish/subscribe messaing
	- You can decouple applications asynchronously by using publish/subscript (pub/sub) messaging 
	- Use pub/sub messaging when the sending application sends a message to multiple receiving applications and has little or no knowledge about the receiving applications 
	- The sending application is called publisher 
	- The receiving application is called a subscriber 
	- Pub/sub messaging uses a topic to decouple applications 

Amazon Simple Notification Service (Amazon SNS)
- Is a fully managed pub/sub messaging service 
- Helps decouple applications through notifications 
- Provides highly scalable, secure, and cost-effective notification capabilities 
- Provides an AWS Management Console interface and a web services API 

Types of subscribers 
- Email destination 
- Mobile text messaging destination 
- Mobile push notifications endpoint 
- HTTP or HTTPS endpoint 
- AWS Lambda function
- SQS queue 
- Amazon Kinesis Data Firehouse delivery system 

Amazon SNS use cases 
- Application and system alert notification 
- Email and text message notification 
- Mobile push notification 

Decoupling example: Using Amazon SQS with Amazon SNS 
- 1
	- Mobile client
		- Image upload
- 2
	- S3 bucket for uploaded images 
		- Event notification 
- 3
	- Image uploaded notification topic 
- 4
	- Generate thumbnail
	- Size for mobile queue
	- Size for web queue 
- 5
	- Thumbnail application 
		- Auto Scaling group 
	- Mobile sizing application 
		- Auto Scaling group 
	- Web sizing application 
		- Auto Scaling group 
- 6
	- S3 bucket for converting images 

Amazon SNS considerations 
- Message publishing 
	- Single published message 
	- No recall options 
- Message delivery 
	- User a *standard* topic if the message delivery order does not matter
	- Use a FIFO topic if an exact message delivery order is required 
	- Customize the delivery policy of an HTTP or HTTPS endpoint to control the retry behavior 

Amazon SNS and Amazon SQS comparion 
- Amazon SNS
	- Messaging model 
		- Publisher-Subscriber 
	- Distribution Model 
		- One to Many 
	- Delivery Mechanism 
		- Push (passive)
	- Message Persistence 
		- No 
- Amazon SQS 
	- Messaging Model 
		- Producer-Consumer 
	- Distribution Model 
		- One to one 
	- Delivery Mechanism 
		- Pull (active)
	- Message Persistance 
		- Yes 

Key takeaways:
- Amazon SNS is a web service that you can use to set up, operate, and send notificaitons from the cloud
- Amazon SNS follows the pub/sub messaging paradigm 
- To use Amazon SNS, you create a topic, create subscribers for the topic, and publish messages to the topic 
- You can use topics to decopule message publishers from subscribers and fanout messages to multiple recipients at one time 
- AWS services can publish messages to an SNS topic to invoke event-driven computing and workflows 

