 - Low level hardware controller detail too complicated for applicaiton porgrammers/users
 - Hardware state can get messed up through use of incorrect protocols
 - Need special software that 
	 - Knows how to interact with hardware controllers
	 - Provides simpler external interface to application programmers/users

 - Operating System (OS)
	 - Software that sits between hardware and application (user) programs
		 - Most systems have user interface layer between OS and applications
	- Provides a virtual interface to underlying hardware
		- Simple interface for applications/users (hides hardware complexity)
		- Ensures safety (protects hardware, prevents & handles errors)
		- May provide multiple levels of abstruaction 
	- Acts a a resource manager
		- Allows multiple applications/users to share resources
		- Ensures fair, efficient and protected access to resouces

Services provided by Operating System
 - Program execution 
	 - Load program and data, schedule and execute program 
- Memory management 
	- Manage main memory; ensure programs can't mess with other programs' memory 
- File management
	- Create, read, write files
	- Access control for files 
- I/O management 
	- Safe and controller access to I/O devices 
- Information maintenance
	- Get/set system time/date
- Communication services
	- Communication between programs
- User management
	- Authentication for access to system
- Error management
	- Detect and handle errors
- Accounting services
	- Collect statistics, monitor performance

To manage complexity
 - OS design typically seperates mechanism from policy 
	 - I.e., seperates how from what/when/which
- Mechanism
	- Data structures/operations used to implement abstraction/service 
- Policy
	- Procedures/rules to guide selection of action from possible alternatives

Protection
 - Need structures/mechanisms that ensure:
	 - Protection of hardware (CPU, memory, I/O devices)
	 - Protection between multiple applications/users
- System operation split into two modes
	- User mode
		- Execution on behalf of user -> protected mode
		- No direct access to hardware
		- Can execute only subset of instructions
		- Can access only restricted memory areas
	- Kernel mode
		- Execution on behalf of operating system -> privileged mode
		- Complete access to hardware
		- Can execute any instruction 
		- can Access any memory area 

Hardware support for modes
 - System maintains mode bit indicating current mode
 - If privileged operation is attempted in user mode
	 - It must be prevented from taking place
	 - System must be notified
- These are achieved using an exeception 
	- Synchronous interrupt -> caused by current instruction 
- When an exeception occurs
	- System enters privileged mode
	- Appropriate actions are taken 

Consequence of modes
 - Need special mechanism for applications to access OS services 
 - System call is the answer
	 - Interface between running programs and OS
	 - Provides controlled entry into kernel for privileged operation
	 - Makes sure access is performed in specific well defined way 

System Call
 - Causes system to switch to kernel mode
	 - Trap - a kind of synchronous interrupt - used to achieve this 
	 - In general, any interrupt causes switch to kernel mode
- Typically invoked using assembly language instructions 
	- Systems generally provide library or API to invoke system call
	- Library function serves as wrapper for actual system call

Internal structure of Operating Systems
 - Monolithic Architecture
	 - Entire OS is a single program
		 - Collection of procedures linked into single executable 
		 - Program runs fully in kernal mode
		 - Sometimes called "spaghetti nest" approach
			 - Everything tangled up with everything else 
	- Still usually has some structure 
		- Main procedure
			- Entry to OS here - invokes service procs
		- Service procedures
			- Carry out system calls
		- Utility procedures
			- Help service procedures 
		- Examples:
			- Linux, Windows
	- Pros & Cons
		- Any procedure can call any other directly
			- Efficient procedure calls
		- Design, implementation, debugging etc. can be hard
		- OS could become unwieldy & difficult to understand
		- Error in one part of OS can bring down entire OS 
- Layered Architecture
	- Divide OS into multiple layers
		- Each layer responsible for certain operations/services
		- Layser independent of layers above them
	- Example: THE operating system
- A variable of layered structure
	- Similar concept but layers represented as concentric circles
		- Inner layers have gigher privilege than outer layers
	- Example: MULTICS
- MicroKernel Architecture
	- Split OS functionality into multiple small modules 
		- Core module, called microkernel, runs in kernel mode
		- All other modules run in user mode
		- Communication between modules using message passing
	- Examples: QNX, MINIX 3
	- More commonly used in embedded/real-time systems
	- Pros & Cons
		- Easier to design, implement and debug
		- More flexible and easier to read
		- More isolation of faults/errors
			- Error in one module need not bring down entire OS
		- More reliable and more secure
		- Significant performance overhead

Modern operating system design 
 - Hybrid, object-oriented approach
 - Separate modules for seperate functionaltiy
 - Modules loadable into kernel as needed
 - Modules communicate via well defined interfaces 