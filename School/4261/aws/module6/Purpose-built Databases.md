The evolution of purpose-build databases
- Improve on hierarchical databases' limited abilities to define relationships among data
	- Database evoltuion
		- Relational
	- AWS Example 
		- Amazon RDS
- Improve performance by separating read-heavy reporting from an application's transactional database
	- Database Evolution 
		- Data warehouse/OLAP
	- AWS ex
		- Amazon Redshift
- Analyze the more varied types of data being generated in large amounts on the internet 
	- Database Evolution 
		- Non-relational
	- AWS ex
		- DynamoDB
- Take advantage of cloud computing's freedom to scale data stores up and down based on actual usage, and the east of connecting different microservices to purpose-built stores 
	- Database Evolution 
		- Purpose-built:
			- Document 
			- Wide-column
			- In-memory 
			- Graph 
			- Timeseries
			- Ledger
	- AWS ex
		- Fully managed database services:
			- Amazon DocumentDB
			- Amazon Keyspaces
			- MemoryDB
			- Neptune
			- Timestream
			- Amazon QLDB

Amazon Redshift
- Is a fully managed, cloud-based data warehousing service designed to handel petabyte-scale analytics workloads
- Achieves optimum query performanc ewith columnar storage 
- Has an Amazon Redshift Serverless option 
- Is used for online analytics processing (OLAP)
  
AWS fully managed purpose-build database options
- Amazon DocumentDB
	- Document database
- Amazon Neptune
	- Graph database
- Amazon keyspaces 
	- Cassandra workloads
- Amazon MemoryDB for Redis
	- In-memory workloads
- Amazon Timestream
	- Timeseries database
- Amazon Quantum Ledger Database (Amazon QLDB) 
	- Ledger database 

Matching a database to your business need 
- Sutiable workloads 
	- Analyze your workload requirements to see if they match the database capabilities 
- Data model 
	- Understand the characteristics of the data model that you would need to use with the database 
- Features and benefits 
	- Familiarize yourself with key features and configuration options to optimize performance
- Common use cases
	- Review common use cases to find reference architectures and examples 

Amazon DocumentDB
- Suitable workloads
	- Require a flexible schema for fast, iterative development 
	- Need to store data that has different attributes and data values 
- Data model 
	- Uses a document data model 
	- Stores and quickly accesses documents
	- Queries on any attribute
- Features and benefits 
	- Is a MongoDB-compatible, JSON document database 
	- Is good complex documents that are dynamic and require one-time querying, indexing and aggregations 
- Common use cases
	- Content management system (CMS)
	- Customer profiles 
	- Store and management of operational data from any source 

Amazon Keyspaces
- Suitable workloads
	- Fast querying capacity of high volumes of data 
	- Scalability and consistent performance on heavy write loads
- Data model 
	- Is a wide column data model 
	- Stores data in flexible columns, which permits data to evolve over time 
	- Partitions across distributed database systems 
- Features and benefits 
	- Scalable, highly availablea nd managed Apache-Cassandra-compatible database service 
- Common Use cases
	- Process data at high speeds for applications that requrie milliseocnd latency 
		- Industral equipment maintance 
		- Trade monitoring 
		- Route optimization 

MemoryDB
- Sutiable workloads
	- Latency-sensitive workloads 
	- High request rate 
	- High data throughput 
	- No data loss 
- Data model 
	- Is an in-memory database service 
	- Relies primarily on memory for data storage 
	- Minimizes response time by eliminating the need to access disks 
- Featues and benefits 
	- Stores an entire dataset in memory and leaverages a distributed transactional log to provide the following:
		- In-memory speed and consistency 
		- Data durability and recoverability 
- Common use cases
	- Caching 
	- Game leaderboards
	- Bank user transactions 

Neptune 
- Suitable workloads 
	- Find connections or paths in data 
	- Combine data with complex relationships across data silos 
	- Navigate highly connected datasets, and filter results based on certain variables 
- Data model 
	- Is a graph data model 
	- Stores data and the relationship of that data to other data as equally important to the data itself 
	- Quickly creates and navigates relationships between data 
- Features and benefits 
	- Supports graph applications that require high thorughput and low latency graph queries 
	- Creates and navigates data relations quickly 
- Common use cases
	- Recommendation engines 
	- Fraud detection 
	- Knowledge graphs 
	- Drug discovery 
	- Social networking 

Timestream 
- Suitable workloads 
	- Identify patterns and trends over time 
	- Determine value or performance over time 
	- Rely on efficient data processing and analytics 
	- Require ease of data management 
- Data model 
	- Is a timeseries of data model 
	- Is a sequence of data points recorded over a time interval for measuring events that change over time 
	- Provides the ability to collect, store, and process data sequenced by time 
- Features and benefits 
	- Simplifies timeseries data access 
	- Has built-in timeseries functions for quick analysis of timeseries data by using SQL 
- Common use cases
	- Identify trends from data generated by Internet of Things (IoT) applicaitons 
	- Improve performance by analyzing web traffic data for your applications in real time 

Amazon QLDB
- Suitable workloads 
	- Maintain an accurate history of application data 
	- Track the history of financial transactions 
	- Verify the data lineage of claims 
- Data model 
	- Is a ledger database 
	- Provides an immutable and verifiable history of all changes to application data 
- Features and benefits 
	- Provides a transparent immutable, and cryptographically verifiable transaction log 
	- Provides built-in data integrity 
	- Provides a consistent event store 
- Common use cases 
	- Storing financial transactions 
	- Maintaining claim history

Key takeaways 
- Amazon Redshift is a cloud-based data warehousing service 
- Amazon DocumentDB is a MongoDB-comptiable, JSON document database 
- Amazon Keyspaces is a wide-column database service that is compatible with Apache Cassandra 
- MemoryDB is a durable in-memory database service 
- Neptune is a high-performance graph database engine 
- Timestream is a purpose-build database for timeseries data 
- Amazon QLDB is a ledger database that maintaines a verifiable log of data changes 