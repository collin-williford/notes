 - NodeJS uses a single-threaded event loop to handle multiple concurrent requests
 - To prevent a request from blocking the event loop, call non-JavaScript operations, such as I/O operations asynchornously
 - Callback functions can be used to handel asynchronous calls

Asynchronous OPerations with Callback Funcitons
 - A callback function is passed as an argument ot an asychronous function call
 - After the asynchronous operation finishes executing, it sends results or errors through the callback function 
 - Example
 ![](Pasted%20image%2020231017230043.png)

Callback Hell
 - Sometimes multiple asynchronous operations are executed sequentially, where each subsequent operation starts with the previous operation succeeds, with the result from previous step
 - This will result in nested callback functions also called callback hell
 - Example
 - ![](Pasted%20image%2020231017230300.png)

Promise
 - Promise was introduced in ES6 (2015) as an alternative to callback functions. It allows for more readable asynchronous code
 - A promice is an object representing the result of an asynchronous operation 
 - A promice has 3 possible states:
	 - Pending
		 - Asynchronous operation has not completed yet
	- Fufilled:
		- Asynchronous operation has completed successfully and the promice has the value
	- Rejected
		- Asynchronous operation has completed with an error

Create a Promise
 - To create a promise, call constructor
	 - Promise((resolve, reject) => {
		   //perform asynchronous operations, then
		   // depends on the outcome, call resolve or reject
		   });
 - The constructor takes a function as a parameter, which takes two callback functions as parameters
	 - If the asynchronous operation succeeds, resolve() is called with result
	 - If there is an error, reject() is called with error

Consume a Promise
 - When a function returns a promise, the caller consumes it by calling
	 - then(callback): process the result returned by the promise
	 - catch(callback): handle the error thrown by the promise
- ![](Pasted%20image%2020231017230947.png)
 - ![](Pasted%20image%2020231017231022.png)
 - 

Chaining
 - Promises can be chained to execute multiple asynchronous operations sequentially
 - Return a new promise for the next asynchronous operation in then funciton
 - ![](Pasted%20image%2020231017231300.png)


