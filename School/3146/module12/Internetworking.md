 - Several routing algorithms considered so far assume 
	 - Homogeneous network 
	 - All nodes use common protocols in all layers
- Not true in reality 
	- Networks may differ in several ways
- In what ways do networks differ?
	- Services:
		- connectionless versus connection oriented
	- Addressing
		- different sizes, flat or hierarchial 
	- Packet size
		- Different maximum sizes
	- Quality of Service
		- Priority
- ![](Pasted%20image%2020240402144138.png)

One Solution - Cerf & Kahn
 - Common network layer above different physical networks
	 - E.g., Internet Protocol (IP): foundation of the Internet
- ![](Pasted%20image%2020240402144345.png)

Internet Protocol (IP)
 - Common network layer protocol
	 - Glue that holds Internet together
- Connectionless, best efforts service 
	- No reliability guarantees
	- No ordering guarantees
- IP versions
	- Version 4 (IPv4)
	- Version 6 (IPv6)

IP version 4 (IPv4)
 - IPv4 header included in all network layer packet 
 - ![](Pasted%20image%2020240402144543.png)
 - IHL
	 - Header length in 32-bit words - min 5 words (20 bytes), max 15 words (60 bytes)
 - Differentiated services 
	 - Current usage: Service class and explicit congestion notification bits 
- Total length: 
	- Total length of entire packet (header + data) - max 64KB
- Identification
	- Packet identification when fragmentation is used
- DF, MF
	- "Don't Fragment"
	- "More Fragment" flags
- Fragment offset 
	- Fragment offset within packet (max 8K fragments per packet)
- Time to live
	- Counter used to limit packet lifetime (decremented on each hop)
- Protocol 
	- Which transport layer process to give packet to 
- Header checksum
	- Checksum used for error dectection
- Source address & destination address
	- Source and destination endpoint address
- Options
	- Specify options - security options, routing options, etc.

Keeping up with growth
 - IPv4 can't keep up with growing size of the Internet
 - New version -> IPv6
	 - Supports 128-bit address
	 - Has simpler header -> reduces processing overhead
	 - Better support options
- Has not been easy to deploy on Internet-scale
	- Does not internetwork easily with IPv4

IP version 6 
 - Required header
 - ![](Pasted%20image%2020240402150923.png)
 - Flow label 
	 - Way to make groups of packets with same requirements
- Payload length
	- Length of payload after required header
- Next header
	- Indicates optional extension headers; in last extension header, indicates trasnport layer handler
- Hop limit
	- Limits packet lifetime (same leaning as time to live field in IPv4)
- Source address and Destination address
	- Source and destinatino endpoint addresses

IP version 6 
 - Extension headers handle other functionality
 - ![](Pasted%20image%2020240402151243.png)
 - 