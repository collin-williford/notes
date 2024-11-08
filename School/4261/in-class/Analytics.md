Redshift 
- Fully managed data warehouse OLAP 
- RedShift is 10x faster than a traditional SQL DB 
	- Run complex analytic queries against petabytes of structured data 
- Uses EC2 
	- Vertical scaling: size of EC2 
	- Horizontal scaling: add nodes 
- Access through application, not EC2 directly 
	- Learner node: formulate and coordinate queries
	- Compute node: store data and compute 
- Redshift Spectrum 
	- Runs analytics over (unstructured data) stored in S3 instead of structured data stored in Redshift cluster 

Open Seach 
- AWS version of Elasticsearch 
- Visualization 

Kinesis 
- Collect, store and analyze real-time data
- Kinesis video stream 
	- Stream video for analysis 
	- Encryption with serverside KMS 
- Kinesis data stream 
	- Fast intake of data 
	- Real-time metrics 
	- Real-time analysis and processing 
- Kinesis firehose 
	- Capture real time data 
	- Destination 
		- S3 
		- Redshift 
		- Opensearch 
		- Splunk 

Athena 
- Interactive SQL query over data in S3 
- Serverless 
- Works with a variety of standard data formats, including CSV, JSON, ORC, Apache Parquet and Avro 

QuickSight
- Scalable, serverless, embeddable, machine learning-powered business intelligence (BI)
- Designed to provide fast, easy-to-use, and cost-effective analytics and data visualization solutions for businesses of all sizes 
- Integrated with Athena 

EMR 
- Utilizes Hadoop Map and Reduce 
- Distributed parallel processing petabyte-scale analysis 

Glue 
- Fully-managed, pay-as-you-go, extract, transform, and load (ETL) service that automates the time-consuming steps of data preparation for analytics 



