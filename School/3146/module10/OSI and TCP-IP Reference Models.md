OSI reference model 
 - OSI stands for Open Systems Interconnection 
 - Has seven layers
 - Specifies funciton of each layer
 - But doesn't specify exact services/protocols to use 
 - Applicaiton layer
	 - User interface to networking services 
	 - Provides variety of commonly used functions
		 - E.g., file transfer, e-mail, etc.
- Presentation layer
	- Handles formatting details for data
		- E.g., encryption, compression, stream formatting, etc. 
- Session layer
	- Provides services to initiate, maintain and end connection between sender and receiver
- Transport layer 
	- Provides end-to-end message delivery service
	- Control rate of transfer and ensures network is not overloaded 
		- Flow control and congestion control 
- Network layer
	- Controls actual transfer of unit of data through network 
	- Determines path to take from source to destination (routing)
	- Forwards unit of data to next node/router in path 
	- Shares congestion control responsibility 
- Data link layer
	- Transmits data over link between two nodes 
	- Performs error and flow control over link 
	- Determines when computer has the right to access medium 
		- Medium Access Control (MAC) sub-layer
- Physical layer
	- Consists of basic networking hardware
	- Transmits/receives raw bits over communication channel 
	- Determines how connection is established 
	- Determines mode of transmission 
![](Pasted%20image%2020240318143612.png)

TCP/IP reference model 
 - Has four layers
	 - Was used in ARPANET (research network sponsored by DoD)
	 - ![](Pasted%20image%2020240318143728.png)
- Named after two of its primary protocols 
	- In this model, protocols are more important than strict layering 
	- So, we will mention specific protocols in tihs context 
- Application layer 
	- Roughly covers functions of application, presentation and session layer in OSI model
	- Widley-used application layer protocols for user services 
		- Simple Mail Transfer Protocol (SMTP)
		- Hypertext Transfer Protocol (HTTP)
		- File Transfer Protocol (FTP)
- Transport Layer 
	- Similar to transport layer in OSI model 
	- Provides end-to-end message delivery service independent of underlying network 
		- Can provide reliability if needed 
	- Provides error control, flow control and congestion control 
	- Widely used protocols 
		- Transmission Control Protocol (TCP)
		- User Datagram Protocol (UDP)
- Internet layer
	- Roughly corresponds to network layer in OSI model 
	- Responsible for sending units of data over network 
		- Preforms routing for units of data
	- Provides unreliable (best-effort) service 
		- Data units could arrive out of order at destination 
	- Principal, very widley used protocol 
		- Internet Protocol (IP)
- Link layer
	- Roughly corresponds to data link and physical layers in OSI model 
	- Responsible for moving data units over link between two hosts 
		- Provides interface between hosts and transmission links
		- Includes protocols to describe local network topology 

Discussion 
 - OSI model strength is model or layering itself 
	 - Excluding presentation and session layer 
- Strength of TCP/IP model is its protocols 
- Tanenbaum book considers hybrid model 
	- ![](Pasted%20image%2020240318144843.png)

Peer Layer Communication 
![](Pasted%20image%2020240318144953.png)


