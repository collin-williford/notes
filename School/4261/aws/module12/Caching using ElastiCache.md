When should you cache your database
- You are concered about response times for your customer 
- You have high volume of requests that are overburdening your database 
- You want to reduce your database costs 

ElastiCache
- Is a fully managed, key-value, in-memory data store with sub-millisecond latency 
- Sits between an application and on origin data store 
- Decreases access latency and eases the load of databases and applications 
- Provides a high performance and cost-effective in-memory cache 
- Is fully compatible with open source Redis and Memcached engines 

Choose an ElastiCache engine based on what you need
- If you need choose ElastiCache for Memcached
	- The most basic model 
	- The ability to run large nodes with multiple cores or threads 
	- the ability to scale horizontally with Auto Discovery 
- If you need choose ElastiCache for Redis 
	- to support complex data types 
	- to provide persistence of your key store 
	- to sort or rank in-memory datasets 
	- to provide high availability with automatic failover 
	- to support publish/subscribe messaging 

ElastiCache components
- A node is the smallest block of an ElastiCache deployment 
- An ElastiCache cluster is a logical grouping of one or more nodes 
- With the Memcached engine, data is partitioned across up to 20 nodes in a cluster. With the Redis engine, you can scale up to 250 nodes 

Time to Live (TTL)
- A TTL value is added to each write 
- The TTL specifies the nubmer of seconds or miliseconds until the key expires 
- After the TTL expires, the application queries the database for data 

Strategies for handling stale data 
- Lazy Loading 
	- This strategy updates teh cache after the data is requested 
	- The cahe contains only data that the application actually requests 
	- This strategy requires a programmatic strategy to handle keeping the cache as up to date 
- Write-Through 
	- This strategy updates the cache immediately after updating the primary database
	- The cache is up-to-date with the primary database (most likely data will be found in the cache)
	- This strategy results in an incrase in cost from storing data in-memory that you might not use 

Caching strategies
- Lazy Loading 
	- user appliation 
	- Data request 
	- Cache Node 
	- Requested data in the cache?
		- if no -> cache miss 
			- Reduced load on primary database 
			- Data copied to the cache for future requests 
		- If yes -> cache hit 
			- Lower latency response to the requester 
- Write-through 
	- User application 
	- Writes to database
	- updates the cache 

Key takeaways:
- ElastiCache is a key-value, in-memory data store with the purpose of providing millisecond latency and inexpensive access to copies of data 
- ElastiCache reduces the complexity of administering your caching systems for Redis and Memcached engines 
- Lazy loading and write-through are two stragies to handle keeping the cache as up to date as is appropriate 

