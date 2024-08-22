Policies
 - We've looked at mechanism for page oriented management 
 - There are several polity questions to be considered
	 - Which page frame should new page be allocated to?
	 - Which page should be de-allocated/replaced if no free page frame available?
	 - Which page table entries should be placed in TLB?
- Which page frame should a new page be allocated to?
	- All page frames are of same size 
	- So, any empty page frame can be used for a new page 
- What if there are no empty frame?
	- Choose page to evict from main memory 
	- Write back page to be evicted to disk 
		- Only really needed if page has been modified since being loaded
		- Page table keeps track of whether page has been modified or not 
	- Allocate new page to the now free frame 
- Which page should be evicted?
	- This actually needs a well-defined page replacement policy!

Page replacement 
 - Let's use an example through this discussion
	 - Assume main memory with 3 page frames
	 - Assume program with following memory pattern 
		 - 7, 0, 1, 2, 0, 3, 0, 4, 2, 3
- We will no look at a few possible policies

![](Pasted%20image%2020240228172333.png)


Page replacement 
 - Ideally, evict page that won't be needed in near future
 - If memory reference patterns of processes known 
	 - Evict page that will not be used for longest time in future
	 - This is called optimal page replacement policy 
	 - ![](Pasted%20image%2020240228172346.png)
	 - ![](Pasted%20image%2020240228172355.png)
	 - ![](Pasted%20image%2020240228172405.png)
	 - ![](Pasted%20image%2020240228172422.png)
	 - ![](Pasted%20image%2020240228172506.png)
- Optimal, but impractical

Page replacement 
 - A simple option 
	 - Evict page that has been in main memory longest
	 - First in First out (FIFO)
	 - ![](Pasted%20image%2020240228172621.png)
	 - ![](Pasted%20image%2020240228172633.png)
	 - ![](Pasted%20image%2020240228172638.png)
	 - ![](Pasted%20image%2020240228172645.png)
	 - ![](Pasted%20image%2020240228172656.png)
	 - ![](Pasted%20image%2020240228172702.png)
	 - ![](Pasted%20image%2020240228172708.png)
	 - ![](Pasted%20image%2020240228172715.png)
	 - ![](Pasted%20image%2020240228172720.png)
- Provides fairness
- but doesn't really look at page usage

