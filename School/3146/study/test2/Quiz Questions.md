 Module 4-1 (Introduction to Multi-threading, POSIX threads)
 - A process embodies two primary characteristics, namely **resource** ownership and the execution of **sequence** of instructions 
 -  A process models **passive** characteristics and a thread models **active** characteristics
 - A thread is the basic unit of **execution** and **scheduling**
 - A process **is not** limited to a single thread of execution 
 - The Operating system **does not** provide protection among threads of the same process. Threads of the same process are exepcted to **cooperate** with each other 
 - It is possible that a process may have zero threads of execution
	 - False
- The header **pthread** must be included in any program that wants to use functions from teh pthrad library. When building a program that uses pthread functions, a **linker** flag, **-lpthread**, must be specified
- Which of the following is the correct command to build a C++ program my_pthread_program.cpp, that uses the pthread library?
	- g++ my_pthread_program.cpp -lpthread
- Any function that contains a sequence of instruction to be executed by a pthread must take a parameter type **void**** and return a value of type **void**** 
- The third parameter in the function to create a pthread is the **name** of the **function** containing the sequence of instructions to be executed by the pthread
- In a program with multiple threads, the order of execution of the different threads is **not guarenteed**
- Once the main function in a pthread program is done, it implicity calls a function named **exit**. This function terminates **the entire process**.
- If a pthread function requires more than one parameter, the program must create a user-defined **data struture** to consolidate the parameters

Module 5-1 (Data Sharing - Introduction, Strict Alternation, Peterson's Solution)
 - There needs to be an **explicit** mechanism for sharing among difference processes 
 - The sharing mechanism is **implicit** for threads of the same process 
 - The bank example demonstrated that threads must not be **interleaved** when accessing shared data. This means that when one thread is accessing shared data, no other thread should be allowed to **access** that same shared data 
 - The rules of strict alternation stipulate that while one of the siblings is taking a turn the other sibling must **wait**
 - Mutual **exclusion** is the idea that when one thread enters its critical region, the other thread cannot enter its critical region. This is a benefit of strict alternation. 
 - Busy **waiting** is a drawback of strict alternation because processes wait CPU cycles unnecesarily by repeatedly checking the turn variable 
 - In the code presented for Peterson's solution, a proces will indicate that it is leaving the critical region by setting the interested flag to FLASE in the **leave_region** method.
 - In **Peterson's Solution** a process does not have to wait unless another process is taking a turn or has expressed interest in taking a turn. In **Strict Alternation**, on the other hand, a process must wait until the other process has taken a turn, even if another process is not interested in taking a turn is not taking a turn  

Module 5-2 (Data Sharing - Mutex Introduction, Pthread Mutex)
 - Busy waiting uses CPU cycles because it is constantly checking or **polling** the status of critical region entry 
 - An alternative to busy waiting is to put the thread to **sleep** instead of having it continually poll the status of critical region entry. This effectively blocks or suspends the thread from **execution**
 - A **mutex** is a shared variable that can be in either a locked state or a unlocked state
 - With a mutex, a thread or process that wishes to enter the critical region must invoke a **lock** operation 
 - With a mutex, the thread_yield call means that the current thread or process yields the **CPU** so another process or thread can be scheduled instead
 - In the pthread library you would declare a variable of type **pthread_mutex_t** to create the global mutex variable 
 - The pthread_mutex_lock method takes a **pointer** to the mutex variable as the parameter 
 - In the example in the video the bank balance will always be the same no matter how many times we run the program because we can be sure that threads are accessing the balance variable in a **safe** manner by using a mutex variable

Module 6-1 (Data Sharing - Producer Consumer, Pthread Condition Variable)
 - Task decomposition is when multiple threads execute **different functions** with **the same** data whereas data decomposition is when multiple threads execute the **same function** with **different** data
 - A apporach in which a thread executes a function and **produces** output data, which is then **consumed** by another thread executing a different function is reffered to as **data flow** decomposition 
 - A way to facilitate **data flow** decomposition is to use a **shared buffer**, which must be used in a **safe** manner, i.e., its state must always be consistent
 - The pthread library provides a mechanism, called **condition variable**, that allows **synchronzation** based on the **value** or state of data
 - The **pthread_cond_wait** function is used when a thread wants to wait for a particular condition to occur and takes **two** parameters. The **pthread_cond_signal** function is used when a thread wants to signal the occurance of a particular condition and it takes **one** parameter
 - A condition variable is used in conjunction with a mutex variable 
	 - True
- When the pthread_cond_wait function is called, the system automatically **unlocks** the associated mutex variable and then **puts the calling thread to sleep**. When the corresponding pthread_cond_signal function is called, the system **wakes up the waiting thread** and then **locks** the associated mutex on its behalf. 

Module 6-2 (CPU Scheduling)
 - The part of the CPU that is responsible for deciding which job to run at any given time is called the **scheduler**. It uses a scheduling **algorithm** to make these decisions
 - Match the kind of policy with the description 
	 - Batch
		 - A system where performance can be optimized based on the jobs 
	- Interactive
		- A system where performance as percieved by the user must optimized 
	- Real-time
		- A system where predictibiliy rather than performance is most important as there are specific deadlines for each job 
- Batch systems have three main objectives
	- Maximize the number of jobs to complete in a given time period. This is know as **throughput**
	- Minimize the time between the submission and completion of jobs, otherwise know as **turnaround** time 
	- Keep the CPU **utilized** at all times 
- Interactive system have two main objectives: 
	- Minimize the time between the issuing and completion of jobs, otherwise known as **response** time 
	- Honor the users' perception that short jobs will take a short amount of time and that long jobs will take longer. This is known as **proportionality**.
- Real-time systems maintain predictability for the system by meeting the **deadlines** and by considering the **priorities** set by the system
- In **non-preemptive** scheduling, a job that is currently being executed cannot be interrupted to schedule another job. In **preemptive** scheduling, a job that is currently being executed can be interrupted to schedule another job
- The Shortest-Time-First(SJF) policy will execute the job with the shortest CPU **burst** first. In the **non-preemptive** version, the jobs that arrive later will wait even if they have shorter time than what remains on the currently running job.
- The Round Robin scheduling policy is more suitable for **interactive** systems than First Come First Served or Shortest-Job-First 
- In a Round Robin system, if the **quantum** of the CPU time is too short, there will be too many **context** switches, which creates too much switching **overhead**.
- Priority based scheduling will schedule the jobs with the **highest** priority first. Priority can be determined by an **internal** factor such as how long it has been in the system or by an **external** factor such as the importance to the user
- Multi-level scheduling is used for **hybrid** approaches for mixed type jobs. This scheduling approach divides jobs into separate **queues** that may use different scheduling policies
