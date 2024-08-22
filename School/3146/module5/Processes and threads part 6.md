Option: strict alternation 
 - Threads/processes take turns executing their critical regions
	 - turn == 0 -> thread/process 0 executes 
	 - turn == 1 -> thread/process 1 executes
	 - ![](Pasted%20image%2020240209141307.png)
	 - ![](Pasted%20image%2020240209141314.png)

Option: strict alternation
 - Pros
	 - Mutual exclusion correctly maintained
- Cons
	- Busy waiting required 
		- processor cycles unnessarily wasted
	- Thread/process forced to wait even if other thread/process executing its non critical region 
		- Violates one of the requirements we looked at earlier
		- Makes method unsuitable for use in practice
		- Gets worse as num competing threads/processes increases