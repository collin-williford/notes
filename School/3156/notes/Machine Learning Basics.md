Scalar
- Scalar is a value (1, 2, -3.2, 1000)
- A scalar is a quantity that only has magnitude 

Vector 
- A tuple of numerical values 
- collection or grouping of scalars 
- ![[Pasted image 20250319150218.png]]

Matrix
- rectangular table of numbers in rows and columns 
- n represnets the number of rows
- m represents the number of columns 
- ![[Pasted image 20250318213147.png]]

N-Dimensional Array 
- generalizations of matrices to the 3, 4, 5, or n-dimensions
- n represents the length of 1st dimension 
- m represents the length of 2nd dimension
- l represents the length of 3rd dimension 
- code 
	- np.random.rand(2, 2, 2)
		- 3 dimensional with each having a length of two 

Basic stages of ML 
1. Problem Formulation 
	1. What problem, and how will you frame your problem 
		1. Think about which type of ML problem you will be facing (supervised learning, unsupervised, reinforcement learning)
	2. What assumptions, if any, are you making about this problem 
	3. What are the current solutions?
	4. Are there any comparable problems?
	5. Which performance measures (i.e., metrics) will be best to evaluate your problem?
		1. Performance measures help measure how well your algorithm/model is learning to solve the problem 
2. Gathering data 
	1. Determine what data features you will need and how much data you might need 
	2. Find data related to your problem. If there is none, collect it 
		1. Do not be afraid to combine multiple datasets 
	3. Convert to a usable format 
	4. Identify which feature will act as your labels/targets 
	5. Figure out how to store the data if your dataset is very large 
3. Data Exploration and visualization 
	1. Plotting features and observing data characteristics such as scale and values 
		1. Pay attention to data types, missing values, noise, outliers, distribution of data 
	2. Studying correlations between features 
		1. For example, are there any features that correlate with our target features
	3. Testing different feature engineering/transformations techniques to see if they might improve the quality of data 
		1. For example, dimensionality reduction techiques or log transform 
4. Data Preprocessing 
	1. Split data into train, validation, and test splits 
	2. Clean data through removing outliers or filling/removing missing values 
	3. Discretizing continuous features 
	4. Converting categorical variables or strings into numerical representations 
	5. Normalizing features 
	6. Feature selection 
	7. Aggregating features 
	8. Decomposing features 
	9. Adding new features 
5. Training 
	1. Train algorithm(s) using training data and selected hyperparameters 
		1. Hyperparameters refers to the parameters that are used to configure the model (external from the parameters the model learns) while model parameters, or just referred to as parameters, refer to the weights the model learns (internal parameters the model learns)
	2. Measure training performance using selected performance measures 
		1. If you have multiple models, you can begin to compare training performance, through the validation set should be used to choose the "best"
6. Evaluation, hyperparameter tuning and model selection 
	1. Perform Hyperparameters tuning by changing the values manually or by using automated algorithms like nested k-fold cross-validation
		1. This entails testing different parameters for an algorithm using the training and validation splits 
	2. Use the validation split to compare algorithm performance. Select the algorithm with the highest validation performance 
		1. You can use methods like K-fold cross-validation as well to compare model performancemore throughly 
	3. Try combing your best algorithm models to make a single prediction (referred to as ensemble learning) and test performance using the validation set 
	4. If all algorithms perform poorly, you might have to revisit choices made in any previous stages.
		1. For example, you might need to refine the data preparation process or even select new algorithms or hyperparameters. In a worst case scenario, your problem could even be poor quality data in which no algorithm will work 
7. Prediction 
	1. Compute predictions using the test set or any unseen data and the best model selected from the previous stage 
	2. Measure the generalization error (also called test error) using the test split and your selected performance measures 
	3. Analyze how your model is performing on the test set. If your algorithm performs poorly on the test set, you may need to start all the way from stage 1 again. Additionally, you will need to find a brand new test set in order to avoid selection bias 

