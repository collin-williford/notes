Mesh architecture using VPC peering 
- When you have a small number of VPCs or your network budget is contrained by paying for transit gateway, you can use the VPC peering feature to establish a one-to-one network connection between two VPCs 

VPC peering does not support transitive peering
- Transitive peering is not supported by VPC peering. This makes peering secure and manageable to isolate errors and limit the blast radius for network attacks 

Use cases: Peering to one VPC to access centralized resources
- Your company's IT department has a VPC for file sharing. You want to  peer other VPCs to that central VPC; however, you do not want the other VPCs to send traffic to each other
- Your company has a VPC that you want to share with your customers. Each customer can create a VPC peering connection with your VPC; however your customers cannot route traffic to other VPCs that are peered to yours, nor are they aware of other customers' routes
- You have a central VPC that is used for Active Directory services. Specific instances in peer VPCs send requests to the Active Direcotry servers and require full access to the central VPC. The central VPC does not require full access to the peer VPCs; it needs only to route response traffic to the specific instances 

VPC connectivity with AWS PrivateLink architecture
- You can use AWS PrivateLink to privately connect to a service or application that resides in a service provider VPC from consumer VPCs within an AWS Region. The benefit of this architecture is that only consumer VPCs initiate connections to the service provider VPC 

Key takeaways:
- VPC peering establishes a one-to-one peering networking connection between two VPCs to provide private network traffic routes 
- VPC peering does not incur costs, but transferring data across Availability Zones and Regions does 
- VPC peering can provide network traffic flow between different AWS accounts and AWS Regions 
- VPC peering does not support transitive VPC peering relationships 
- If VPC Classless Inter-Domain Routing (CIDR) blocks overlap, use PrivateLink with a Network Load Balancer to establish VPC connectivity 