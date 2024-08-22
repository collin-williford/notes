Data Sharing - Producer Consumer, Pthread Condition Variables 

Dividing work among threads/processes
 - Different threads/processes execute same function on different data
	 - Data decomposition
- Different threads/processes execute different functions 
	- Task decomposition
- Third option 
	- One thread executes a function & produces output data
	- Other thread executes a differenct function & consumes data
	- Data-flow decomposition 

Shared buffer to facilitate this 
 - Producer thread/process produces data items & places them in shared buffer
 - Consumer thread/process removes data items from shared buffer & consumes them
 - Need to maintain consistency of buffer at all times
	 - Producer should not put items into full buffer
	 - Consumer should not remove items from empty buffer
- Busy waiting should be avoided

Producer-consumer problem 
 - Also called bounded buffer problem 
 - Solution 
	 - Keep count of number of items in buffer
	 - Producer can check number of items
		 - Go to sleep when buffer is full
		 - Be woken up when buffer has at least one empty space
	- Consumer can check number of items
		- Go to sleep when buffer is empty 
		- Be woken up when buffer has at least one item

Pthread library provides a mechanism that can be used for synchronization based on value/state of data 

Pthread condition variable
 ![](Pasted%20image%2020240212174522.png)

![](Pasted%20image%2020240212174535.png)
![](Pasted%20image%2020240212174556.png)

![](Pasted%20image%2020240212174606.png)

