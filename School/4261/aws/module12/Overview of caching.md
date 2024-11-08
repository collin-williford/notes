Why cache content?
- A cache is a high-speed data storage layer that stores a subset of data so that future requests for that data are served up faster 
	- Store regularly accessed data in a more optimized way 
	- Increase data retrieval performance
	- Reduce the need to access the underlying slower storage layer

Why should you cache?
- Static and frequently accessed data 
- Results of computationally intensive calculations 
- Results of time-consuming, frequently used or complex database queries 

Trade-offs to consider when caching 
- Benefits of caching 
	- Reduces reponse latency 
	- Reduces cost 
	- Alleviates the load on the origin (data source)
	- Provides predictable performance 
	- Improves availability 
- Challenges of caching 
	- Requires additional engineering 
	- Requires someone to determine how cache data and deal wiht stale data based on the business use case 

Types of caching and AWS caching services 
- Amazon CloudFront 
	- Static caching (edge caching)
		- Retrieve content from the nearest edge location 
- Amazon ElastiCache
	- Database caching (data caching)
		- Retrieve content from an in-memory database layer 

Key takeaways:
- A cache is a high-speed data storage layer that stores a subset of data so that future requests for that data are served up faster
- Static and frequently accessed data are good candidates for caching 
- Caching improves application speed and decreases database cost 
- Content is retrieved from the nearest edge location with static caching and retrieved from an in-memory database layer with database caching 

