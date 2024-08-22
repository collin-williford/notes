 Assume there are 4 lawsn that need to be mowed, fertilized and watered. Assume that one garderner mows all the lawns, another fertilizes all of them and a third waters all of them. If you think of this situation in terms of threaded program, what form of decompositon is being employed here?
	 - Task decomposition 

Assume that there are 4 lawns that need to be mowed, fertilized and watered. Once again, thinking of this situation in terms of a thraeded program, which of the following is an example of data decomposition?
	 - One gardener mowing, fertilizing and watering two of the lawns and another one mowing, fertilizing and watering the other two
	 - One gardener mowing, fertilizing and watering one of the lawsn and another onw mowing, fertilizing and watering the other three
	 - Both above

Before calling the pthread_cond_wait function, a thread must make sure to ___ the mutex whose address is to be passed as a parameter to the function 
 - lock

After callling the pthread_cond_signal function, a thread must make sure to unlock the mutex associated with the condition variable being signalled. 
 - True

Which of the following factors are important when scheduling in batch systems?
1. minimize throughput
2. Minimize response time
3. Minimize turnaround time
4. Meet job deadlines
 - Minimize turnaround time 

Which of the following scenarios may trigger a scheduling decision?
 - New process activation 
 - Completion of I/O event 
	 - Both of the above

A preemptive schedule is better than a non-preemptive one 
 - Depends 

Which of the following scheduling policies requires a-priori knowledge of CPU burst lenghts of jobs?
 - Shortest Remaining Time First policy 

What is the advantage of a shorter quantum of execution when using a Round Robin policy?
 - Increaed responsiviness

Which of the following scheduling schemes do you believe whould be best suited to a system like a personal laptop computer?


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
