 - Load-store architecture
	 - both operands and destination for an ADD operation must be in registers
- Register-memory architecture
	- one of the operands for the ADD operations may be in memory, while the other is in a register

Memory Wall Problem
 - Processor is faster than memory 
 - processor can execute instrucitons quickly, it spends a significant amout of time waiting for data to be transferred to and from memory 
 - Solution
	 - L-caches
		 - small but very fast
		 - static random-access memory (SRAM)
		 - 