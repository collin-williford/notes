Transmission Control Protocol (TCP)
 - Stream service
	 - Reliable, connnection-oriented service
	 - In-order devlivery to application process
- Flow control
- Congestion
- Has significant overhead
	- Suitable for applications that need this degree of reliability

Connections in TCP
 - Host being connected to must be ready to accept connections
	 - Listen or passive open state
- Host that wants to establish new connection 
	- Connect or active open state
- E.g., server is in passive open state and clients can establish connections with server

Reliable, in-order delivery
 - Acknowledgement
	 - Receiver acknowledges receipt of every segment (ACK)
- Retransmission
	- When segment sent, retransmission timer started
	- If ACK received before timer expires, timer stopped
	- If timer goes off, segment retransmitted
- Sequence number
	- Used by receiver to identify correct order of stream

TCP header
 - ![](Pasted%20image%2020240417200350.png)
	 - CWR, ECE
		 - Flags for Explicit Congestion Notification (ECN)
	- URG
		- 1 indicates segment is urgen and that urgent pointer is significant
	- ACK
		- Value of 1 indicates inclusion of acknowledgement adn that acknowledgement number is significant
	- PSH
		- Value of 1 informs TCP to push segments received so far to application right away
	- RST
		- Value of 1 indicates with to reset connection 
	- SYN
		- Value of 1 marks beginning of connection 
	- FIN
		- Value of 1 indicates sender has no more data to transmit
	- Sequence number
		- If SYN is 1, initial sequence number (first data byte is initial + 1)
		- If SYN is 0, sequence number of first data byte in segment
	- Acknowledgement number
		- If ACK is 1, indicates next sequence number receiver is expecting
	- Window Size
		- Range of sequence number beyond last acknowledged one that sender is free to transmit without further acknowledgement (flow control)
	- Checksum
		- Checksum, including TCP header, IPv4 pseudo-header adn TCP data
	- Urgent Pointer
		- If URG is 1, offset pointing to sequence number of urgent data

Connections in TCP
 - 3-way handshake to start connection 
	 - Host 2 -> passive open state
	 - Host 1 -> requests new connection 
		 - Host 1 sends segment with SYN = 1 and SEQ num = x
		 - Host 2 responds with ACK = 1, ACK  num = x + 1, SYN = 1, and SEQ num = y
		 - Host 1 sends segment with SYN = 0, ACK flag = 1, ACK num = y + 1
	- ![](Pasted%20image%2020240417201134.png)
	- Connection is now active 
- Connection termination -> independently for each direction 
	- One computer (say Host 1) sends segmeent with FIN = 1
	- Other computer (say Host 2) acknowledges FIN
	- Communication stops in direction Host 1 -> Host 2
- Pair of two-way handshakes 
- Each side uses timer
	- If FIN now acknowledged before timer expires, connection released

Flow control in TCP
 - Flow control -> ensure sender does not inundate receiver 
 - Mechanism used in TCP: sliding window protocol
	 - Window field set by receiver
	- Sequence numbers beyond last acknowledged one that sender is allowed to transmit before it receives more acknowledgements
- ![](Pasted%20image%2020240417201516.png)

Congestion Control in TCP
 - Congestion control -> avoid/recover from congestion
	 - Network layer detects congestion and notifies sender
	 - Transport layer on sender side adjusts transmission rate
		 - Uses congestion window to restrict number of segments in network 