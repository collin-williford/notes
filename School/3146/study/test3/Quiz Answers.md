Module 7-1
- All of the memory resources needed by a process are referred to as **process** **data**. For a process to be able to execute, its data must be in **main** **memory** 
- A mechanism that can be used to allow multiple processes to reside in memory simultaneously is memory **memory partitioning**.
- When using static equal sized partitions, a given process is **always mapped to the same physical partition**.
- An advantage of static equal sized partition scheme is its **simplicity**. A disadvantage is that it suffers from **internal** fragmentation.
- In a scheme with static unequal sized partitions, the system needs to store the **base** address and the **limit** in order to enforce protection.
- A scheme that allows dynamic partitions of varying sizes starts with unpartitioned memory, called **free space**, and then creates partitions dynamically based on process needs. 
- A possible **mechanism** to keep track of free  spaces is to use a linked list 
- In the first approach, the system chooses the **first** free space that is **large** enough to fit the process being placed. 
- Both the best fit and the worse fit approaches require traversal of the entire free space list. 
	- True
- In general programs issue **logical or relative** addresses and not **physical or absolute** addresses

8-1
 - Compaction is an option to reduce **external** fragmentation of main memory. The disadvantage of this approach is that it is **expensive** to keep doing it every now and then. 
 - Paging is a **mechanism** that allows a process to be split into multiple parts and allocated to multiple partitions. Here, the main memory is divided into equal sized blocks called **page frames** and the logical address space of a process is divided into blocks of the same size called **pages** 
 - Logical pages of a given process must always be allocated to contiguous page frames in the physical main memory. 
	 - False
- To keep track of what logical page of which process maps to what physical page frame in the main memory, the Operating Systems use structures called **page tables**.
- In a paged system, the logical address issued by a process includes two parts, namely, the logical **page** number and the **offset** within it. Similarly, the physical address includes the physical **page frame** number and the **offset** within it. 
- The operating system is responsible for translating the logical address issued by a process into a physical address. While doing so, it can retain the **offset** as it is. To speed up access to page table entries, systems typically store frequently used page table entries in a special cache called the **Translation look-aside** buffer. 
- A process may not use all of its data all the time. An approach in which pages may be brought into the main memory as needed is called **demand paging**. When using this approach, if a process request for data on some page and that page is not in the main memory yet, a **page fault** is said to occur. In a system using this approach, logical - also known as **virtual** addresses may be **longer** than physical addresses. 

8-2
 - Choose answers from each dropdown boxes below that will correctly complete the "algorithm" shown below for the Optimal page replaement policy. 
	 - If (newly requested page is already in main memory) 
		 - access is a hit
	- else 
		- access causes a page fault
		- identify page whose next access will be farthest in the future
		- replace identified page with newly requested page

- First In First Out page replacement policy algorithm
	- If (newly requested page is already in main memory) 
		- access is a hit
	- else 
		- access causes a page fault
		- identify page that was brought into main memory the longest time ago
		- replace identified page with newly requested page. 

- Second Chance page replacement policy 
	- If (newly requested page is already in the main memory)
		- access is a hit 
		- set reference bit to true
	- else 
		- access causes a page fault
		- do
			- identify page currently marked as the oldest page 
			- If (identified page has its reference bit set to true) 
				- mark identifed page as the newest page
				- set reference bit of identified page to false
				- mark the second oldest page as the oldest page 
			- else 
				- replace identified page with newly requested page
				- break out of loop

 - Least Recently Used page replacement policy 
	 - If (newly requested page is already in main memory) 
		 - access is a hit
	- else 
		- access causes a page fault
		- Identify page whose previous access was farthest in the past 
		- replace identified page with newly requested page


9-1
 - Data on a disk is organized as a sequence of equal-sized **blocks**.

 - The following characteristics of **non-volatile**, **long-term** storage:
	 - Must store very large amount of information 
	 - Must persist beyond process lifetime
	 - Must be accessible by multiple processes at once

 - What is one of the benefits of using contiguous allocation?
	 - Figuring out the location of a specific file block requires a very simple calculation 

 - When using a File Allocation Table that is loaded in memory, when is a disk access needed?
	 - To actually fetch a block after it has been located

 - Operating systems that use i-node file allocation typically impose a limit on:
	 - The number of files that a process can open at any given time and the total number of files that can be open at any given time on a system 

 - Match the given description with its corresponding access mode
	 - Read
		 - Grants the capability of view the contents of the file 
	- Write 
		- Grants the capability of modify or remove the content of the file 
	- Execute
		- User with execute permissions can run a file as a program 

 - When using absolute permissions, what number can be used to grant permissions to view and modify the contents of a file and also to run it if it is a program?
	 - 7

 - What is the Unix command to change file or directory permissions?
	 - chmod

 - What is the Unix command to change the owner or a file or directory?
	 - chown