Polices for partition placement 
 - First fit (FF)
	 - Scan list, choose first free space large enough for partition 
	 - Pros
		 - Simple 
		 - fast
	- Cons 
		- Partitions may crowd initial regions of main memory 
- Next fit (NF)
	- Similar to first fit; scanning starts where previous scan ended 
	- Pros
		- more distrubuted allocation 
- Best fit (BF)
	- Scan entire list; choose smallest free space large enough 
	- Cons
		- Slow 
		- leaves many small unusable free spaces 
- Worst fit (WF)
	- Scan entire list; choose largest free space that fits process
	- Pros
		- Leaves larger free space
	- Cons 
		- Slow 




**1. Internal Fragmentation:**   
Internal fragmentation happens when the memory is split into mounted-sized blocks. Whenever a method is requested for the memory, the mounted-sized block is allotted to the method. In the case where the memory allotted to the method is somewhat larger than the memory requested, then the difference between allotted and requested memory is called internal fragmentation. We fixed the sizes of the memory blocks, which has caused this issue. If we use dynamic partitioning to allot space to the process, this issue can be solved.




**2. External Fragmentation:**   
External fragmentation happens when there’s a sufficient quantity of area within the memory to satisfy the memory request of a method. However, the process’s memory request cannot be fulfilled because the memory offered is in a non-contiguous manner. Whether you apply a first-fit or best-fit memory allocation strategy it’ll cause [external fragmentation](https://www.geeksforgeeks.org/what-is-fragmentation-in-operating-system/).