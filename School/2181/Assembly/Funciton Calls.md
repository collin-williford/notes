Function declaration or prototype
 - Specifies the function's name, its return type, and its parameter list (the number and types of all the parameters)

Function Definition
 - Includes teh code to be executed when the function is called. All functions in C must be declared before they're called. This can be done by delcring a function prototype or by fully defining the function before calling it.

Function Call
 - A function call invlokes a function, passing specific argument values for the particular call
 - A function is called by its name and is passed arguemnts, with one argument for each corresponding funciton parameter

Execution Stack  
 - The execution stack keeps track of the state of active functions in a program. Each functino call creates a new stack frame containing its parameter and local variable values 
 - The frame on the top of the stack is the active frame
 - first in first out 

6 steps of performing a funciton call in a program?
1. Place arguments for callee in registers
2. Transfer control to callee function
3. Acquire Storage for callee function 
4. Perform callee's operations
5. Place result in register for caller
6. Return to place of call

What are three things a computer system needs to solve in order to support function calls
1. Instructions for control transfer for procedue call and call return 
 - Caller callee transfer
 - Callee to caller transfer
2. Register/memory for passing data between caller and callee
 - Passing argumet from caller to callee
 - Passing return value from callee to caller
3. Stack memory for function call
 - Storage for function variables
 - Preserve register data of the caller when control is in calllee
 - Restore the data when control is returned to caller

