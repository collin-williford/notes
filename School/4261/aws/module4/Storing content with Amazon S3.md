Object storage classes 
- General purpose 
	- S3 standard 
		- >= 3 Availability zones
- Intelligent tiering 
	- S3 Intelligent-Tiering 
		- >= 3 Availability zones
- Infrequent access
	- S3 Standard-IA
		- >= 3 Availablity zones 
		- 128 KB minimum capacity charge for each object 
		- 30 days minimum storage duration 
		- Per GB retrieved retrieval charge 
	- S3 One Zone-IA 
		- 1 availabilty zone
		- 128 KB minimum capacity charge for each object 
		- 30 days minimum storage duration 
		- Per GB retrieved retrieval charge 
- Archive 
	- S3 Glacier Instance Retrieval 
		- >= 3 availability zones
		- 128 KB minimum capacity charge for each object 
		- 90 days minimum storage duration charge 
		- Per GB retrieved retrieval charge
	- S3 Glacier Flexible Retrieval 
		- >= 3 availability zones
		- 90 days minimum storage duriation charge 
		- Per GB retrieved retrieval charge 
	- S3 Glacier Deep Archive
		- >= 3 availability zones
		- 180 days minimum storage duration charge 
		- per GB retrieved retrieval charge 
	- S3 on Outposts 
All storage class are desiged for the following
- Durability at 99.999999999 percent 
- Availability at 99.9 percent with S3 One Zone-IA at 99.5 percent 
- Available service-level agreement (SLA) at 99 percent 
- Millisecond latency for the first byte of data 
- Object storage type 
- Lifecycle transitions 

Configuring an Amazon S3 Lifecycle 
- Amazon S3 lifecycle configurations are a set of rules that define actions that Amazon S3 applies to a group of objects 
	- Transition actions transition to another storage class 
	- Expiration actions defind when objects expire 
- Set an S3 lifecycle policy -> Data will automatically transfer to a different storage class without any changes to your application 

Amazon S3 lifecycle examples 
- S3 Standard (required for 30 days) -> delete 
- Amazon S3 Glacier (archived for 10 years for regulatory compliance)
- S3 Standard (frequently accessed for 60 days) -> S3 Standard-IA (infrequently accessed for 1 year) -> Amazon S3 Glacier (Archived for 7 years) -> delete 

Amazon S3 versioning 
- Amazon S3 versioning protects objects fom accidental overwrites and deletes 
- Upload an object with the same key 
	- Versioning enabled 
		- Creates a new object with a different version ID, and both are retrievable by the version ID 
	- Versioning disabled or suspended 
		- Overwrites the original object, and the previous object is no longer retrievable 
- Delete 
	- Versioning enabled 
		- Adds a delete marker, but the object is still retrievable by the version ID 
	- disabled/suspended
		- Deletes the object, and it is no longer retrievable 

Adding an object in a versioning-enabled bucket 
- When you use a PUT request to add an object into a versioning-enabled bucket, the noncurrent version is not overwritten. As the diagram shows, when a new version of photo.gif is PUT into a bucket that already contains an object wth the same name, the following behavior occurs:
	- The original object (ID == 1111111) remains in the bucket 
	- Amazon S3 generates a new version ID 121212 and adds this newer version of teh object to the bucket 

Deleting an object in a version-enabled bucket 
- When a request is made to delete an object in a version-enabled bucket, all versions remain in the bucket, but Amazon S3 inserts a delete marker 

Retrieving the most recently stored version 
- Requests for an object key return the most recent version 
- If the most recent version is a delete marker, the request is not successful 

Retrieving an object with its specific ID 
- Requests for an object with its version ID will successfully return that version of the object 

Permanently delete an object 
- Owners of the bucket can permanently delete an object by using delete with the version ID 
- In this case, no delete marker is added, and the specified version is not recoverable 

Support for cross-origin resource sharing (CORS)
- You want to host a web font in your S3 bucket. A webpage in an alternate domain may try to use this web font. Before the browser loads this webpage, it performs a CORS check to make sure that the domain from which the page is being loaded is allowed to access S3 bucket resources 

Amazon S3 data consistency model 
- Is consistent for all new and existing objects in all Regions 
- Provides read-after-write consistency for all GET, LIST, PUT, and DELETE operations on objects in S3 buckets 
- Offers an advantage for big data workloads 
- Simplifies the migration of on-premises analytics workloads 

Key takeaways
- S3 Standard storage is appropriate for cloud applications, dynamic websites, content distrubution, mobile and gaming applications, and big data analytics
- Set an S3 lifecycle policy and your data will automatically transfer to a different storage class without any changes to your application 
- Recover from both unintended user actions and application failures by using versioning 
- CORS defines a way for client web applications that are loaded in one domain to interact with resources in a different domain 
- The Amazon S3 data consistency model simplifies the migration of on-premises analytics workloads by removing the need to make changes to support applications 