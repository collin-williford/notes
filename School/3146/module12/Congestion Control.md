 - Responsibility shared by transport and network layers
	 - We discuss network layers aspects here
- Several approaches could be taken to handle congestion 
	- Let routing algorithm handle it (traffic-aware routing)
	- Decrease traffic/load
	- Increase capacity
		- Add more resources to network (provisioning)
		- More of a long-term solution 

Traffic-aware routing 
 - Goal
	 - consider load and direct traffic away from hotspots 
- Choose routes depending on traffic, not just topology
- ![](Pasted%20image%2020240402151847.png)
	- I.e., use EI for West-to-East traffic if CF is loaded
- Could lead to oscillations in routing tables
	- Just routing all traffic in another direction could cause that new direction to get overloaded
- Solutions to oscillation problem 
	- Change routes slowly, not all at once
		- Use external traffic engineering to decide on weights
	- Use multiple paths at once 
		- I.e., distribute traffic over links (e.g. ,use both CF and EI)

Traffic throttling
 - Routers determie when congestion is impending 
 - Routers notify senders of impending ongestion 
 - Some approaches 
	 - Send choke packet to senders causing congestion 
		 - Sender required to reduce rate of transmission 
	- Set flag in packets notifying impeading congestion
		- Explicit congestion notificaiton (ECN)
- ![](Pasted%20image%2020240402152258.png)

Admission Control
 - Useful in connection-oriented service
 - Refuse new connection (virtual circuit) if network can handle it without being congested
 - How do you know if new connection will cause congestion?
	 - Need some way to represent traffic state
	 - Approaches include leaky bucket

And if nothing else works
 - Routers resort to loading shedding
 - I.e., routers simple drop packets when inundated
 - Which packets should be dropped?
	 - Depends
	 - File transfer -> old packet worth more than new one 
	 - Real-time streaming -> new packet worth more than old one