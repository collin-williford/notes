 - Computer system essentially used to execute/run programs
	 - May run several different programs
		 - Ex: email client, browser, editor, music player
- May run multiple instances of same program
	- Ex: Multiple instances of browser, editor
- Need some way to represent running programs internally 

Process
 - Abstraction for running program instance
	 - Represents an activity of some kind - hence the name!
	 - Used by OS to manage concurrently running programs
- A process is not equivalent to a program
	- TextEdit -> program
	- Running instance of TextEdit -> process
- More to process than just a program
	- Has program, data, state information
	- Owns resources (memory)

Program Execution
 - To execute a program, corresponding process must be created
	 - All processes can be created when system starts 
		 - Okay for embedded system like a dish washer
		 - Not so great for general purpose personal computer
	- Of course, some proceses are created when system starts
	- Others are created as requested/needed by user/system
- After creation, process becomes active or ready for execution 
![](Pasted%20image%2020240122144551.png)

Program Execution 
 - If processor is free, ready process can be dispatched/scheduled
 - ![](Pasted%20image%2020240122144636.png)
 - Process may sometimes have to wait for event (ex: I/O)
	 - Process gets blocked

Program Execution 
 - Once event being waited for occurs, process is ready again 
	 - This ready - running - waiting cycle can repeat
	 - ![](Pasted%20image%2020240122161836.png)
- Once process is complete, it may be terminated

Program Execution 
  - Process my be killed explicity or teminated due to error 
  - ![](Pasted%20image%2020240122161919.png)

More about processes
 - Mulitiple processes can be simultaneously active/ready
 - Only one process can actually run on a processor at a time
	 - For now, lets assume single processor system
- OS switches between multiple processes as appropriate
	- Multiprogramming

This introduces more concepts
 - Decide what process to run when -> scheduling policy
	 - Brings up another possible scenario - preemption
	 - ![](Pasted%20image%2020240122163107.png)

To manage multiple processes
 - information about each process must be maintained
	 - Process control block used for this 
		 - Process ID
		 - Process State (ready, running etc.)
		 - Program Counter - address of next instructed to be executed
		 - Registers - general purpose registers, stack pointer etc.
		 - Scheduling information
		 - Memory management information 
		 - Accounting information - time limits, etc.


