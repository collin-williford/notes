 - A situation where several threads access and manipulate the same data concurrently and the outcome of hte execution depends on teh particular order is which access takes place is called 
	 - Race condition 

 - A critical section or region is 
	 - A piece of code in which a thread accessed resources that are shared by other threads as well 

 - Overall mutual exclusion requirements include 
	 - A process that is not itself in a critical section must not prevent another process from entering its critical section 

The fundamental differetnce between strict alternation and petersons solution is that
 - Petersons solution allows a waiting process to take a second turn as long as no other process is waitng to take a turn, whereas strict alternation forces a processs to wait until other processes have taken a turn 

 - Strict alternation satisfies all of the 4 mutual exclustion requirements 
	 - No

 - The fundamental difference between strict alternation and petersons's solution on the one side an dmutuxes on the other side is that 
	 - Strict alternation and Peterson's solution sufer from busy waiting whereas mutexes do not 

 - Since the instructions that pthreads must execute are captured using functions, mutex variables that pthreads use for safe data sharing must be local to their functions
	 - false

 - Which of the following is the data type for a mutex variable? 
	 -  pthread_mutex_t

 - PTHREAD_MUTEX_INITIALIZER is a ___ that is used to initialize a mutex variable to ____ attribute values 
	 - macro, default 


