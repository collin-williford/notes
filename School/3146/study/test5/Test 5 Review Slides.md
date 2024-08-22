  - OSI Model - What it actually looks like
	  - 7 Layers
		  - Application
			  - End user layer
			  - HTTP, FTP, IRC, SSH, DNS
		- Presentation
			- Syntax layer
			- SSL, SSH, IMAP, FTP, MPEG, JPEG
		- Session
			- Synch and send to prot
			- API's, Sockets, WinSock
		- Transport
			- End-to-End connections
			- TCP, UDP
		- Network
			- Packets
			- IP, ICMP, IPSec, IGMP
		- Data Link 
			- Frames
			- Ethernet, PPP, Switch, Bridge
		- Physical
			- Physical structure
			- Coax, Fiber, Wireless, Hubs, Repeaters

Binary / Hexadecimal converstion
 - Binary to Hexadecimal
	 - Four binary bits is the same as one hex value
		 - For example - '1111' in binary is the same as 'F' in hex
- Hex to binary 
	- One hex value is the same as four binary bits 
		- For example - 'A' in hex is the same as '1010' in binary 
- Decimal as a buffer
	- It may be useful to convert the value from the source type to decimal then to the target type 
		- binary to hex
			- 1011 -> 11 -> B
		- Hex to binary 
			- C -> 12 -> 1100

Subnet Host Calculation
 - You are given a subnet mask with a value of 255.255.192.0 What are the total and actual number of hosts that the subnet can handle?
	 - Convert 255.255.190.0 to Binary 
		 - 11111111.11111111.11000000.00000000
		 - 32-18 = 14
		 - 2^14 = 16384 total number of hosts
		 - 16384 - 2 = 16382 actual number of hosts (first address (network address) and last address (broadcast address) are not usable for hosts)

Subnet Mask Calculation 
 - Given the following subnet - 135.99.82.4/14 - What is the subnet mask in binary that will be used by the router to extract the prefix bits?
	 - Answer:
		 - 32 - 14 = 18
		 - 11111111 11111100 00000000 00000000

Transport Layer - TCP/UDP Overview
 - TCP - Reliable-Connection Oriented service
	 - Delivers in order
	 - Handles flow control, congetsion control 
	 - Used for reliability 
	 - Uses acknowledgements
- UDP - Unreliable, Connectionless
	- Limited error control 
	- No flow and congestion control 
	- Best for programs with handle error control themselves

Transport Layer - Congestion Control 
 - TCP utilizes congestion control to avoid and recover from network congestion 
 - Sender adjusts transmission rate of packets according to congestion 
 - Uses a variable size congestion window and threshold to restrict number of packets to send
 - Mechanisms such as TCP Reno, TCP Tahoe, etc.
 - Different than flow control deals with which packets can be send in relation to the receiver's window, congestion control restricts packets based on network congestion 

Application Layer - HTTP, FTP, SSH, SMTP
 - HTTP is the protocol of the world wide web, used to transfer web pages and other web objects between browsers and web servers
	 - Stateless, request-response protocl over TCP, port 80
- FTP is use to transfer files from host to host
	- Not seucre by default, port 21
- SSH is protocol for secure communication between hosts
	- Hosts use cryptographic keys to encrypt communication tunnel, port 22 
- SMTP is used to push emails to a mail server
	- Port 22 