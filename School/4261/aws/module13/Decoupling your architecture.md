Tight coupling in a three-tier architecture
- Web client 
	- All communication is synchronous (send or wait for a reply) 
- Web server on Amazon EC2 
	- The web server communicates directly with the app server 
- Application server on Amazon EC2
	- Challenge: Failure on the application server means a failure of the system 

Tight coupling increases the complexity of scaling 
- Web client 
- Route 53
- Web tier 
	- Web server instance 1
	- Web server instance 2
	- Web server instance 3
- Application tier 
	- Application server instance 1 
	- Application server instance 2
- Database tier 
	- Database on Amazon RDS instance 
- An application outage impacts all connected web servers 
- Each new server requires multiple connections that must be updated in code 

Loose coupling: Amazon MQ
- Corporate Data center 
	- Image producer application server
- AWS Cloud
	- Amazon MQ broker 
	- Amazon EFS
	- Transcoding consumer application server instance

Categories of soulutions for loose coupling 
- Loose coupling solves tight integration problems and can be achieved through both synchronous and asynchronous solutions 
- Synchronous
	- Infrastructure level 
		- ELB 
	- Application level 
		- Microservice architecture 
- Asynchronous 
	- Application level 
		- Microservice architecture 
	- Queue based 
		- Amazon SQS 
		- Amazon MQ
	- Topic based 
		- Amazon MQ 
		- Amazon SNS 

Key takeaways:
- Tightly coupled systems are difficult to scale and introduce bottlenecks and single points of failure 
- A loosely coupled architecture removes direct dependencies between related components and permits scalability and resiliency 
- Loose coupling solutions divide infrastructure layers or application functions and typically introduce an intermediary component between them 
- Loose coupling solutions can be synchronous or asynchronous 
	- ELB is an example of a synchronous solution 
	- Amazon SQS, Amazon SNS, and Amazon MQ are examples of an asynchronous solution 

