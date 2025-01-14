Question 1: All correct 

Starting IP: 198.16.32.0
A: 1000
B: 3000
C: 2000
D: 4500

Org A:
 - Start IP: 198.16.32.0
 - 1000 addresses
 - 2^10 = 1024
	 - Subnet mask /22
	 - 198.16.32.0/22
- Last IP
	- 198.16.32.0 to binary 
	- 11000110 00010000 00100000 00000000
	- Set last 10 bits to 1
		- 11000110 00010000 00100011 11111111
		- Convert to decimal 
			- 198.16.35.255
			- Last IP address 

Org B:
 - Start IP 
	 - ~~198.16.36.0~~
	 - 198.16.48.0 run into collision so this is first 
- Subnet Rep
	- require 3000 addresses
	- 2^12 = 4096
	- 198.16.48.0/20
- Last IP 
	- IP to binary 
	- 198.16.36.0
	- 11000110 00010000 00100100 00000000
	- change last 12 bits to 1's 
		- Collision 
		- because the 11th digit is a 1 we have to shift the network section 
		- 11000110 00010000 00100100 00000000
		- remove the last 12
		- 11000110 00010000 0010
		- then add 1 
		- 11000110 00010000 00110000 00000000
			- now this is 198.16.48.0 (this is first address now )
			- now change last 12 bits to 1's
			- 11000110 00010000 00111111 11111111
			- 198.16.63.255 (this is last address) 

Org C:
 - First IP 
	 - 198.16.64.0
- Subnet
	- need 2000 addresses
	- 2^11 = 2048
	- 198.16.64.0/21
- Last IP
	- IP to binary
	- 198.16.64.0
	- 11000110 00010000 01000000 00000000
	- last 11 bits to 1's
	- 11000110 00010000 01000111 11111111
	- 198.16.71.255

Org D:
 - First IP 
	 - ~~198.16.72.0~~
	 - 198.16.96.0
- Subnet
	- need 4500 addresses
	- 2^13 = 8192
	- ~~198.16.72.0/19~~
	- 198.16.96.0/19
- Last IP
	- IP to binary 
	- 198.16.72.0
	- 11000110 00010000 01001000 00000000
	- last 13 to 1's 
		- Collision 
		- remove last 13
		- 11000110 00010000 010
		- add 1
			- 11000110 00010000 01100000 00000000
			- 198.16.96.0
			- chanage last 13 bits to 1;s
			- 11000110 00010000 01111111 11111111
				- 198.16.127.255