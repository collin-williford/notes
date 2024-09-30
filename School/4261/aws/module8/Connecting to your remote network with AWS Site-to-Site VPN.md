AWS Site-to-Site VPN 
- Creates a secure connection between an on-premises customer gateway and AWS virtual private gateway (or transit gateway) for VPC access 
- Creates two encrypted IPsec VPN tunnels for each connection across multiple Availability Zones 
- Charges for each VPN connection-hour

Connection multiple on-premises networks by using AWS VPN CloudHub
- Large corporate organization usually have multipe on-premises network enviroments that can be physically located at different premises far apart. If the enviroments need primary or backup connectivity to each of the other enviroments, you need a centralized hub to facilitate connectivity 

Accelerating Site-to-site VPN connections 
- Because public internet traffic can potentially have network distruptions, you can use AWS Global Accelerator to accelerate your Site-to-Site VPN connection. An accelerated VPN connection uses Global Accelerator to route traffic from your on-premises network to an AWS edge location that is closest to your customer gateway device. Network traffic is now using the AWS backbone infrastructure to efficiently route traffic from the edge location to the transit gateway with better response times. Note that acceleration is supported only for VPN connections that are attached to a transit gateway and not a virtual private gateway

Key takeaways:
- Site-to-Site VPN creates a secure connection between an on-premises customer gateway and an AWS virtual private gateway (or transit gateway) for VPC access 
- You can connect multiple on-premises networks to a single virtual private gateway 
- Use Global Accelerator to accelerate Site-to-Site VPN connections 
- Configure multiple Transit Gateway routing tables to isolate VPCs to provide full VPN access 