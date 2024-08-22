The Physical Layer
 - Eletrical, timing and other interfaces for transfer of dat bits between two adjacent nodes 

The Data Link Layer
 - What does the link layer do?
 - Provides well-defined services to the network layer
	 - Transfer of data unit between adjacent nodes (i.e., over single link)
		 - Unit of data given by network layer is called a packet
		 - Use physical address of nodes (MAC addresss)
		 - Receiver must be able to distinguish packets from each other 
	- Detect and/or correct transmission errors
		- Ensure packet that reaches receiver network layer is error-free
		- Error control 
	- Regulate flow of packets
		- Ensure receiver does not get inundated!
		- Flow control 

Packet transmission
 - Receiver must be able to distinguish packets from each other 
	 - Encapsulates packets given by network layer into frames
		 - Adds header and trailer to packets for this 
		 - ![](Pasted%20image%2020240325194329.png)
	- Need understanding between sender and receiver link layers on format of header/trailer
		- I.e., need link layer protocol understood by both computers

Framing
 - Byte count
 - Flag bytes with byte stuffing
 - Flag bits with bit stuffing 
 - Physical layer coding violations

Byte count 
 - Field in header contains number of bytes in frame 
 - ![](Pasted%20image%2020240325194519.png)

Flag bytes with byte stuffing
 - Each frame starts and ends with special bytes 
	 - Could use same byte - flag byte for start and end 
		- ![](Pasted%20image%2020240325194605.png)
- If receiver sees two consecutive flag bytes 
	- End of one frame and beginning of next frame 
- What if flag byte happens to occur with payload?
	- Byte stuffing - insert special escape byte before flag byte 
	- Escape byte itself can be escaped if needed
	- ![](Pasted%20image%2020240325194750.png)

Flag bits with bit stuffing
 - Each frame starts and ends with special sequence of bits
	 - Bit stuffing used if payload contains same sequence of bits
	 - ![](Pasted%20image%2020240325194840.png)
- In byte/bit stuffing, frame lengths vary based on payload

Physical layer coding violations
 - Encoding bits as signals includes redundancy 
	 - Some signals can never occur in payload
	 - Use these "reserved" signals as frame delimiters
	 - In practice, combination of different methods may be used

