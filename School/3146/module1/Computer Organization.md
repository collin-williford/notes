Main Components of a PC 
 - Processor
	 - Central Processing Unit (CPU)
		 - Brain (computation center)
	- Capable of executing specific set of instructions
		- Instructions have pre-determined codes
	- Instructions may have input/output data
 - Memory and storage
	 - Used to store instructions and data
	 - Permanent (non-volatile)
		 - Retains data permanently
		 - Read Only Memory (ROM)
			 - Name misleading  - some ROMs can be modified
		- Read/Write Memory (disks)
	- Temporary (volatile) 
		- Random Access Memory (RAM)
			- Static RAM (SRAM)
				- Retains value indefinitely as long as power is on 
			- Dynamic RAM (DRAM)
				- Values must be refressed every 10-100ms
	- Comparision
		- Disk
			- Defidenly need this for permanent storage
			- Cheap, large storage possible 
			- Slow, bottleneck because CPUs are fast
		- DRAM
			- More expensive, relatively small storage
			- Faster, but still not fast enough
		- SRAM
			- Fast
			- Expensive, very small storage possible 
	- Magnetic Disk 
		- Very cheap, very large, non-volatile storage
		- Mechanical device -> random access of data is very slow 
		- Set of rotating metal platters
		- Mechanical arms with read/write heads to access data
		- Organized into tracks & sectors
	- Main Memory 
		- Smaller volatile memory closer to CPU
		- Collection of cells (1-bit each) organized into sets called supercells
		- Each supercell has unique address used to read/write data
		- Logically organized and handled in lines/blocks of supercells
	- Cache
		- Small, fast memory for frequently used data
			- Organized into lines/blocks of data similar to main memory 
			- Works on principle of locality of reference (temporal/spatial)
		- When the CPU requests for data 
			- If line containing data is already in cache -> cache hit 
			- If line containing data not in cache -> cache miss
				- Fetch line containing data from next level in memory hierarchy 
				- (typically) put line into current level of cache 
		- System may have multiple levels of cache 
			- Cache levels are typically inclusive 
	- Registers
		- Very small, very fast memory in CPU itself 
		- Special registers
			- Program counter (PC)
			- Stack Pointer (SP)
				- Stores address of top of stack 
				- Stack -> area of memory containing data for procedures (funcitons) that have started, but not completed
			- Program status word (PSW)
				- Stores bits relevent to current state of system 
- Instruction Execution 
	- General Sequence of operations 
		- Retrieve next instruction from memory (fetch)
			- Program Counter (PC) has address of instruction to fetch 
		- Figure out what type of instruction it is (decode)
			- Each type of instruction has a specific format
		- Fetch data - if needed - from memory 
		- Execute instruction
		- Store results
		- Update PC to store address of next instruction
 - Precieved Performance is important 
	 - Process one instruction fully, then next -> simple, but slow 
	 - Split instruction execution sequence into stages
	 - Multiple instructinos can make progress concurrently 
	 - This idea is known as pipelining -> similar to assembly line 

I/O devices 
 - Monitor, Keyboard, (disk), printer
 - Physical device operation is very complex
	 - Each device has controller h/w that directly interacts with it 
	 - Controller provides simpler interface to device
- CPU - I/O device interation
	- CPU and I/O devices work asynchronously
	- Need a way for CPU to know when device 
		- Has input data to give to CPU
		- Is ready to recieve commands or output data from CPU 
		- Has completed command issued by CPU 
- Modes of I/O operation 
	- One option
		- CPU stops current activity 
		- CPU asks if device is ready 
			- Device has new input
			- Device is done with prevous command/output
		- If yea, CPU servies device
		- CPU moves to next device 
		- Once done, CPU resumes prevously stopped activity 
		- CPU repeats above steps periodically
	- This concept is known as polling 
	-  Another option 
		- CPU sends commands/data to device
		- CPU goes back to other activity
		- Device signals completion to CPU using interrupt 
			- Interrput
				- External event that causes change in flow of current execution 
				- Sequence of activities
					- CPU executing instructions
					- Interrupt received 
					- CPU
						- Finishes current instruction
						- Recognizes interrupt
						- Saves current state
						- Services interrput
						- Resumes normal activity 
				- Handling code in special function called interrupt handler
				- Interrupt handler services interrupt
				- Different handlers for different types of interrupts
				- Handler may trigger another function for extended service 
	- Direct Memory Access (DMA)
		- CPU initiates data transfer
		- Transfer coordinated by special DMA hardware 
		- Interrupt generated upon completion 