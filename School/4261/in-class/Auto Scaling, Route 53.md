Services related to auto scaling 
- Computing 
	- Auto scaling group of EC2 
	- ECS 
	- DynamoDB 
	- Aurora 
- Elastic Load Balancing (ELB)
	- Application load balancer 
	- Network load balancer 
	- Classic load balancer 
- Route 53 

Auto Scaling Group 
- Maintain 
	- Ensures the required number of instances are running 
	- Use when you always need a known number of instances running at all times 
- Manual 
	- Manually change desired capacity 
	- Use when your needs change rarely enough that you're ok to make manual changes 
- Scheduled 
	- Adjust min/max on specific dates/times or recurring time periods 
	- Use when you know your busy and quiet tunes are, Useful for ensuring enough instances are available before very busy times 
- Step scaling 
	- Define resources based on metrics ranges 
	- Lower bound, upper bound, adjustment type, amount to increase the desired capacity 
- Simple scaling 
	- One of: ChangeCapacity, ExactCapacity, PercentChangeCapacity
	- Whenever metric rises above a threshold, change capacity in one of three ways, cooldown period before executing policy again 
- Dynamics 
	- Scale in response to system load or other triggers using metrics 
	- Useful for changing capacity based on system utilization, eg.g CPU hits 80% 
- Predictive 
	- Predict capacity required ahead of time using ML 
	- Useful when capacity and number of instances is unknown 

DDOS Protection 
- ELB provides standard DDOS protection for free 
- WAF can be used with ALB 
	- Block certain IP addresses 
	- Reduce rates from a specific IP address
	- This can be effective against certain types of DDOS attacks 

Listeners and Rules 
- Each ALB needs at least one listener and can have up to 10 
- Listeners define the port and protocols to listen on 
- Cannot have the same port in multiple listeners 
- Two types of rules for listeners when condition med, action taken 
	- Host (domain-based e.g. example.com)
	- Path (e.g. example.com/images)
	- combined
- Rules can route based on the content of the request for either host or path 
	- E.g. query string paramter, request method, and source IP 

Route53 Record Types 
- A record: IPv4
- AAAA record: IPv6
- CNAME record: map one DNS (e.g. example.com) to another DNS name (e.g. elb1234.amazonaws.com)
- Alias record: AWS specific record type 
	- Map resource record sets in your hosted zone to Amazon Elastic Load Balancing load balancers, Amazon CloudFront distributions, AWS Elastic Beanstalk environments, or Amazon S3 buckets that are configured as websites 
	- Works like CNAME 
	- Use Alias whenever possible (free) 

Global Accelerator 
- High performance AWS network 
	- Fault tolerance 
	- Traffic does not use Internet (except for on and off ramp) 
	- Two static IP addresses (IPv4) serviced by independent network zones 
	- Comes with Shield standard and can enable Shield advanced 

