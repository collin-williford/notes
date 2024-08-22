 - So far, one problem still persists
	 - Busy waiting
	 - Alternative approach
		 - If thread/process unbale to enter critical region
			 - Thread/process can be put to sleep (i.e., it gets blocked) 
		- Wake up signal sent to thread/process when it becomes eligible to enter critical section 

One solution
 - Shared variable mutex that can be in one of two states
	 - Locked or 1
	 - Unlocked or 0
- Can be used to implement software lock without busy waiting

Mutex Operation
 - ![](Pasted%20image%2020240207214640.png)
 - Similar to software lock with enter_region and leave_region
 - Crucial difference
	 - No continous checking of mutex, i.e., no busy waiting 