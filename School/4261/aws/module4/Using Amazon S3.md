How customers use Amazon S3
- Spikes in demand 
	- Host web content that needs bandwidth to address extreme spikes in demand 
- Static site 
	- Host a static site that consists of HTML files, images and videos 
- Financial analysis 
	- Store data that other services can use for analysis 
- Disaster recovery 
	- Support disaster recovery or data backup solutions 

Use case: 
- Media hosting 
	- Amazon S3 is used to store and distrubute videos, photos, music files and other media. This contnet can be delivered directly from Amazon S3 because each object in Amazon S3 has a unique HTTP URL 
- Host static websites 
	- To host a static website, configure an S3 bucket for website hosting, and attach a bucket policy that allows access to the objects. Then upload your website to the bucket 
	- With this approach you do not need to run a virtual machine that hosts a web server
- Data store for computation and analytics 
	- An amazon EC2 spot fleet is spun up when the bid price for Spot instances is low or when an Amazon EMR cluster is spun up 
	- Regardless, after the compute capacity is available, raw unprocessed data is extracted from Amazon S3 and also from another data source 
	- The data is run through compute algorithms that integrate and transform it 
	- The resulting processed data is loaded into a differetn S3 bucket 
	- Now that the data has been processed, the compute capacity is terminated to save on costs 
	- Finally, an analytics tool, such as Amazon QuickSight, might be used to harvest meaningful insights from the processed data. This is just one example scenario of how Amazon S3 can play an essential role for data storage in a large-scale analytics solution architecture 
- Back up and archive critical data 
	- Data is backed up from an on-premises corporate data center and also from a large number of Amazon EC2 instances. These instances run applications that generate data 

Key takeaways:
- Amazon S3 is often used to do the following
	- Store and distrubute videos, photos, music file and other media 
	- Support static content, including HTML files, images, videos
	- Store data for computation and large-scale analytics 
	- Provide a data backup solution 
