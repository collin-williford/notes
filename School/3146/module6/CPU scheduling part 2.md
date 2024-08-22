  - Schedling policies for batch systems

First come first served (FCFS)
 - Scheduler maintains queue
	 - Incoming job added to end of queue 
	 - Job at head of queue chosen for execution 
- Jobs scheduled in non-preemptive manner 
	- Once job starts, it continues until it blocks/terminates/yields
	- Blocked job removed from queue
	- Upon unblocking, job added to end of queue
- Pros: very simple
- Cons: short jobs may have long wait time
- ![](Pasted%20image%2020240214215137.png)

Shortest-Job-First (SJF)
 - Scheduler chooses shortest job for exectuion at any given time
 - Two versions of SJF may be used
	 - Version 1: non-preemptive
		 - Once job is scheduled, it cannot be preempted until it completes CPU burst
	- Version 2: Preemptive
		- New job with shorter CPU burst than remaining time of current job arrives
			- Preempt current job and schedule new job 
			- A.k.a Shortest-Remaining-Time-First (SRTF)
- Pros: 
	- Good for short jobs
- Cons
	- Needs a-priori knowledge of execution times of CPU bursts
	- Long jobs may starve 

Non-preemptive SJF example 
![](Pasted%20image%2020240214215459.png)

Preemptive SJF example 
![](Pasted%20image%2020240214215515.png)


