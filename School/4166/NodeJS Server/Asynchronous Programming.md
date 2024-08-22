Synchronous Programming
 - Statements are executed one by one 
 - Not efficient 

Asynchronous Programming
 - We can avoid blocking in the previous example by using asynchronous programming 
	 - allow the program continues running while waiting for the result of one operation 
- One way of asynchronous programming is to add a function as an argument to the slow operation 
- The function is called **call back function**, as it is called when the slow operation finishes 

Call Back Function 
 - Call back function is usually defined as an anonymous function with the following syntax
	 - (err, result) => {
		   if (err) {
		   //err handling code
			} else {
		 // success handling code
		 }
		}

Event Loop
 - NodeJS uses asynchronous, non-blocking I/O model
	 - Works a lot like a drive-through fast food place
		 - if the meal is easy the cashier will make it while the customer is still waiting upfront 
		 - if meal takes a while it gets passed to a worker in the back while the customer waits 
![[Pasted image 20230917192910.png]]
