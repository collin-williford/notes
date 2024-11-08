Content delivery network (CDN)
- Delivery challenge 
	- Deliver geographically dispersed content with low latency and low cost for end users to access 
- CDN solution 
	- Is a globally distributed system of cahcing servers
	- Has intermediary servers betweeen the client and the application
	- Caches copies of commonly requested files (static content)
	- Delivers a local copy of the requested content from a nearby cache edge or point of presence 

Which type of content can you cache by using an edge cache?
- Dynamically generated content cannot be cached by using an edge cache 
- Images can be cached 
- Videos can be cached 
- User-generated data cannot be cached by using an edge cache 
- Web objects can be cached 

CloudFront 
- Is a CDN service that delivers content across the globe securely with low latency and high transfer speeds 
- Provides high-speed content distribution by delivering through edge locaions 
- Improves application resiliency from distributed denial of service (DDoS) attacks by leveraging services such as AWS Shield and AWS WAF 

CloudFront global edge network components 
- CloudFront edge locations 
	- Are more numerous and closer to users 
	- Have smaller caches 
	- Help ensure that popular content can be served quickly to viewers
- CloudFront Regional edge caches 
	- Are fewer and farther away from users 
	- Have larger caches 
	- Helps with less popular content in particular 

How to configure a CloudFront distribution 
- Specify an origin location 
- Configure the distribution 
- CloudFront becomes available 
- CloudFront sends your distribution's configuration to edge locations 

Controlling how long content is cached 
- Set a maximum TTL value 
	- Expires cached content faster with a low maximum TTL value 
- Implemet content versioning 
	- Fetches and caches new files immediately 
- Specify cache-control headers
	- Provides precise control over content expiration for individual files 
- Use CloudFront invalidation requests
	- Forces CloudFront to expire content from edge caches 

DDoS mitigation 
- Security challenge 
	- Publicly accessible content is exposed to common web threats that affect availability and compromise security 
- CloudFront solution 
	- Monitoring and mitigation are built into Amazon Route 53 as it routes traffic to CloudFront 
	- CloudFront can create an AWS WAF web access control list (ACL) that configures rules to analyze incoming requests and block threats before they reach your servers 
	- Shield DDoS mitigations allow only traffic that is valid for web applications to pass through CloudFront 

Key takeaways:
- Static caching is done by using a CDN
- CloudFront is a CDN service that uses edge locations and Regional edge caches to deliver content securely across the globe 
- You can control CloudFront caching behavior by using a combination of actions 
- By using CloudFront for distributing content, you are also protecting your systems from DDoS attacks 

