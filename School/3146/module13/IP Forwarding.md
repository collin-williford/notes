 IP Forwarding
  - Packet must be forwarded based on destination IP address
  - Should routing table have one entry per destination IP?
	  - Routing table explosion 
- All IP addresses on one subnet have same prefix 
	- Can combine destination addresses within subnet 
	- Routing tables needs to store just one entry for each prefix 
	- ![](Pasted%20image%2020240408181024.png)
	- 
- Router matches destination IP address without prefixes in table 
	- IP address and-ed with subnet mask to extract prefix bits
	- Subnet mask contains 1 in all prefix bits and 0 for host bits
	- ![](Pasted%20image%2020240408181141.png)
- One entry per subnet is also very large
	- Route aggregation can be performed (supernet)
	- ![](Pasted%20image%2020240408181252.png)
	- Router in London keeps all entries 
	- Router in New York could aggregate entries 1, 2 and 4
	- ![](Pasted%20image%2020240408181327.png)
	- Destination IP address 194.24.16.150
		- Forwward to L
	- Destination IP address 194.24.15.104
		- Forward to C
	- If prefixes overlap, forward based on longest matching prefix 