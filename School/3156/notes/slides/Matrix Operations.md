Matrix/Vector Operations 
- Basic Operations 
	- Scalar Multiplication 
		- Multiply a matrix by an operation 
		- Distribute 
		- ![[Pasted image 20250319141051.png]]
	- Addition 
		- Both matrices must have same order 
		- Add corresponding units 
		- ![[Pasted image 20250319141139.png]]
	- Subtraction 
		- Both matrices must have same order
		- Subtract corresponding elements 
		- ![[Pasted image 20250319141202.png]]
	- Multiplication
		- When product (m x n) * (n x p)
			- the inside elements must be the same 
			- ![[Pasted image 20250319141404.png]]
- Inverse
	- ![[Pasted image 20250319142227.png]]
- Determinant 
	- A real number associated with a square matrix 
	- Used for inversion 
	- if det(A) = 0, then A has no inverse 
		- ![[Pasted image 20250319143718.png]]
	- det(A) = ad - bc
- Trace of a Matrix 
	- If A is a square matrix, the trace of A, denoted by tr(A), is defined to be the sum of the diagnoal entries of A 
	- The trace is undefined if A is not a square matrix 
	- ![[Pasted image 20250319144228.png]]
- Rank 
	- Let A be an m x n matrix. The trace of A is the maximal number of linear independent row vectors 
	- This is complicated do we need to know this?

Vector Operations 
- Dot Product 
	 - Same as multiplying each feature by the corresponding weight and summing 
	 - Think of dot product as matrix multiplication
	 - ![[Pasted image 20250319141606.png]]
- Magnitude
	- The magnitude is the dot product of a vector with itself
	- ![[Pasted image 20250319141843.png]]
- The angle between two vectors 
	- The dot product is also related to the angle between two vectors but it doesn't tell us the angle 
	- ![[Pasted image 20250319141952.png]]


