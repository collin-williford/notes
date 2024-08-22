External Fragmentation 
 - Reduces memory utilization 
	 - Even if enough free memory exists to allocate new process
	 - Not useful since memory is not contiguous
- Possible approaches
	- Reduce external fragmentation using compaction 
	- Find way to allow non-contiguous partitions 
		- I.e., split process footprint into multiple parts

Compaction 
 - Move partitions to abut each other 
 - ![](Pasted%20image%2020240226142836.png)
- Needs partition relocation 
- ![](Pasted%20image%2020240226142906.png)

Allowing non-contiguous allocation 
  - ![](Pasted%20image%2020240226142938.png)
  - What is the base address?
  - What is them limit?
  - ![](Pasted%20image%2020240226143035.png)

What we need 
 - Is a more sophisticated memory management mechanism 
	 - Maintain information for multiple parts of process
- One such mechanism is paging 
- Divide physical memory into equal-sized blocks: page frames
- Divide logical memory into same sized blocks: pages
- Process pages mapped to physical page frames
- Page frames sizes are powers of 2
	- E.g., 4096 bytes, 8192 bytes 

Paging 
 - ![](Pasted%20image%2020240226143244.png)
 - Mapping of process pages could end up being contiguous
 - But it need bot be 
 - Depends on state of memory when process is allocated
 - And on policy used for allocation 
 - ![](Pasted%20image%2020240226143344.png)
 - OS maintains page to page frame mappings -> page tables 
 - ![](Pasted%20image%2020240226143428.png)

Paging 
 - OS keeps track of free page frames -> linked list
 - To allocate process that needs n pages 
	 - Find n free page frames; allocate process pages to frames 
- Internal fragmentation possible due to fixed-sized frames 
	- Manageable by carefully choosing size of page/page frame 

