Static, unequal-sized partitions 
 - Statically create partitions of different sizes
 - Map each process to a partition that's large enough for it 
	 - For now, assume mapping does not change
	 - ![](Pasted%20image%2020240219153545.png)
	 - ![](Pasted%20image%2020240219153619.png)
	 - ![](Pasted%20image%2020240219153633.png)
	 - ![](Pasted%20image%2020240219153645.png)
	 - ![](Pasted%20image%2020240219153657.png)
- As before, this can be combined with swapping 
- ![](Pasted%20image%2020240219153728.png)
- ![](Pasted%20image%2020240219204122.png)

Protection 
 - Store base address (BA) + limit for each process' partition 
 - Check every address issued by process 
	 - Must lie between BA and (BA + limit)

Discussion 
 - Pros
	 - Supports processes of different sizes better
	 - Less internal fragmentation 
- Cons
	- Slightly more complex than equal-sized partitions
		- Needs policy for mapping processes to partitions (partition placement) 
		- Needs slightly enhanced protection mechanism 
	- Needs partition to be created statically 
		- Chosen sizes may not suit processes that may need to be supported 
	- Still can't support processes larger than largest partition 