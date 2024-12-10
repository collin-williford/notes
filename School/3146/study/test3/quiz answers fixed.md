8-1
 - Compaction is an option to reduce **external** fragmentation of main memory. The disadvantage of this approach is that it is **expensive** to keep doing it every now and then. 
 - Paging is a **mechanism** that allows a process to be split into multiple parts and allocated to multiple partitions. Here, the main memory is divided into equal sized blocks called **page frames** and the logical address space of a process is divided into blocks of the same size called **pages** 
 - Logical pages of a given process must always be allocated to contiguous page frames in the physical main memory. 
	 - False
- To keep track of what logical page of which process maps to what physical page frame in the main memory, the Operating Systems use structures called **page tables**.
- In a paged system, the logical address issued by a process includes two parts, namely, the logical **page** number and the **offset** within it. Similarly, the physical address includes the physical **page frame** number and the **offset** within it. 
- The operating system is responsible for translating the logical address issued by a process into a physical address. While doing so, it can retain the **offset** as it is. To speed up access to page table entries, systems typically store frequently used page table entries in a special cache called the **Translation look-aside** buffer. 
- A process may not use all of its data all the time. An approach in which pages may be brought into the main memory as needed is called **demand paging**. When using this approach, if a process request for data on some page and that page is not in the main memory yet, a **page fault** is said to occur. In a system using this approach, logical - also known as **virtual** addresses may be **longer** than physical addresses. 

8-2
 - Choose answers from each dropdown boxes below that will correctly complete the "algorithm" shown below for the Optimal page replaement policy. 
	 - If (newly requested page is already in main memory) 
		 - access is a hit
	- else 
		- access causes a page fault
		- identify page whose next access will be farthest in the future
		- replace identified page with newly requested page

- First In First Out page replacement policy algorithm
	- If (newly requested page is already in main memory) 
		- access is a hit
	- else 
		- access causes a page fault
		- identify page that was brought into main memory the longest time ago
		- replace identified page with newly requested page. 

- Second Chance page replacement policy 
	- If (newly requested page is already in the main memory)
		- access is a hit 
		- set reference bit to true
	- else 
		- access causes a page fault
		- do
			- identify page currently marked as the oldest page 
			- If (identified page has its reference bit set to true) 
				- mark identifed page as the newest page
				- set reference bit of identified page to false
				- mark the second oldest page as the oldest page 
			- else 
				- replace identified page with newly requested page
				- break out of loop

 - Least Recently Used page replacement policy 
	 - If (newly requested page is already in main memory) 
		 - access is a hit
	- else 
		- access causes a page fault
		- Identify page whose previous access was farthest in the past 
		- replace identified page with newly requested page


9-1
 - Data on a disk is organized as a sequence of equal-sized **blocks**.

 - The following characteristics of **non-volatile**, **long-term** storage:
	 - Must store very large amount of information 
	 - Must persist beyond process lifetime
	 - Must be accessible by multiple processes at once

 - What is one of the benefits of using contiguous allocation?
	 - Figuring out the location of a specific file block requires a very simple calculation 

 - When using a File Allocation Table that is loaded in memory, when is a disk access needed?
	 - To actually fetch a block after it has been located

 - Operating systems that use i-node file allocation typically impose a limit on:
	 - The number of files that a process can open at any given time and the total number of files that can be open at any given time on a system 

 - Match the given description with its corresponding access mode
	 - Read
		 - Grants the capability of view the contents of the file 
	- Write 
		- Grants the capability of modify or remove the content of the file 
	- Execute
		- User with execute permissions can run a file as a program 

 - When using absolute permissions, what number can be used to grant permissions to view and modify the contents of a file and also to run it if it is a program?
	 - 7

 - What is the Unix command to change file or directory permissions?
	 - chmod

 - What is the Unix command to change the owner or a file or directory?
	 - chown

9-2-2
 - A computer network is one that provides **communication** among computers, i.e., it is a **mechanism** through which computers can exchange **data**
 - Which of the following represet possible uses of a computer network?
	 - To share storage space among multiple computers
	 - Information sharing among people
- In a postal network, every sender and receiver is uniquely identified by a postal address. In a plain old telephone network, each telephone is uniquely identified by a telephone number. Similarly, any computer or device that is connected to the Internet is uniquely identified by a/an **IP address**
- IPv4 addresses are **32** bits long and are represented using the **dotted** **decimal** notation.

9-2-3
 - The **source** or sender component of a network generates the data to be sent and uses a **transmitter** component, which converts the data into signals that can be carried by a **communication** medium. 
 - The **receiver** converts signals back into data and passes this data onto the destination computer.
 - Select ALL that apply. Which of the following are considered to be mediums of communication?
	 - Co-axial cables 
	 - Bluetooth
	 - WiFi
- Match the topology with a accurate statements about that topology
	- Mesh topology
		- Every computer has a direct connection with every other computer 
	- Bus topology 
		- All computers are connected to a common component which allows every computer to communicate with every other computer
	- Ring topology
		- Every computer is connected to two neighbors
	- Star topology
		- Computers are connected to a central hub
	- Tree topology
		- computers are arranged hierarchically
- Match the network type with the correct example
	- Personal Area Network (PAN)
		- Two devices connected via bluetooth
	- Local Area Network (LAN)
		- Two computers networked in a single room, connected via ethernet cables
	- Metropolitan Area Network (MAN)
		- Cable television service connected via co-axial cables
	- Wide Area Network (WAN)
		- Multiple devices connected across an entire country, connected wirelessly 
- In a **client-server** model a central computer is a provider of services and resources and other computers are consumers of those services and resrouces. In a **peer-to-peer** model computers can be both providers and consumers of data or services
- Each layer in a network software **abstracts** a set of services, which means underlying details are hidden to other layers
- Data in a layered approach travels from the **top** to the **bottom** layer on the sender side, but travels from the **bottom** to the **top** layer on the receiver side
- True or False. Peer layers (i.e., layers with same number on two different computers) in a layered approach communicate directly with one another 
	- False
- In a layered approach, a given layer could change individual **protocols** without affecting other layers.

10-1
 - The Open Systems Interconnected (OSI) model specifies the **function** of each layer, but does not specify what **protocols** each layer will use
 - Match the OSI layer with its responsibility 
	 - Application layer
		 - Handles the user interfaces to networking devices
	- Presentation layer
		- Handles formatting the details for the data
	- Session Layer
		- Handles the initiation, maintance and termination of the connection
	- Transportation 
		- Handles the transfer of messages between the sender and receiver 
	- Network Layer
		- Handles the path or rout between source and destination through the network
	- Data Link Layer
		- Handles the transmission of data between two nodes
	- Physical layer
		- Handles the transmission of raw bits over the communication channel 
- Unlike the OSI Model, **protocols** are specifed and are part of the TCP/IP reference model
- In the TCP/IP model, the **applicaiton** layer covers the same functionality as the application, presentation, and session layers in the OSI model. The internet layer in the TCP/IP model corresponds with the **network** layer in the OSI model. The **link** layer in the TCP/IP model corresponds with the data link and physical layers in the OSI model
- Wireshark is a software that can capture **packets** that are sent and received over your network for analysis
- True or False. Wireshark packet captures can be exported.
	- True
- Proxy servers and firewalls operate at the **transport** layer
- Match the OSI layer with the protocols
	- Application Layer 
		- HTTP, SMTP, FTP, Telenet
	- Presentation Layer
		- ASCII, MP3, JPEG, MPEG
	- Session Layer
		- Netbios
	- Transportation Layer
		- TCP, UDP
	- Network Layer
		- IP
	- Data Link Layer
		- Ethernet 
	- Physical Layer
		- Cat5 Cable 
- The Statistics -> Protocol Hierarchy menue item will give you the layout of all the different **protocols** found by wireshark
- In Wireshark, you can see that frame corresponds to the **physical** layer and you will be able to similarly see how different protocols correspond to different layers in the OSI model.

11-1
 - In a reliable network service, the sender requires an acknowledge ment from the receiver. True or False
	 - True
- The link layer deals with 
	- Logical units of data
- What does it mean when we say that the receiver knows how to de-stuff the received bytes?
	- The receiver ignores escape bytes inserted when the flag byte occurs in the payload
- In bit stuffing, each data frame starts and ends with a special **sequence** of **bits**
- Match the given enviroment with the error control approach that should be used with it
	- Media that is not error prone (optical fiber) 
		- Error detecting codes
	- Media that is error prone (wireless links)
		- Error correcting codes
- Hamming code and Reed-Solomon code are examples of **error correcting codes**
- Which value (or field) in the IP header (layer-3) is used to prevent accidental routing loops?
	- Time to Live
- The source address field in the TCP IP header contains the **IP** address of the original **sender** of the **packet**.
- The **ACK** flag is set to 1 in the TCP IP header to indicate that the value in the Acknowledgment number field is the next sequence number that the receiver is expecting 
- The **FIN** flag is set to 1 in the TCP IP header to indicate that the sender has no more data to send

11-2
 - Most applications use an IP address, which is a **logical** address to send/receive messages, but the actual communication happens over a MAC address, which is a **Physical** address
 - ARP stands for Address **Resolution** Protocol
 - Nodes or systems keeps an ARP **table** or "cache" to store a mapping between IP addresses and MAC addresses
 - When an IP address is not found in the ARP cache of a system, the system needs to initiate an ARP request. An ARP request is a broadcast whereas an ARP response is a unicast
 - The ARP cache **timeout** indicates the time for which a MAC address can reside in the cache
 - The Linux command for displaying the ARP table is **arp -a**

12-1
 - The primary goal of the network layer is to transfer packets between the **source** of the data and the **final** **destination**, possibly via multiple **links**
 - The network layer is responsible for routing (i.e., identifying the **path** that a packet must take to get from the source node to the destination node) and **forwarding** received packets to the next node along the identifed **path**
 - Which of the following additional responsibilities does the network layer have
	 - Congestion control
	 - Internetworking
- Every packet that the network layer of any node receives from the link layer is sent up to the transport layer of that node
	- False
- Which of the following is not a goal of a routing algorithm
	- Modularity
- When using shortest path routing, the shortest path is calculated and stored in a **routing table**
- Dijkstra's algorithm finds the shortest path between **a given** source node(s) and **all** destination nodes within a network 
- Elements written in blue front represented 
	- Nodes that have been finalized
	- Nodes to which the shortest distance from the source node has been found 
- In any given iteration, nodes to which distances from the source nodes are as yet unknown are indicated using the value **infinity**.
- In every iteration, the node **with the shortest known distance from the source node** is chosen for exploration next

12-2
 - The common protocol in the **network** layer that all nodes understand is called the **Internet** Protocol
 - The Internet Protocol (IP) does not provide any **reliability** guarantees and so it is known as the **best** **effort** service
 - In Internet Protocol Version 4 protocol an IPv4 header is added to all network layer **packets** before sending them down to the **link layer**.
 - The **identification** field in the header provides a way recombine a packet that has been split into multiple **fragments**
 - If a packet has the "do not fragment" flag set and cannot move nay further becaues it is too large, it will be **dropped**.
 - IPv6 supports a **larger** address than IPv4 and has a **simpler** header than IPv4
 - Congestion is when the network gets **flooded** with more **packets** that it can handle
 - In traffic-aware **routing**, we consider the current **load** and direct traffic away from hotspots
 - In traffic **throttling**, routers track the network state and determine when **congestion** will occur
 - Load **shedding** is when routers drop packets when congestion is too high