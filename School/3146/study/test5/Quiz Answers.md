 13-1
 - Public IP addresses are guaranteed to be unique across the Internet. True or False
	 - True
- **IPv6** addresses are the future of the Internet Protocol. These addresses use **128** bits. THe notation used is **8** groups of **4 hexadecimal** digits each separated by colons 
-  For the subnet represented by 171.14.0.0/18, how many least significant bits are used to identify individual hosts?
	- 14
- If the IP address range for a subnet is 145.2.12.0 to 145.2.12.255, which is the correct slash notation for this subnet?
	- 145.2.12.0/24
- A subnet with a **shorter** prefix is less specific than one with a **longer** prefix. 
- Routing tables contain one etry for every possible destination IP on the internet. True or False
	- False
- How do routers extract the prefix bits from an IP address
	- The perform a binary AND operation between the IP and subnet mask
- If there are mulitiple matching entries in the routing table, the match with the most specific prefix is chosen. True or False
	- True
- Use the routing table in the following table, where will the IP 192.24.11.100 be forwarded?
	- ![](Pasted%20image%2020240503190128.png)
		- L

13-2
 - The transport layer provides **logical** end-to-end communication between hosts and is entirely run on **host** computers 
- Transport layer data **is not** examined by nodes in between the source and destiation computers
- Transport layer protocols support **concurrent** network usage by multiple **application** process on the host.
- Which of the following features may be provided by transport layer protocols?
	- Flow control 
	- Congestion Control 
- A host identifier (IP address) is known as a **Network** Service Access Point and a process identifier within a host (port number) is also known as a **Transport** Service Access Point. The combinatino of teh two identifiers forms a **socket**.
- User Datagram Protocol (UDP) is **an unreliable** **connectionless** protocol 
- UDP provides limited flow control 
	- False
- The length of the UDP header **is fixed**
- The IPv4 pseudo-header contents are not part of the UDP header and are only used in the UDP checksum calculation. 
	- True 

14-1
 - Transmission Control Protocol or TCP provides a **stream** service, which is **a reliable** **connection-oriented** service. 
 - A host must be a **listen** or **passive open** state in order to receive incoming TCP connection requests 
 - TCP uses a mechanism called **sequence numbers** through which the destination/receiver can specify which **segment** it is acknowledging and through which the destination node can **reconstruct** the original stream of data if needed
 - If the SYN flag is set to 1 in a segment sent by host A to host B, the sequence number field indicates the **initial** sequence number that host **A** will use in segments that it sends to host B. If the SYN flag is set to 0 in the segment sent by host A to host **B**, the sequence number feidl indicates the **sequence number of the first data byte** in the segment. 
 - Connection establishment in TCP requires a **3**-way handshake between the two hosts involved
 - Which of the following flags are used during the connection establishment phase of TCP?
	 - SYN
	 - ACK
- TCP uses a mechanism called the **sliding window** protocol for flow control 
- Congestion control is achieved in TCP by adjusting the **transmission** rate on the sender/source node

15-1
 - The fundamental responsibility of the Application layer is to provide **networking** services to **users**.
 - Domain Name System (DNS) is a service that resolves **Human-readable names** into **IP addresses**
 - DNS uses **name** **servers** to maintain the mapping it needs
 - Name resolution performed by DNS is a single stp process
	 - False 
- A DNS cache is a temporary **database** that contains a record of recent and attempted **visits** to websites or other intenet domains 
- A DNS cache becomes **poisoned** when **unauthorized** domain names or IP addresses are inserted into it 

15-2
 - The world wide web is a vast collection of **pages** which are named with a **Uniform Resource Locator**
 - The viewing of a webpage on a browser is the result of a conversation between the browser (which acts as the **client**) and the **server**. 
 - Consider the following URL and identify its constituent parts: \https://www.lifewire.com/how-urls-work-2482921. What is the protocol **https**. What is the server name? **\www.lifewire.com** What is the name of the page being requested? **how-urls-work-2482921**
 - Secure Shell or SSH is a **network** protocol for **securing** data that flows between a client and a server
 - FTP and Telnet, two other protocols that send data across a network, are differetn from SSh in that they send unencrypted data. SSH on the other hand, sends **encrypted** data using a set of cryptographic **keys**. 
 - Select ALL that apply. What are some things that you can do securely with SSH.
	 - Transfer files across a network 
	 - Execute system commands from a remote location 
	 - Perform port forwarding
- Port forwarding allows traffic flowing from an SSH client to an SSH server to be **multiplexed** into port **22** and then sent across the network in an encrypted tunnel.

