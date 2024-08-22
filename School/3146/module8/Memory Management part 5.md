 Address translate in paged systems 
 - Logical address includes two parts 
	 - Page number (pn)
	 - Offset within page (off)
- Physical address includes corresponding parts
	- Page frame number (fn)
	- Offset within frame (off) 
- ![](Pasted%20image%2020240226144631.png)
- ![](Pasted%20image%2020240226144645.png)

In a computer 
 - Addresses representd in binary 
	 - Main memory and page frames sizes are powers of 2 
	 - hexadecimal -> more compact
- Knowledge of number system and conversions needed
- Binary -> bit values 0 and 1 
	- 2 bits:
		- 4(2^2) combinations (00, 01, 10, 11)
	- 3 bits:
		- 8 (2^3) combinations (000, 001, 010, 011, 100, 101, 110, 111)
	- n bits:
		- 2^n combinations 

Memory System 
 - 32KB (2^15) main memory 
	 - 15 bit physical address
- 16KB (2^14) logical addres space 
	- 14 bit logical address
- 4KB (2^12) page frame / page
	- 12 bit offset \[LSB]
	- 2^15 / 2^12 = 2^3 page frames 
		- 3 bit page frame number
	- 2^14 / 2^12 = 2^2 pages
		- 2 bit logical page numbers 

Address translation in paged systems 
 - ![](Pasted%20image%2020240226145217.png)

Page table entry structure
 - Structure is dependent on system 
 - Let's look at one possible structure 
 - ![](Pasted%20image%2020240226145349.png)

More about paging 
 - Page table itself stored in main memory 
	 - Expensive to access it for each memory request 
- Solution 
	- cache subset of page table entries 
- Translation look-aside buffer (TLB) 
	- Small set of associate registers
	- Provides fast access 

Address translation with TLB
 - ![](Pasted%20image%2020240226150110.png)

We still have one restrictive assumption 
 - All process pages must be in main memory to execute process 
	 - Limits num processes in main memory and process data size 
- Observation 
	- Process does not ues all its data all the time 
- Better option 
	- Keep only subset of process pages in main memory 
	- Bring others as needed 
	- This is called demand paging 

Demand paging
 - When process requests for data
	 - Check if page with data already in main memory 
	 - If yes, proceed as usual 
	 - If not, page fault is set to occur
- When page fault occurs
	- Load missing page into main memory 
		- May add TLB entry for new page
	- Restart instructure that caused page fault 

A consequence of demand paging 
 - Process data not limited to physical main memory size
	 - I.e., size of process virtually unlimited
- This is referred to as virtual memory 
	- Did not support this in our earlier example
- What can we do?
	- Allow more logical pages in process than physical page frames
	- Logical page number can be longer than physical page frame number
	- Logical (virtual) address can be longer than physical address 
