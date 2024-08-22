Looking deeper into processes
 - Processes embodies two primary characteristics
	 - Resource ownership (memory image)
	 - Execution of sequence of instructions
		 - The characteristic is captured by abstraction called thread
- Process provides enviroment and resouces for thread execution 
- Thread is the basic unit of execution and scheduling
- Every process has a thread of execution 
	- Process not limited to single thread of execution 

Consider an example
 - Making roasted vegetale pasta
 - Come up with sequence of operations for it 

What we learn from the example
 - Process could contain multiple instruction sequencees
 - Sequences can be modeled as threads in single process
	 - Allows concurrency within single process
- Threads of a given process are closely related 
	- Threads may share process resouces
	- Work in co-operative manner
- This concept is called multi-threading

Examples of multi-threading
- Word processor
	- Thread to interface with user
	- Thread to reformat document in background
	- Thread to perform periodic disk backup (autosave)
	- ...
- Web server
	- Dispatcher thread listens for requests or given connection 
	- Requests serviced by different worker threads

Thread states
 - Similar to processes, threads also can be different states
	 - States and transitions are similar to processes
	 - ![](Pasted%20image%2020240129172724.png)

What information is per-thread?
 - Program counter
 - Stack and stack pointer
 - Registers
 - Process with multiple threads look like this 

Thread information 
 - Just like Process Control Blocks are used for processes
	 - Thread Control Blocks are used to maintain thread info
	 - ![](Pasted%20image%2020240129172919.png)

Important points to note
 - Process -> instance of single program owned by single user
 - OS provides no protection among threads of same process
	 - Assuption -> threads within processes cooperate, not compete 
- All thread specific data (TCBs & stacks for all threads)
	- Part of process memory image
	- and hence accessible to all threads
- Programs must be carefully designed and implemented to ensure correctness
- Every process has at least one thread of execution (e.g. main)
	- Processes start with this one default thread
	- This thread can create other threads, which can create more

Advantages of multi-threading
 - More efficient CPU utilization within process
 - Creation/terminatino of threads is cheap
 - Context switch time between threads of process is minimal 
	 - Only info exclusive to threads needs to be "switched"
- Support effective communication due to shared memory 
