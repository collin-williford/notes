Physical main memory size = 64KB = 2^16 bytes
Page frame size = 8KB = 2^13 bytes
Logical address space size = 2^16

Number of physical page frames = Physical main memory size / Page frame size 
2^(16-13) = 2^3

Number of bits needed to represent a physical page frame number in the system 
 = 3

Number of logical pages = Logical address space size / Page size
2^(16-13) = 2^3

number of bits needed to represent a logical page number for P?
 = 3

To find the logical page number 
logical address = 0x969C 
0x969C = 1001011010011100
Since the page size is 2^3 (8KB), we need the first 3 bits (since 2^3 = 8) = 100
100 = 0x4

corresponding physical frame number given by table is 
 = 0x 2

____________________________

main memory size: 1MB (2^20)
page frame size: 32KB (2^15)
Logical address space: 512KB (2^19)

Given the logical address of 0x 69656 what will be the logical page number issued by a process P?
logical address: 0x69656
01101001011001010110
page frame is 2^15 so take 15 off back = 01101
decimal 431702
01101 = 0x D

find Hexadecimal physical address
 - frame size is 2^15 so lower 15 bits of the logical address represent offset
	 - 001011001010110
- then add 0x15 because the table 0x D corresponded to 0x 15 physical frame 
	- 00010101 this is physical frame from table
	- 001011001010110 this is page offset (rear 15 bits)
	- dont add decimals just put physical frame in front of page offset
	-  = 00010101001011001010110
	- which is 0xA9656


431702 / 2^15 = 13 r 5718
offset within frame: 0x5718
offset within frame to decimal = 22296
0x 15 in decimal = 21
21 + 22296 = 22317
22317 to hex = 0x572D


_____________________________

physical main memory size: 32KB (2^15)
page frame size: 4KB (2^12)
System uses pure demand paging and that system supports up to 16-bit logical/virtual addresses
process P2 with logical address space of 64KB (2^16) executes on system 

![](Pasted%20image%2020240227214659.png)

How many page frames are there in the above pure demand paging memory system?
 - 2^3
How many bits are needed to represent a physical page frame number in the system?
 - 3

How many logical pages are there in process P2?
 - Number of logical pages = Logical address space size / Page size
 - 2^16 / 2^12 = 2^4 = 16

At any given time, what is the maximum number of entries in the page table of P2 that can have valid physical frame number?
 - 8
	 - Given that the system has 8 page frames, at any given time, only the pages that are currently resident in these frames would have valid physical frame numbers. 

Assume that P2 issues the logical address 0xA87A. What is the logical page number containted in the given logical address, in hex?
 - logical address = 0xA87A
	 - 0b 1010100001111010
	 - 1010
		 - 0x A
