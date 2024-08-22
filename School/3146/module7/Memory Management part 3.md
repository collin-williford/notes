 Dynamic, variable-sized partitions
 - Basic idea
	 - Start with un-partitioned memory (a.k.a. "free space")
	 - Create partitions dynamically based on process data size 
		 - Number of partitions changes dynamically 
		 - Lenghts of partitions may be different 
- Place initial partitions contigously in main memory 
- ![](Pasted%20image%2020240219204727.png)
- ![](Pasted%20image%2020240219204744.png)
- ![](Pasted%20image%2020240219204755.png)
- ![](Pasted%20image%2020240219204810.png)
- ![](Pasted%20image%2020240219204825.png)
- ![](Pasted%20image%2020240219204846.png)
- ![](Pasted%20image%2020240219204903.png)
- ![](Pasted%20image%2020240219204930.png)
- ![](Pasted%20image%2020240219204946.png)
- ![](Pasted%20image%2020240219205001.png)
- As processes get swapped in and out of main memory 
	- Memory ends up with "free spaces" / "holes" between partitions 

Consequences
 - Need mechanism to keep track of free spaces
 - Need policy for partition placement 

Possible mechanism to keep track of free spaces
 - Maintain linked list of free spaces
 - Each list element stores base address and size of free space 
 - ![](Pasted%20image%2020240219205151.png)

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

First Fit 
![](Pasted%20image%2020240219211109.png)

Best Fit 
![](Pasted%20image%2020240219211126.png)

Discussion 
 - Pros
	 - More flexible than static partitioning 
- Cons 
	- Management more complex than with static partitioning 
	- Has external fragmentation (extent varies with policy) 

Now consider this
 - How should a program specify memory addresses?
	 - Absolute addresses?
	 - Definitely not for dynamic partitioning
	 - Probably not even for static partitioning -> loses portability 

In practice 
  - Program uses offsets relative to start address of 0
	  - I.e., program uses logical address
	  - Range of logical addresses for process: logical address space 
- System translates relative offset into absolute address
	- I.e., system generates physical address
	- Range of absolute address of process: physical address space 
- Translation mechanism 
	- Maintain base address and limit for process partition 
	- Add base address to logical address issued by program
	- Check whether result is within limit 

Consequence of relative addressing 
 - Process need not be mapped to same physical partition all the time...
 - ... partition relocation is possible 
 - Very useful, espically when using dynamic partitioning 