Generating Arrays 
- np.array(\[1, 2, 3 ])
	- type(a)
		- numpy.ndarray
	- a.shape
		- (3,)
	- len(a)
		- 3
- np.zeros
	- creates an array of zeros 
	- np.zeros((2, 2))
		- array(\[\[0, 0], \[0, 0]])
		- array.shape
			- (2, 2)

Reshaping and Adding New Dimensions 
- Reshaping
	- array = np.arange(1, 7)
		- array(\[1, 2, 3, 4, 5, 6])
	- array.reshape(2, 3)
		- array(\[\[1, 2, 3], \[4, 5, 6]])

Axis 
- the axis parameter refers to which axis gets collapsed 
- axis=None
	- Apply function or operations across entire array-wise
- axis=0
	- Apply operation column-wise, function or operations is applied across all rows for each column (i.e., 1 output for each column)
- axis=1
	- Apply operation row-wise (i.e., 1 output for each row)
- ![[Pasted image 20250318221249.png]]

Broadcasting 
- Broadcasting allows arithmetric between arrays of different dimensions or shapes 
- Rules 
	- If the two arrays differ in their number of dimensions, the shape of the one with fewer dimensions has its shape padded with ones on its leading (left) side
	- If the shape of the two arrays does not match any dimension, the array with shape equal to 1 in that dimension is stretched to match the other shape
	- If any dimension sizes disagree and neither is equal to 1, an error is raised 
- ![[Pasted image 20250318221839.png]]

Dot Product 
- An operation between two vectors that results in a singular scalar value. 
- computed by 
	- np.dot(A, B)
	- A @ B