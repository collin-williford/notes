Expert Systems
- Expert systems approach (also called rule-based or traditional programming):
	- Experts write rules that capture patterns about the problem 
	- Programmers implement the rule-based solution in computer code
- Expert Systems approach:
	- Congnitively demanding 
		- Difficult for humans to reason with many useful by imprecise rules that are indicative (signals) of span or not spam:
			- words, phrases, images, meta-data, time series
			- Need to combine a large number of rules, figure out their relative importance in determining spam vs. ham label 
	- Brittle: Always going to miss some useful features or patterns
		- "all grammars leak"
		- Spam filtering is adversarial, new features need to be added over time 

Machine Learning 
- ML = program computers to learn from experience to perform well on a given task 
	- Automaticlally discover patterns from solved problem instances (i.e., experience) that enale solving new instances of the problem 
- Supervised Learning approach:
	- Acquire a large enough dataset of labeled examples: 
		- Email is the example, the label is spam (+1) vs. not spam (-1)
		- Collecting labels is easier than writting rules
	- Represent examples as features vectors, each feature has a weight 
	- Learn the weights such that the model prediction (weighted combination of features) matches the labels of training examples

Machine learning: Training and Testing 
- ML = constructing computer programs that learn from experience to perform well on a given task 
	- Supervised learning 
		- discovery patterns from labled examples that enable predictions on (previously unseen) unlabled examples 

ML is Meta-Programming 
- An ML model is a computer program 
	- We do not want ot explicitly program (model) the computer for each particular task 
	- Use a general ML algorithm and task-specific data to automatically create the Program, i.e., the Model, that solves the task 
- An ML algorithm (e.g., gradient descent) is a meta-program 


Occam's Razor
- Do not make things needlessly complicated 
- Prefer the simplest hypothesis that fits the data 

Kologorov Complexity 
- the length of the shortest program that generates the data 

ML Objective 
- Find a model M that is simple and fits the training data
- inductive Hypothesis 
	- Models that perform well on training examples are expected to do well on test (unseen) examples 
- Occam's Razor 
	- Simpler models are expected to do better than complex models on test examples (assuming similar training performance)

ML Concepts and Notation 
- A (labeled) example (x, y) consists of:
	- Instance / observation / raw feature vector x
	- Label y
- A training dataset is a set of (training) examples (x1, y1), (x2, y2), (x3, y3) ...
	- The data matrix X consists of all instance vectors (x1, x2, x3) row-wise
	- The label vector y = (y1, y2, y3)
- A test dataset is a set of (test) examples
	- Must be unseen
- There is a function f that maps an instance x to its label y=f(x)
	- f is unknown 

Fitting vs Generalization 
- Fitting performance 
	- how well the model does on training examples 
- Generalization performance 
	- How well the model does on unseen (test) examples 
- We prefer finding patterns to memorize examples 
	- Overfitting 
		- Line is to aggressive on data points 
	- Underfitting
		- Line is to relaxed and doesn't actually represent data 

Underfitting vs. Overfitting
- Underfitting
	- Model does not do well on training data 
		- Low capacity (too few params) or Training issues (too little training) 
- Overfitting 
	- Model does well on training, poorly on test 
	- Can be mitigated by tuning hyper-parameters 
		- Perceptron
		- Logistic regression 
		- Neural networks 

Regularization 
- Any method that alleviates Overfitting 
	- Parameter norm penalities 
	- Dataset augmentation 
	- Dropout (dropout rate)
	- Ensembles 
	- Semi-supervised learning 
	- Early stopping (limit number of epochs)
	- Noise robustness 
	- Sparse representations 
	- Adversarial training 

Supervised Learning 
- Training 
	- Training examples -> learning algorithm -> Model x
	- Model x -> test examples -> Generalization Performance 

Supervised Learning 
- Learning from labeled examples 
	- Classification 
	- Regression 

Unsupervised Learning 
- Learning from unlabled examples 
	- Clustering 
	- Dimensionality reduction (visualization)
	- Density estimation 

Reinforcement Learning 
- Learning with delayed feedback 

