As we know 
 - Every process must have at least one thread of execution 
 - Function "main" forms this default thread

Important notes
 - Include file: pthread.h
 - Linker flag: -lpthread
	 - If program file is test_pthread.cpp, command would be g++ test_pthread.cpp -lpthread

We need to know 
 - Setup sequence of instructions
	 - Create function with desired sequence of instructions
		 - void* func(void*)
	- void* can point to any type of data
- Create new thread to execute sequence of instructions

Thread Creation
![](Pasted%20image%2020240129214645.png)

Why no hello?
 - By default, scheduling of threads is up to system 
	 - No gaurantee when and in what order threads execute
- Function main implicitly calls exit function when it's done
	- Terminates process, i.e., all threads - even if they're not done 
- Use different function to terminate only calling thread
	- ![](Pasted%20image%2020240129214809.png)

Parameters & return values
 - Any parameter to be passed must be converted to void*
	 - int arg;
	 - void* to_pass  (void*) &arg;
- Similarly, return values must also be converted to void*
	- char retval;
	- void* to_return  = (void*) retrval;
- What if there is more than one parameter to pass?
	- Consolidate parameters into single structure
	- Convert and pass pointer to structure as parameter