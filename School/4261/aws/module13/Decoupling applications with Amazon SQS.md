Point-to-point messaging 
- You can decouple applications asynchronously by using point-to-point messaging 
- Using point-to-point messaging when the sending application sends a message to only one specific receiving application 
- The sending application is called a producer 
- The receiving application is called a consumer
- Point-to-point messaging uses a message queue to decouple applications 

Amazon Simple Query Service (Amazon SQS) 
- Is a fully managed message queueing service 
- Helps integrate and decouple distributed software systems and application components 
- Provides highly available, secure and durable message-queueing capabilities
- Provides an AWS Management Console interface and a web services API 

Amazon SQS benefits 
- Fully managed 
	- Avoid the need to manage messaging software or maintain infrastructure 
- Reliability 
	- Deliver large volumes of data without losing messages
- Security 
	- Send sensitive data securely between applications 
- Scalability 
	- Scale elasticallly based on usage 

Amazon SQS basic components 
- Message 
	- A message can be up to 256 KB in size 
	- A message remains in the queue until it is explicitly deleted or exceedes the queue's message retention period
- Queue
	- Amazon SQS offers two types of queues: standard and first-in-first-out (FIFO)
	- You can configure queue parameters, including the following: 
		- Message retention period 
		- Visibility timeout 
		- Receive message wait time (short polling versus long polling)
- Dead-letter queue 
	- You can associate a dead-letter queue (DLQ) with any queue 
	- A DLQ stores messages that cannot be consumed successfully 

Decoupling example: Amazon SQS
- ALB 
	- Application tier 
- -> 
- Producer application tier 
	- Instance 1 
		- Order capture application 
	- Instance 2
		- Order captuer application 
	- Instance 3
		- Order capture application 
- -> 
- messages 
- Amazon SQS
	- Customer order queue 
		- -> Dead-letter queue 
- <- 
- messages
- Consumer application tier 
	- Instance 4
		- Order fulfillment application 
	- Instance 5 
		- Order fulfillment application 

Queue types 
- Standard queue 
	- messages (3, 2, 1)--> Standard queue --> messages (2, 3, 1, 3)
		- At-least-once delivery 
		- Best-efford ordering 
		- Nearly umlimited throughput
- FIFO queue
	- Messages (3, 2, 1) --> FIFO queue --> messages (3, 2, 1)
		- FIFO delivery 
		- Exactly once processing 
		- High throughput 

Queue configuration: Polling type 
- Choose the right polling type 
	- Short polling 
		- Receive message wait time = 0 
	- Long polling 
		- Receive message wait time > 0

Amazon SQS use cases
- Work queues
	- Decouple components of a distributed application that process the same amount of work at a different rate 
- Request offloading 
	- Queue resuts to move slow operations off of interactive request paths
- Buffering and batch operations 
	- Provide a buffer against traffic spikes or batch work for processing at a later time 
- Trigger Amazon EC2 Auto Scaling 
	- Use SQS queues to help determine the load on an application invoke scaling actions 

Key takeaways:
- Amazon SQS is a fully managed message-queuing service that you can use to decouple application components so that they run independently 
- Amazon SQS supports standard and FIFO queues 
- Messages that cannot be processed can be sent to a dead-letter queue 
- Long polling helps reduce the cost of using Amazon SQS by reducing the number of empty responses to a consumer's receve message request 
- A producer sends a message to a queue. A consumer processes and deletes the message during the visibility timeout period 