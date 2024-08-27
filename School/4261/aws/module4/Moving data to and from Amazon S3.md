Storage objects in Amazon S3
- There is no limit to the number of objects in a bucket 
- Uploading an object requires write permissions to the bucket 
- Objects are encrypted by default 
	- During upload, objects are automatically encrypted using server-side encryption 
	- During download, objects are decrypted 

Options for uploading objects to Amazon 
- AWS Managemnt Console 
	- Use a wizard-based approach to move data into or out of Amazon S3, including the option to drag and drop files (maximum size is 160GB)
- AWS Command Line Interface (AWS CLI)
	- Upload or download from a terminal command prompt or in a call from a script 
- AWS SDKs 
	- Use AWS SDKs to upload objects programmatically 
- Amazon S3 REST API 
	- Send a PUT request to upload data in a single operation 

Amazon S3 feature: Multipart upload 
- Multipart uploads have the following advantages:
	- Improve throughput
	- Recover quickly from any network issues 
	- Pause and resume object uploads 
	- Begin an upload before you know the final object size 

S3 Transfer Acceleration 
- Provides fast and secure transfers of files over long distances 
- Optimizes transfer speeds from across the world into S3 buckets 
- Uses globally distributed edge locations in CloudFront 
- Improves speed by 50-500 percent on average for cross-country transfer of larger objects 

AWS Transfer Family
- Is a fully managed AWS service 
- Is used to transfer files into and out of Amazon S3 storage or Amazon Elastic File System (Amazon EFS) file systems over the following protocols 

Transfer Family Benefits 
- Transfer family is a managed service that scales in real time to meet your needs
- You don't need to modify your applications or run any file transfer protocol infrastructure 
- With Transfer Family, you use native AWS services for processing, analytics, reporting, auditing, and archival functions with your data in durable Amazon S3 storage 
- Transfer Family is a managed elastic file system (with Amazon EFS) for use with AWS Cloud services and on-premises resources 
- Transfer Family is a managed, serverless file transfer workflow service that you can use to set up, run, automate and monitor file uploads 
- You pay for only the use of the service, and there are no upfront costs 

Use cases for Transfer Family 
- Amazon S3
	- Data lakes in AWS for uploads from third parties 
	- Subscription-based data distrubution with customers 
	- Internal transfers within your organization 
- Amazon EFS 
	- Data distrubution 
	- Supply chain 
	- Content management 
	- Web-serving applications 

Key takeaways 
- Upload objects to Amazon S3 by using the AWS Management Console, AWS CLI, AWS SDKs or Amazon S3 REST API 
- Use multipart upload to upload a single object as a set of parts when the object size reaches 100 MB or greater 
- Use S3 Transfer Acceleration on an S3 bucket to provide fast and secure transfers of files over long distances between your client and an S3 bucket 
- Use Transfer Family to provide a secure transfer of files into and out of AWS storage services 