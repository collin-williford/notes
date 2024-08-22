IP address
 - Defining feature of IP is an IP address
	 - IPv4 -> 32 bits
- IP address uniquely identifies a network interface
	- Host typically has one network interface, so one IP address
	- Routers have multiple interfaces, so multiple IP addresses
- IPv4 dotted decimal notation 
	- Four 8-bit numbers (octets) separated by dots
	- 10101100 00010000 00000000 01100100 -> 172.16.0.100
- Can be public or private
	- Public 
		- Valid destination on Internet
		- Globally known 
	- Private 
		- Can be used freely within just private networks
			- E.g., home, small company, etc.
		- Still need public IP address to connect to Internet 
			- Will need NAT to translate private to public IP addresses
- Public IP addresses are allocated and managed hierarchically 
	- IANA delegates blocks of addresses to regional authorities (RIR)
	- ISPs/organizations get blocks of addresses from RIRs
	- ISPs/organizations assign addresses to customers/computers

IPv6 addresses
 - Future of the Internet Protocol 
	 - 128-bit addresses
- IPv6 notation
	- 8 groups of 4 hexadecimal digits each separate by colons 
		- 2001:0DB8:0000:0000:0000:ff00:0042:8329
	- Can omit leading zeros in any group 
		- 2001:DB8:0:0:0:ff00:42:8329
	- Can omit groups of zeros altogether
		- 2001:DB8::ff00:42:8329

Issue is 
 - Wide-scale deployment of IPv6
 - IPv6 will have to co-exits with IPv4 for several more years
	 - Communication between computers with IPv4 and IPv6 addresses
- Some approaches have been proposed 