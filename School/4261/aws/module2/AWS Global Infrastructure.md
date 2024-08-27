AWS infrastructure topics
- AWS Regions 
	- 32 geographic regions
	- A region is a physical geographical location with two or more availability zones
- Availability Zones 
	- 102 availability zones
	- A availability zone consists of one or more data centers
- AWS Local Zones
- AWS data centers
- AWS points of presence (PoPs)
	- A PoPs network sits at the edge of the network to reduce latency

Selection Regions
- A region is a geographical area
- Each region usually consists of two or more Availability zones 
- Communication between regions uses AWS backbone network infrastructure 
- You enable and control data replication across Regions 
- Regions
	- Are conected to several ISPs 
	- connected to a private global netowkr backbone 
		- lower cost and more consistent cross-region network latency compared to public internet 
	- Regions are isolated for from one another

Selecting Availabiltiy Zones
- Each Availabiltiy Zone includes the following:
	- It is made up of one or more data centers
	- It is designed for fault isolation 
	- It is interconnected with other Availability Zones in a Region using high-speed private links 
- For certian services, you can choose your Availability Zones
- AWS recommends replicated across Availability Zones for resiliency 

Using Local Zones
- Local Zones make it possible for you to run latency-sensitive portions of applications closer to end users and resources in a specific geography 
- They are an extension of a Region 
- With Local Zones, you can place AWS compute, storage, database, and other select services closer to large population, industry and IT centers where no Regions exist today 
- Local Zones are managed and supported by AWS 

Role of AWS data centers
- Data centers are where the data resides and data processing occurs
- A data center typically has tens of thousands of servers
- All data centers are online and serving customers
- AWS custom network equipment includes the following:
	- Is sourced from multiple original device manufactures (ODMs)
	- Has a customized network protocol stack 

AWS PoPs
- Edge location 
	- AWS data centers and servers located close to customers and designed to deliver services with the lowest latency possible 
- Regional edge cache 
	- AWS data centers between the origin server and the edge location that have a longer cache 

Key takeaways:
- The AWS Global Infrastructure consists of Regions, Availability Zones, and edge locations
- Your choice of a Region is typically based on compliance requirements or to reduce latency
- Each Availability Zone is physically seperate from other Availability Zones and has redundant power, networking and connectivity 
- Edge locations and regional edge caches improve performance by caching content closer to users 