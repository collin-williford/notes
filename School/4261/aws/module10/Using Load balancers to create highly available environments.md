ELB
- Distrbutes traffic across multiple targets in one or more Availablity Zone
- Can receive public or private traffic 
- Monitors the health of registered targets with health checks 
- Routes traffic to only health targets 
- Scales based on incoming traffic 

Types of AWS Load Balancers 
- Application Load Balancer 
	- Is used for HTTP and HTTPS traffic 
	- Operates at OSI layer 7, the application layer 
	- Is used for application architectures 
- Network Load Balancer
	- Is used for TLS offloading, UDP and static IP addresses 
	- Operates at OSI layer 4, the transport layer 
	- Is used for millions of requests per second at ultra-low latency 
- Gateway Load Balancer 
	- Is used for third-party virtual appliance fleet using GENEVE protocol 
	- Operates at OSI layer 3, the network layer 
	- Is used to improve security, compliance and policy controls 
- Classic Load Balancer
	- Is used for previous generation EC2-Classic networks
	- Operates at OSI layers 3 and 7, the transport and application layers 
	- Is used if upgrading to other load balancers is not fesible 

Key takeaways:
- ELB distrubutes traffic across multiple targets in or more Availablity Zones and monitors the health of registered targets with health checks 
- An Application Load Balancer is used for application architectures and operates at the OSI model application layer (layer 7) 
- A Network Load Balancer is used for millions of concurrent, ultra-low latency requests and operates at the OSI model transport layer (layer 4)
- A Gateway Load Balancer is used to improve security, compliance and policy controls and operates at the OSI model network layer (layer 3)


