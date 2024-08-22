Transport layer
 - Provide logical end-to-end communication between source and destination 
 - ![](Pasted%20image%2020240415173236.png)
 - Run entirely on host computers
	 - Network layer protocols run on host and routers
- Supports concurrent network usage by multiple processes
	- Provides communication between application processes on hosts
	- Provides clean interface for procescesses to use 
- Relies on and enhance network layer services
- Can provide connection-oriented or connectionless service
- Can provide following features 
	- Reliability
		- even on top of an unreliable network 
	- Flow control 
	- Congestion control 

Supporting Multiple Processes
 - Know how to identify hosts
	 - IP address
	 - Network Service Access Point (NSAP)
- Need to identify processes in host 
	- Port number
	- Transport Serivce Access Point (TSAP)
- Host address + process port number -> socket

Let's clarify some terminology
![](Pasted%20image%2020240415173704.png)

Transport layer protocols in the Internet
 - We will look at two widley used protocols 
	 - User Datagram Protocol (UDP)
	 - Transmission Control Protocol (TCP)

User Datagram Protocol (UDP)
 - Unreliable (best-effort)
 - Connectionless
 - Limited error control 
 - No flow control or congestion control 
 - Suitable for 
	 - Request-response communication with no error/flow control
	 - Use with applications that handle error/flow control 
	 - Multicast or broadcast communication 
- UDP header
- ![](Pasted%20image%2020240415174128.png)
	- Source port
		- Application port number within source host
	- Destination port
		- Application port member within destination host 
	- UDP length
		- 8 bytes header length + length of data
	- UDP checksum
		- Optional checksum for UDP header, IPv4 pseudo-header and data
- IPv4 pseudo-header included in UDP checksum
	- ![](Pasted%20image%2020240415174406.png)
		- UDP length
			- Length of UDP segment (UDP header + data)