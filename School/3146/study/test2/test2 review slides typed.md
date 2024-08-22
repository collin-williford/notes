Pthreads
 - Multiple threads run in the same process 
 - Using multiple threads is called multithreading 
 - main() function creates default thread 
 - Setup special methods to create new threads

Pthreads continued
 - Include file 
	 - \#include \<pthread.h>
- Linker flag when compiling -lpthread
	- g++ filename.cpp -o filename -lpthread
- Function header to start pthread
	- void* funcName(void* arg)
- Function call to create pthread
	- pthread_create(&id, NULL, funcName, (void* )&arg);

pthread_create statement components
 - ![](Pasted%20image%2020240220162845.png)

void* 
 - void* is a pointer to any type of data
 - Converting data to void* (before creating thread)
	 - int x; // Parameter
	 - int* ptr = &x;
	 - void* to_pass = (void*)ptr;
- or
	- void* to_pass = (void*)&x
- Converting data from void* (after creating thread):
	- void* arg; // Parameter
	- int* arg_ptr = (int*)arg;
	- int act_arg = \*arg_ptr;
- or
	- int act_arg = \*((int*)arg);

Structs
 - Parameters and return values 
	 - What if there is more than one parameter to pass?
		 - Consolidate parameters into single structure 
		 - Convert and pass pointer to structure as parameter
		 - ![](Pasted%20image%2020240220163311.png)

Data Sharing 
 - Threads can share data
 - Critical Region 
	 - Area of shared data
- Multiple threads in the critical region leads to conflicts (race conditions)
- Race Condition 
	- Multiple threads in the critical region can end up with different results

Mutual Exclusion Principles 
 - No two threads/processes may simultaneously be in critical sections accessing the same shared data 
 - No assumptions must be made about hardware (# of processors, speed, etc.)
 - A thread/process not in critical section must not prevent other thread/process from entering critical section 
 - No thread/process should have to wait for ever to enter critical section 

Data Sharing - Strict alternation 
 - Threads/processes take turns executing their critical regions 
	 - turn == 0 -> thread/processes 0 executes
	 - turn == 1 -> thread/process 1 executes 
- ![](Pasted%20image%2020240220163818.png)
- ![](Pasted%20image%2020240220163917.png)

Data Sharing  - Peterson's Solution 
 - A concurrent programming algorith for mutual exclusino that allows two or more processes to share a single-use resouce without conflict, using only shared memory for communication 
 - ![](Pasted%20image%2020240220163946.png)

Data Sharing - Mutex Questions 
 - Question 1 
 - Which of the following lines of code should be at line 16?
	 - pthread_mutex_lock(&mutex);
	 - ![](Pasted%20image%2020240220165501.png)
	 - 

Question 2
 - Which of the following lines of code should be at line 20?
	 - pthread_mutex_unlock(&mutex);
	- ![](Pasted%20image%2020240220165657.png)

Data Sharing - Mutex Example 
 - Example of withdraw() function with the mutex lock and unlock statements implemented.
 - This is similar to the deposit() function but instead of adding to the account balance, it removes.
 - ![](Pasted%20image%2020240220165808.png)

Data Sharing - Mutex Question 3
 - Which of the following lines of code should be at line 51? Keep in mind that you are passing to teh deposit void* function.
	 - pthread_create(&id1, NULL, deposit, (void*)pa);
	 - ![](Pasted%20image%2020240220170018.png)

Data Sharing - Mutex Question 4
 - Which of the following lines of code should be at line 55? Keep in mind that you are passing to a void* function.
	 - pthread_create(&id2, NULL, withdraw, (void*)pa);
	 - ![](Pasted%20image%2020240220170153.png)

Data Sharing - Mutex Question 5
 - Which of the following lines of code should be at lines 57 and 58?
	 - pthread_join(id1, NULL);
	 - pthread_join(id2, NULL);
	 - This will make sure each thread is done before the main thread finishes
	 - ![](Pasted%20image%2020240220170331.png)

Data Sharing  - Conditional Variables Question 6
 - Which of the following lines of code should be at line 22?
 - count == N
	 - Because this is the producer you are adding more to the queue, so you need to make sure it isn't full
- ![](Pasted%20image%2020240220170512.png)

Data Sharing - Conditional Variables Question 7
 - Which of the follinw lines of code should be at line 23?
 - pthread_cond_wait(&not_full, &mutex);
 - ![](Pasted%20image%2020240220171934.png)

Data Sharing - Conditional Variables Question 8
 - Which of the following lines of code should be at line 34?
 - pthread_cond_signal(&not_empty);
 - ![](Pasted%20image%2020240220172051.png)


Decomposition Types
 - Dividing work among threads/processes
	 -  Different threads/processes executes same function on different data
		 - Data decomposition 
	- Different threads/processes executes different functions
		- Task decomposition 
	- Third option 
		- One thread executes a function and produces output data
		- Other thread executes a different function and consumes data
		- Data-flow decomposition 

CPU Scheduling Policies 
 - First Come First Served or FCFS
	 - Works with a queue
	 - The first job that arrives is the first job to be ran 
- Shortest Remaining Time First or SRTF
	- Works with a priority queue
	- The job with the lowest remaining time in the current CPU burst is ran 
	- Preemptive - it can interrupt currently running processes 
- Round Robin or RR
	- Ues an enhanced queue
	- Each process is given a set amount of time to run called a quantum 
	- If a process goes through a quantum without finishing, it goes to the end of the queue
- Note: I/O wait time takes the process out of the queue until its over 

