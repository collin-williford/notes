 - What does the network layer do?
	 - Goal: Transfer packets between endpoints via multiple links
	 - Routing and Forwarding
		 - Find path for source to destination 
		 - Forward packets along path 
	- Congestion control 
		- Must avoid/recover from network congestion 
	- Internetworking
		- Must support joining of multiple networks into network of networks 
		- Must provide uniform addressing across entire network of networks 
		- Details of physical network, number/types of nodes and network topology, etc. must be hidden from transport layer

Routing Basics
 - Routing -> identifying path between endpoints
 - What happens along path?
	 - Store-and-forward packet switching 
		 - Wait for full frame to arrive and link layer to verify frame 
		 - Forwards packet to next router along identified router
		 - When destinationi reached, send packet up to transport layer

Routing Goals
 - Could have multiple possible routes between A and B 
	 - Need to make appropriate choice 
- Goals of routing algorithm 
	- Should deliver packets to their intended destination 
	- Should have low overhead (simplicity)
	- Should be efficient (minimize delay, maximize throughput)
	- Should cope with changes in topology and traffic (robustness)
	- Should not take forever to conberge to choice (stability)
	- Should not treat different nodes fairly 

Types of routing algorithms
 - Non-adaptive or static 
	 - Routes fixed offline and simply stored in tables
	 - Makes sense if there's only one clear choice 
- Adaptive or dynamic 
	- Routes changed to reflect changes in network state
		- E.g., topology, traffic changes
	- Have some optimization criteria

Routing algorithm examples 
 - Shortest path routing 
 - Flooding 
 - Distance vector routing 
 - Link state routing 
 - Hierarchical routing 
 - 