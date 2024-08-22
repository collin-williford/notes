Scheduling policies for interactive systems

Round Robin (RR)
 - Active jobs kept in ready queue
 - Each job gets small unit (quantum) of CPU time
	 - Quantum usually 10-100 milliseconds
- After each quantum, job is preempted and next job in queue is scheduled
- Pros
	- Simple
	- ensures fairness
- Cons
	- Assumes all jobs are equally important
- Need to choose a quantum carefully
	- Too short -> to much switching overhead
	- Too long -> system not responsive 
![](Pasted%20image%2020240214215835.png)


Priority based scheduling 
 - Priority value (integer) associated with each job
 - Job with highest priority is scheduled
 - Schedule could be preemptive or non-preemptive
 - Priority assignment based on external factor
	 - Importance of job to user \[typically static assignment]
	 - Cons: low-priority jobs can starve
- Priority assignment based on internal factor
	- Aging
	- %CPU time used in last X hours

Hybrid approaches may be used for mixed job types 

Multilevel scheduling
 - Ready queue partitioned into separate queues 
	 - E.g., system processes, foreground (interactive), background (batch)
- Each queue has its own scheduling algorithm
	- Example: foreground (RR), background (FCFS)
- Scheduling must be done between queues 
	- Fixed priority -e.g, serve all foreground, then background
		- Possibility of starvation 
	- Time slice - e.g. 80% foreground (RR), 20% background (FCFS)