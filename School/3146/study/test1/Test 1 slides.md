Computer Organization - Memory
 - Main memory is a collection of supercells
	 - Typically implemented with RAM
	 - Comprised of smaller 1 bit cells
	 - Stores data (which we access and point to with pointers)
- Cache is like a smaller version of the main memory 
	- Stores commonly used values for faster retrieval in the future
- Memory, at the lowest level, is comprised of registers
	- Registers for:
		- The program counter
			- What line the program currently is at
		- Stack pointer
			- Address at the top of stack 
- All of this helps us store variables quickly and reliably

Computer Organization - Input/Output (I/O)
 - Most programs need to take input of some kind
 - Multiple ways to actually implementing this system 
	 - Polling 
		 - Continually asking if the I/O device has anything new to send
			 - Constly and inefficient usually
	- Interrupts
		- Computer sends a signal to the device letting it know it needs I/O
			- The I/O device then interrupts the program when it has completed its tasks

The Command Line  - File Management 
 - When you are using the command line in this class, you are using BASH
	 - Known as a shell which gives you a textual way of interacting with the system
	 - Relatively easy to understand once you can visualize what is happening 
- Basic Commands to know 
	- cd
		- Stands for "Change in directory" and allows you to change what folder (directory) you are currently in 
	- ls
		-  Displays all files and directories inside of your current directory
- Just like in other compiled languages need to complie code before we can run it 
	- To do this we use g++ command
		- g++ \<NAME OF FILE HERE> -o \<NAME OF EXECUTABLE HERE>
	- To execute the program you just need to tell bash to run it for us 
		- ./\<NAME OF EXECUTABLE HERE>
- Using this, along with the file management commands, should be able to compile and run code easily 

Operating System Basics
 - An Operating System is something that sits between hardware and software
	 - Gives access to hardware components through software
		 - Program execution 
		 - Memory management
		 - File management
		 - I/O mangement
	- OS design separates how (mechanism) from what/when/which (policy)
	- Two different system operation modes
		- User
			- Executes programs on behalf of the user in a protected mode
			- No direct access to hardware with restricted access to instruction and memory areas
		- Kernel
			- Executes on behalf of operating system in a privileged mode 
			- Complete access to all areas of hardware, memory, and instruction sets
- Some programs need access to the things available in kernal mode but don't have that form of access
	- This is achieved through a System call
	- Provides it controlled entry into kernel mode
	- Gives the program certain parameters and boundaries 
- A system call causes the system to switch to Kernel mode
- Sevel ways to architect an operating system
	- Monolithic 
		- Entire OS within a single program
		- All programs operating in Kernel mode
		- Can get very messy - any part can bring any other part down
	- Layered
		- Each part of the OS gets layers that are independent of each other 
	- Microkernel
		- Split all functionality into smaller modules
			- Core is known as microkernel and runs in kernel mode
			- All other modules interface with the microkernel for kernel mode
		- Modern operating system use a mix of all in a hybrid approach 
- ![](Pasted%20image%2020240129201830.png)

C++ Basics - Pointers 
 - Need a way to access the direct memory location of a variable
	 - This is done through pointers
		 - code ex
			 - int test = 5;
			 - int \*testPtr = &test;
			 - cout << \*testPtr;
		- This will print out 5
			- &test gives us the memory address
			- \*testPtr retrieves the value stored at a memory address
- Declare a pointer variable with the * operator
	- Like so
		- int \*testPtr
- Structs
	- A struct is essentially a user defined custom data structure. With a struct, you can store multiple fields together
	- It is similar to a class, but lightweight
	- To access struct members, use the .operator
	- To access struct members when the struct is a pointer, use the -> operator

Processes
 - A process is a running instance of the program
 - Processes are created from cloning
 - ![](Pasted%20image%2020240130103509.png)

Process Control Block
 - Process control block used for this
	 - Process ID
	 - Process State (read, running, etc.)
	 - Program Counter - address of next instruction to be executed
	 - Registers - general purpose registers, stack pointer etc.
	 - Scheduling information
	 - Memory management information
	 - Accounting information - time limits, etc.
	 - ..
	 - ![](Pasted%20image%2020240130103639.png)

Creating Processes
 - In UNIX based systems, processes are cloned from an existing process (init)
- With C++ we can call fork() to create a process
- The fork() call returns a different value
- ![](Pasted%20image%2020240130104329.png)

execvp
 - The execvp command can be used to change a process' memory image
 - Copy on write - start with shared memory and only make a copy when data is modified
 - ![](Pasted%20image%2020240130104423.png)

Orphans and Zombies
 - OS maintains a hierarchy
 - If a parent terminates before the child, the child becomes an orphan and is adopted by the init process
 - If a child is terminated before the parent, the child becomes a zombie and can be reaped by its parent
	 - The os provides the wait command for this 

Processes - Typical Steps
 - \[hw] Save program counters and some registers on stack
 - \[hw] Load program counter specified in interrupt vector
	 - Interrupt vector -> has address of interrupt service routine
- \[asm] Save context info (registers, etc) in Process Control Block of current process
- \[asm] Set up a new stack
- \[C] Remaining work for specific interrupt type
- \[C-sched] Choose new process to be scheduled
- \[asm] Restore context info for new process and start it 

Code Review
