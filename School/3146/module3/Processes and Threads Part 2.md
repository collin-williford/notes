Process creation
 - Traditionally, OS transparently created all processes
 - Modern OSs provide system call for process creation
 - First process (ex: init in Unix) created at boot time
	 - This process creates other processes at start up & later as needed
- Other processes can also create new processes as needed

Process creation steps
 - Assign unique identifier to new process
 - Allocate and set up memory space for process (process memory image)
	 - Process control block (PCB)
	 - Program and data -> organized into regions
		 - Code/text space
		 - Global data space
		 - Heap (dynamically allocated data) space
		 - Stack (local function data) space
- Set up memory management structures for process
- Other structures OS may keep for performace monitoring, etc.

Process creation mechanisms
 - 1st option -> Cloning
	 - Process spawns process that is a copy of itself
		 - Adopted by Unix based OSs -> fork() system call
- 2nd option -> Creation from scratch
	- Process creates new process with appropriate parameters
		- Adopted by Windows -> CreateProcess() system call

Unix process creation (fork)
 - Process invokes fork to initiate creation of new process
 - Creating process is parent & new process is child
 - System call creates new process
 - Data from parent process copied to memory of child process
	 - Memory image, enviroment settings, I/O handles, etc
	 - Of course, child gets its own ID, scheduling info, etc
- fork call returns a value
	- Upon success, fork returns child ID to parent process and returns 0 to child process
- Parent/child processes independently continue execution from statement after fork
- If process spawn fails, fork returns -1 to parent & no child is created

In other words
 - return value to enable conditional execution after fork 
	 - So, even though program is same, paths can be differnt
	 - Different behavior can thus be achieved in parent & child

Alternatively
 - Child can change the program it executes
	 - Invoke exec family of system calls to change its memory image
	 - Stops executing code in parent program & starts new program

Since cloning requires copying
 - it has high overhead
 - Overhead somewhat reduced using copy to write concept
	 - Start with both parent and child sharing same memory
	 - Make copy if and when either process modifies data
		 - So, if child changes memory image, copy need never be made

Process termination 
 - As discussed earlier, process may terminate for many reasons
	 - Voluntary exit upon task completion
	 - Voluntary exit due to fatal error
	 - Involuntary exit due to error/bug
	 - involuntary exit due to kill command by OS or other process
		 - Of course, killer process must have appropriate authorization

On Unix based systems
 - OS maintains notion of process hierarchy
	 - A process, its children, their children, etc. (i.e. all descendants) form process group
- Parent must be allowed to ready child's exit status
- If parent terminates before child
	- Child is now an orphan process
	- Orphan processes are adopted by init process
- If a child process terminates before parent 
	- System will still need to keep child's PCB
	- Child process becomes a zombie process
		- "Dead", but not "reaped"
	- Parent process can reap children by waiting for them to terminate
		- OS provides system call for this -> wait

While processes are alive
 - This must be appropriately managed by OS
 - Multiple processes may be concurrent 
	 - Big part of management is switching between processes
- OS needs to have access to PCBs of processes 
	- Maintains process table to hold PCBs
- Questions that arise
	- When does OS switch to different process?
	- Which process does OS switch to?
	- How does OS perform process switch?

Process switching/context switching
 - Example scenarios that may trigger process switch
	 - Process termination (voluntary/involuntary)
	 - New process activation 
	 - Executing process gets blocked (e.g., due to system call)
	 - Event completion 
	 - Time slice expiration
- Process switching mechanism needs hardware and OS support
	- Require transition to kernel mode -> uses interrupt
	- Overhead of switch depends on hardware support 
	- ![](Pasted%20image%2020240123133845.png)

Typical Steps
 - (hw) Save program counters and some registers on stack
 - (hw) Load program counter specifed in interrupt vector
	 - Interrupt vector -> has address of interrupt service routine
- (asm) Save context info (registers, etc.) in PCB of curr process
- (asm) Set up new stack
- (C) Remaining work for specific interrupt type 
- (C-sched) Choose new process to be scheduled
- (asm) Restore context info for new process and start it 
