 - Multiprogramming enables the OS to make efficient use rof hardware srouces on a system by allowing proccesses to run concurrently an context-switching between them

 - To context switch from executing process A to process B, the OS must 
	 - 1) Save teh context of process A 
	 - 2) restore the context of process B

 - A process is placed in a ready state when it is a candidate for being scheduled on the CPU, but is not currenlty secheduled

 - When a process gets scheduled on the CPU, it moves to a running state

 - When a process cannot continue executing because it needs to wait for some event, it is paced in a blocked state

 - The Unit system call for creating a new process is called fork

 - The fork system call rerturns different values to the parent and child processes

 - At the time of the fork, the child process inherits its execution state from the parent process that creates it 

 - Once a child proc

