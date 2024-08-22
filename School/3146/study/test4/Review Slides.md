 - Mesh Topology
	 - Each computer is connected to every other computer 
	 - Typically used for larger spaces, like a corporate office 
		 - Each node can ast as a router to other nodes
	- When working with wifi, makes for stronger connections throughtout the space

- Bus Topology
	- Each computer is connected to a common bus
	- Generally viewed as the easiest network toconnect node linearly 
	- Requires less physical wire than something like a star or mesh network 

- Ring Topology
	- Each computer is connected to two neighbors
	- Data flows in one direction, thus causing less collision of packets
	- A central server is not needed to manage the networking connections
	- Potential of a node becoming inaccessiable if the nodes tothe left and right of it go offline

Star Topology
 - Each computer is connected to a central hub node that helps with routing 
 - Standard star topologies (seen top right) are ensure that no node becomes unreachable by some other node going down
 - Extended star topologies are scalable version of standard star topologies

OSI Model - What it actually looks like
- Application
	- End user layer
	- HTTP, FTP, IRC, SSH, DNS
- Presentation
	- Syntax layer
	- SLL, SSH, IMAP, FTP, MPEG, JPEG
- Session
	- Synch and send to port
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
	- Coax, Fiber, Wireless, Hubs, Repeaters

Alternatives
 - TCP/IP Model
	 - Created by US Department of Defense in 1960's
		 - Intent was to create an easy to understand model
	- Combine Presentation, Session and Application layers into one Applicaiton layer

Data Link Layer - ARP - Address Resolution Protocol 
 - What is this?
	 - Helps to map IP addresses to MAC addresses
- What is a MAC address?
	- The hardware address
	- Uniquely identifies that particular machine
- What are we using ARP?
	- Great for seeing what machine is one what network

Framing
 - Network traffic is sent in the form of packets
	 - Data in packets are in raw binary form, like most data
	 - Need ways to denote the beginning and end of a piece of datum (piece of information)
- Framing comes in two flavors (for this class)
	- Bit stuffing
		- Stuffing of the physical binary bits
	- Byte stuffing 
		- Stuffing of the physical bytes
- Important to recognize specified "special characters"

Binary  / Hexadecimal Conversion 
 - Binary to Hexadecimal 
	 - Four binary bits is the same as one hexadecimal value 
		 - For example  - '1111' in binary is 'F' in hexadecimal 
- Hexadecimal to binary 
	- One hexadecimal value is the same as four binary bits
		- For example - 'A' in hexadecimal is the same as '1010' in binary 
- Decimal as a Buffer
	- It may be useful to convert the value from the source type to decimal then to the target type
		- Binary to hex - '1011' -> 11 -> 'B'
		- Hex to Binary - 'C' -> 12 -> '1101'

IPv4
 - 32 bit address
 - Four 8 bit numbers separated by periods
	 - 10101100 00010000 00000000 01100100
- Each section is translated to decimal 
	- 172.16.0.100

Network Layer - IPv6
 - 128 bit address
 - 8 groups of 4 hexadecimal digits separated by colons 
	 - 2001:0DB8:0000:0000:0000:ff00:0042:8329
- Can omit leading zeros
	- 2001:DB8:0:0:0:ff00:8329

