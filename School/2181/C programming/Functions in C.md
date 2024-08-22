 - Functions are alco called subroutines or procedures
 - One part of a program calls the function 
 - ![[Pasted image 20230913101736.png]]

Function Return Values 
 - The simplest possible function has no return value and no input parameters
	 - Ex: 
		 - void abort (void)
- The next simplest case: value returned, but no input parameters. 
	- Ex:
		- char getchar (void)
		- int rand (void)
		- clock_t clock (void)


What Values can a function return?
 - The datatype of a function can be any of:
	 - integer or floating point number
	 - structs and unions
	 - enumerated constants
	 - void 
	 - pointers to any of the above
- Each functions type should be declared before use 


How Many Values Returned?
 - A function can return at most one value


Input Parameters of a Function
 - Often called arguments of the function 
 - Two types 
	 - Formal or abstract
		 - Parameter declarations in the function definition 
	- Actual or concrete
		- The actual values passed to the function at run time 
- If no input parameters to the function, leave empty, or use the void keyword


Parameter Passing
 - Parameters are passed by using call-by-value
	 - a copy of the parameter value is made and provided to the function
- Any changes the function makes to this (copied) value have no effect on the caller's variables 


Types for Function Arguments
 - In C,  an implicit type conversion occurs if actual argument type is different from formal argument type
	 - Advice: more predictable if you cast it yourself


Must Declare Function Before Use
![[Pasted image 20230913102712.png]]



