Database considerations
- Scalability 
	- How much throughput is needed?
	- Will it scale
- Storage requirements
	- Will the database need to be sized in gigabytes, terabytes, or petabytes of data?
- Data characteristics
	- What is your data model?
	- What are your data access patterns?
	- Do you need low latency?
- Durability 
	- What level of data durability, availability, and recoverability is required?
	- Do regulatory obligations apply?

Relational and non-relational databases 
- Structure
	- Relational 
		- Tabular form of columns and rows
	- Non-relational 
		- Variety of structure models (key-value pairs, document or graph-based)
- Schema 
	- relational
		- Strict schema rules 
	- non-relational
		- flexibility
- Benefits 
	- relational
		- Ease of use, data integrity, reduced data storage, and common language (SQL)
	- non-relational
		- Flexability, scalability and high performance 
- Use Case
	- relational
		- When migrating an on-premises relational workload or if your workload involves online trasactional processing 
	- non-relational
		- When a caching layer is needed to improve read performance, when storing JSON documents, or when a single digit milisecond data retrieval is needed
- Optimization 
	- relational
		- Optimized for structured data stored in tables; supports complex one-time queries through joins 

Amazon database options
- Relational databases
	- Amazon RDS
	- Managed database service that provides seven familiar database engines to choose from, including Amazon Aurora 
- non-relational databases
	-  Aamazon DynamoDB
	- Amazon Neptune 
	- Amazon ElastiCache
	- Variety of services designed for databases such as key-value, graph, and in-memory 

Less responsibility with managed AWS database services 
- Host database on premises
	- Power, HVAC, and network 
	- Rack and Stack 
	- Server Maintenace
	- OS Installation 
	- OS Patches
	- Database Installation 
	- Database Patches
	- Database Backups 
	- High Availabilty 
	- Scaling 
	- Appliication Optimization 
- Host Database in Amazon EC2
	- Database installation 
	- Database Patches 
	- Database Backups
	- High Availability 
	- Scaling 
	- Application Optimization 
- Host Database in a Managed AWS Database Services 
	- Application Optimization 

Database capacity planning 
- Designing with the end goal in mind 
	- 1. Analyze current storage capacity 
	- 2. Predict capacity requirements 
	- 3. Determine if horizontal scaling, vertical scaling, or a combination is needed 

Key takeaways
- When you choose a database, consider scalability, storage requirements, data characteristics, cost and durability requirements. Database capacity planning is also a consideration 
- Relational databases have strict schema rules, scale vertically, provide data integrity and work well for structed data stored in tables 
- Non-relational databases have flexible schemas, scale horizontally, provide higher scalabality and flexiblity, and work well for semi-structed and unstructed data 
- With AWS managed database services, you are responsible only for optimizing your application 


