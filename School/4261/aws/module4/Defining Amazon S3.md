Types of storage 
- Block storage 
	- Data is stored on a device in fixed-sized blocks 
- File storage 
	- Data is stored in a hierarchical storage 
- Object storage 
	- Data is stored as objects based on attributes and metadata 

Amazon S3
- Amazon S3 stores massive (unlimited) amounts of unstructured data
- Amazon S3 stores data files as objects in a bucket that you define 
- Five TB is the maximum file size of a single object 
- Objects have a globally unique URL 
- Objects have a key, version ID, value, metadata, and sub-resources

Amazon S3 components 
- Bucket 
	- A bucket is a container for objects
		- Each bucket has a unique name and a region-specific endpoint in this format 
			- https//s3-<\aws-region>.amazonaws.com/<\bucket-name>/<\object-key>
- Object 
	- An object is a file and the metadata that describes that file.
	- Metatdata is a set of name-value pairs that are assigned when teh object is uploaded
	- An object includes a key name (object-key) that uniquely identifies the object 

Use prefixes to imply a folder structure in an S3 bucket 
- A GET query with the prefix photos/2022 returns objects 

Amazon S3 benefits 
- Durability 
	- Helps ensure that data is not lost 
	- Provides S3 Standard storage with 11 nines of durability 
- Availability 
	- Provides access to data when needed 
	- Includes unlimited capacity to store data 
	- Provides S3 Standard storage with 4 nines of availability 
- High performance 
	- Achieves thousands of transactions each second when uploading and retrieving storage 
	- Automatically scales to high request rates 

Key takeaways:
- Storage comes in three basic types:
	- Block storage 
	- file storage
	- object storage 
- Amazon S3 is an object storage service 
- Amazon S3 stores massive amounts of unstructured data 
- A bucket is a container for objects that are stored in Amazon S3 
- An object is the fundamental entity that is stored in Amazon S3
- The key benefits of Amazon S3 include durability, availability and high performance 

