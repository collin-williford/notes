Shortest Path Routing 
 - Route packets along shortest path between src and dst
 - Shortest path calculated and stored in routing table
 - Shortest path could mean 
	 - Lowest number of hops
	 - Shortest geographic distance 
	 - Lowest average delay (fastest path)
- Can assign lables using weighted "distance"

Djkstra's Algorithm
 - Find shortest path between given src and all other nodes in network 
 - ![](Pasted%20image%2020240401174232.png)
- ![](Pasted%20image%2020240401174300.png)

Hierarchical routing 
 - As network size increases, routing tables get very large
 - Set up hiearchy among routers
	 - Form regions
	 - Each router knows details of its own region 
	 - Designated routers to get outside region 
- Concept can be extended to multiple levels of hierarchy
	- Region, cluster, zone

When are routing decisions made?
 - Connectionless service (widely used)
	 - Routing decisions made independently for every packet 
	 - Subsequent packets may or may not take same route
- Connection-oriented service 
	- Routing decision made during connection establishment 
	- Same route used for all packets on same connection 