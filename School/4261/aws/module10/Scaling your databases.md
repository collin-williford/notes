Scaling AWS databases 
- Aurora 
	- Scale a cluster 
		- Vertical scaling with instance types 
		- Horizontal scalign with read replicas 
		- Service managed storage scaling 
- Amazon Aurora Serverless
	- Scale a cluster 
		- Horizontal compute scaling with Aurora Compute Units (ACUs)
		- Service managed storage scaling 
- Amazon RDS 
	- Scale a database 
		- Vertical scaling with instance types and storage volume size and type 
		- Horizontal scaling with read replicas 
- DynamoDB
	- Horizontal scaling to scale read capacity units (RCUs) and write capacity units (WCUs) separately 
	- Serivce managed storage scaling 

Key Takeaways:
- With Aurora, you can choose the database instance class size and number of Aurora Replicas 
- Aurora Serverless scales resources automatically based on the minimum and maximum capcity specifications 
- You can manually vertically scale compute capacity for your RDS DB instance 
- You can use read replicas to horizontally scale your RDS DB instance 
- DynamoDB On-Demand offers pricing model based on actual table reads and writes 
- DynamoDB auto scaling uses Application Auto Scaling to dynamically adjust provisioned throughput capcity 