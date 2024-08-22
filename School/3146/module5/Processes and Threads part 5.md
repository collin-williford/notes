Data Sharing
 - Threads of a process share process data
	 - E.g., multiple threads read/write same data
	 - Consider banking process 
		 - Thread 1: withdraw money from account
		 - Thread 2: deposity money into accout
		 - Account is shared by threads 1 and 2
- Similarly, two different processes may share data 
	- E.g., output data of one process is input to anther process
![](Pasted%20image%2020240205144649.png)
![](Pasted%20image%2020240205144703.png)
![](Pasted%20image%2020240205144802.png)
![](Pasted%20image%2020240205144816.png)
![](Pasted%20image%2020240205144832.png)
![](Pasted%20image%2020240205144842.png)
![](Pasted%20image%2020240205144859.png)

Understanding race conditions 
 - Threads must not be interleaved during access to shared data 
 - This propery is calle dmutual exclusion among threads
 - Region of code during which shared data is accessed
	 - Critical section/critical region
- No two threads may simultaneously be inside critical sections accessing same shared data

What we need
![](Pasted%20image%2020240205145101.png)


This rule avoids race conditions
 - There are more rules in place from system perspective 
	 - Must consider fairness, efficiency, etc.
- Overall mutual exclusion requirements are 
	- No two threads/processes may simultaneously be in critical sections accessing same shared data
	- No assumptions must be made about hardware (# processors, speed)
	- A thread/process not in critical section must not prevent other thread/process from entering critical section
	- No thread/process should have to wait for ever to end critical section 
	- No thread/process should have to wait for ever to enter critical section 