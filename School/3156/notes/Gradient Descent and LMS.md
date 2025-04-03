Least Mean Squares 
- Iterative method for finding the weights for our model 

Gradient Descent 
- optimization algorithm which finds minimums or maximums of functions 
	- for most problems the desirable solutions are found at either a maximum or minimum 

Learning rate 
- a hyperparameter that determines the step size taken during each iteration of the algorithm 
- Too Low 
	- A small learning rate requires many updates before reaching the minimum point 
- Just right 
	- The optimal learning rate swiftly reaches the minimum point 
- Too high 
	- Too large of a learning rate causes drastic updates which lead to divergent behaviors 

Stochastic Gradient Descent 
- Instead of sequentially using the data samples, one at a time or in a minibatch at a time, we can randomly select samples. This randomness causes the learning process to be much more noisy. However, this noise can actually be very useful when the error function is very irregular, allowing for a better hange to find the global minimum. 

Gradient Descent Optimization Algorithms 
- Momentum 
- Nesterov Accelerated Gradient (NAG)
- Adaptive learning rates methods:
	- Adagrad
		- Optimized for problems with sparse features 
		- 

