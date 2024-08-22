 What does the Application layer do?
  - Provides services to user
	  - Domain Name System (DNS)
	  - File Transfer Protocol (FTP)
	  - Simple Mail Transfer Protocol (SMTP)
	  - Hypertext Transfer Protocol (HTTP)

Domain Name System (DNS)
 - Support service for several protocols
 - Names are easier for humans to remember than IP addresses
 - Names help with portability even when IP address changes 
 - DNS resolves human-readable names to IP addresses
 - Supports hierarchical, domain-based naming system
 - ![](Pasted%20image%2020240422164515.png)
 - Name servers -> contain data for portions of name space called zones 
 - ![](Pasted%20image%2020240422164605.png)
 - Findings IP address for given hostname -> resolution
	 - Computer requests local name server to resolve
	 - Local name server asks root name server
	 - Root returns name server for lower zone
	 - Continue down zones until name server can answer
- Example
	- ![](Pasted%20image%2020240422164716.png)
	- 