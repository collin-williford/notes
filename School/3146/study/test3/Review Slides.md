Test Contnet
 - Memory Management 
	 - Partitioning
	 - Paging
	 - Page Replacement
- File Management
	- System Commands

Partitioning - Static Equal-Sized 
 - Memory must be divided up int multiple parts
 - Map each process to one partition 
	 - May be gaps within each paritions 
		 - Internal Fragmentation 
 - We can divide memory into partitions and allocate processes to these partitions 

Partitioning - Static Unequal-Sized 
 - Same as previous, but different sizes which will cause less internal fragmentation 
 - Statically create partitions of different sizes
 - Map each process to a partition that's large enough for it 
	 - Less internal fragmentation 

Partitioning - Dynamic, Variable-Sized
 - Start with unpartitioned memory 
 - Add processes to memory as needed
	 - Place initial partition contiguously in main memory 
	 - As processes get swapped in and out of main memory 
		 - Memory ends up with free spaces / holes between partitions 

Consequences of Dynamic, Variable-sized
 - Need to keep track of free spaces in memory 
 - Possible mechanism to keep track of free spaces
	 - Maintain linked list of free spaces 
	 - Each list element stores base address and size of free space 
- Need a policy to select which free space to allocate to 

Policies for partition placement 
 - First fit (FF)
	 - Scan list, choose first free space large enough for partition 
	 - Pros: 
		 - simple, fast
	 - Cons
		 - Partitions may crowd initial regions of main memory 
- Next fit (NF)
	- Similar to first fit 
		- Scanning starts where previous scan ended 
	- Pros:
		- More distrubuted allocation 
- Best fit (BF)
	- Scan entire list
	- Choose smallest free space large enough 
	- Cons:
		- Slow, leaves many small unusable free space 
- Worst fit (WF)
	- Scan entire list
	- Choose largest free space that fits process 
		- Pros:
			- Leaves larger free spaces
		- Cons
			- Slow 




