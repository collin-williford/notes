Network design with multiple VPCs
- Full mesh architecture
	- every node is directly connected to every other node 
	- Work well for networks with a small number of VPCs that require fast network speeds with little network latency 
- Hub-and-spoke architecture
	- A central intermediary hub to manage connectivity. 
	- Each node requires only one connection to the hub 

AWS Transit Gateway 
- Is a centralized, Regional router to connect VPCs and on-premises networks based on hub-and-spoke architecture 
- Is a managed AWS service that automatically scales based on the volume of network traffic 
- Can be peered with other transit gateways in other AWS Regions and AWS accounts 
- Incurs cost charges based on the number of connections and amount of traffic throughput 
- Has a Transit Gateway Flow Logs feature to publish transit gateway traffic logs 

Key takeaways:
- Transit Gateway is a centralized Regional router to connect VPCs 
- Transit Gateway can be peered with other transit gateways in other AWS Regions and AWS accounts 
- Transit Gateway supports thousands of attachments 
- Transit Gateway charges per hour for the number of connections that you make to the transit gateway and the amount of traffic that flows through the transit gateway 

