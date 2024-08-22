Assume that a large number of consecutive IP addresses are available starting at 198.16.0.0 and suppose that four organizations, A, B, C and D request 4000, 2000, 4000, and 8000 addresses, respectively, in that order. For each of these, give the first possible IP address within the assigned subnet, the last possible IP address within the assigned subnet, and the subnet representation in slash notation.

Organization A:
 - Requires 4000 addresses
	 - closes power of 2 greater than 4000 is 2^12, which is 4096
	 - The subnet mask for 2^12 is /20
	 - 198.16.0.0/20
	 - Subnet size: 2^(32-20) - 2= 2^11 - 2 = 4096
- First IP address
	- 198.16.0.0
- Last IP address
	- set all host bits to 1 within the subnet. In this case, the last 12 bits will all be 1's
	- 198.16.0.0 in binary 
		- 11000110 00010000 00000000 00000000
	- 11000110 00010000 00001111 11111111
		- Now convert this to decimal 
		- 198.16.15.255
		- This is last IP address
- Subnet representation 
	- 198.16.0.0/20

Organization B:
 - Requires 2000 addresses
	 - Closes power of 2 is 2^11 = 2048
	 - The subnet mask for 2^11 is /21
	 - Subnet size: 2^(32-21) - 2 = 2^11 - 2 = 2046
- First IP address
	- One after A's last IP address range
	- 198.16.16.0
- Last IP address
	- set last 11 bits to 1's
	- 198.16.16.0
		- 11000110 00010000 00010000 00000000
		- 11000110 00010000 00010111 11111111
			- 198.16.23.255
- Subnet representation
	- 198.16.16.0/21

Organization C
 - 4000 addresses
	 - 2^12 = 4096
	 - subnet mask is /20
 - First Address
	 - 198.16.24.0
- Last Address
	- set last 12 bits to 1's
	- 198.16.24.0
		- 11000110 00010000 00011000 00000000
		- 11000110 00010000 00011111 11111111
			- 198.16.31.255
			- its not this 
		- 11000110 00010000 00100111 11111111
			- 198.16.39.255
			- its this
			- 198.16.24.0 + 4094 = 198.16.24.0 + 0.0.15.255 = 198.16.39.255
- Subnet representation
	- 198.16.24.0/20

Organization D
 - 8000 addresses
	 - 2^13 = 8192
	 - /19
- First address
	- 198.16.40.0
- last address
	- set last 13 bits to 1's
	- 198.16.40.0
		- 11000110 00010000 00101000 00000000
		- 11000110 00010000 00111111 11111111
			- 198.16.63.255
- subnet rep
	- 198.16.40.0/19


hex address 0xD31EC251 to dotted decimal notation 
 - D3
	 - 211
- 1E
	- 30
- C2
	- 194
- 51
	- 81
So its 
 - 211.30.194.81


Wha tis the subnet mask in binary that will be used by the router to extract the prefix bits?
 - Given 
	 - 145.18.157.19/24
	 - for subnet mask we need to convert last 8 bits to 0's
		 - 11111111 11111111 11111111 00000000
		 - 11111111 11111111 11111111 00000000


IP address: 194.24.7.126
in binary: 11000010 00011000 00000111 01111110
subnet mask 255.255.248.0 
 - in binary: 11111111 11111111 11111000 00000000
Perform bitwise AND operation between ip address and subnet mask 
 - 11000010 00011000 00000111 01111110
 - 11111111 11111111 11111000 00000000
	 - 11000010 00011000 00000000 00000000
		 - This address is : 194.24.0.0
		 - So this address matches teh Cambridge location 

address: 194.24.15.80

 - Try subnet mask: 255.255.252.0
	 - 11111111 11111111 11111100 00000000
- Address is:
	- 11000010 00011000 00001111 01010000
- Bitwise AND
	- 11000010 00011000 00001100 00000000
	- This address is
		- 194.24.12.0



Organization C
 - 4000 addresses
	 - 2^12 = 4096
	 - subnet mask is /20
 - First Address
	 - 198.16.32.0
		 - Explain this in last address
- Last Address
	- set last 12 bits to 1's
	- 198.16.24.0
		- 11000110 00010000 00011000 00000000
		- because the 12th digit is a 1 we have to shift the network-bit section 
			- 11000110 00010000 00011000 00000000
				- remove the last 12 
					- 11000110 00010000 0001
					- then add 1
						- 11000110 00010000 00100000 00000000
						- this is now 198.16.32.0
							- Now change the last 12 bits to 1's
								- 11000110 00010000 00101111 11111111
									- 198.16.47.255
					
- Subnet representation
	- 198.16.32.0/20

Organization D
 - 8000 addresses
	 - 2^13 = 8192
	 - /19
- First address
	- Try 198.16.48.0
		- 11000110 00010000 00110000 00000000
			- Changing last 13 bits will run into collision 
			- increment network-bit section 
				- 11000110 00010000 01000000 00000000
					- 198.16.64.0
- last address
	- set last 13 bits to 1's
	- 198.16.64.0
		- 11000110 00010000 01000000 00000000
		- 11000110 00010000 01011111 11111111
			- 198.16.95.255
- subnet rep
	- 198.16.64.0/19