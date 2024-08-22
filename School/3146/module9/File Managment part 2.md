 File allocation - contiguous
  - File blocks stored contiguously 
  - Pros
	  - Simple 
	  - Read is very fast 
	- ![](Pasted%20image%2020240311102909.png)
- Cons
	- Resuls in external fragmentation
		- Compaction or de-fragmetation very expensive
	- Max file size must be known 
	- ![](Pasted%20image%2020240311103144.png)

File allocation - linked list
 - File blocks form linked list 
 - Info about next block stored within disk block itself 
 - ![](Pasted%20image%2020240311103357.png)
 - Pros
	 -  no external fragmentation 
	 - File size can dynamically change 
- Cons
	- Could have internal fragmentation in last block 
	- Entire disk block not used for file content
	- To locate random block in file, several disk accesses needed
- Linked list info stored as table in main memory 
	- File allocation table (FAT)
	- Disk blocks entirely used for file content 
	- External pointers to first and possibly last blocks 
	- Each block points to next block (or special EOF value)
	- ![](Pasted%20image%2020240311112345.png)
	- Pro:
		- To locate random block within file, only memory accesses needed
	- Cons: 
		- Entire table must be in main memory 

File allocation  - i-node
 - Attributes and disk block addresses of file stored in data structure call i-node
 - When file opened, its i-node brought into main memory 
	 - I.e., only i-nodes of open files kept in main memory 
