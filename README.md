# Bootstrapping-and-Boosting

## Table of Contents
- [Bootstrapping](#bootstrapping)
- [Bagging](#bagging)
- [Boosting](#boosting)
- [Types of Boosting](#types-of-boosting)
- [Benefits of Boosting](#benefits-of-boosting)
- [Challenges of Boosting](#challenges-of-boosting)
- [XGBoosting vs Random Forest](#xgboosting-vs-randomforest)
- [Fitting and Tuning Random Forests](#Fitting-and-Tuning-Random-Forests)
- [Simulation Study](#Simulation-Study)

  
## 1. Bootstrapping
<img width="545" alt="Screenshot 2024-01-09 at 10 33 22 PM" src="https://github.com/ColleenJung/Bootstrapping-and-Boosting/assets/119357849/0fc1acb6-84cb-41d1-98af-a386e0985042">

This is a resampling method that uses random sampling **with replacement**.


## 2. Bagging (**B**ootstrap+**agg**regating )
<img width="599" alt="Screenshot 2024-01-09 at 10 33 35 PM" src="https://github.com/ColleenJung/Bootstrapping-and-Boosting/assets/119357849/a540bf6b-d5b7-4510-86f8-261bf2fefcde">

Bagging, which is short for bootstrap aggregating, is an ensemble learning technique that helps to improve the performance and accuracy of machine learning algorithms.
<img width="731" alt="Screenshot 2024-01-09 at 10 38 02 PM" src="https://github.com/ColleenJung/Bootstrapping-and-Boosting/assets/119357849/771d4afa-80b4-49f4-9d18-cd00403b71a2">


## 3. Boosting
<img width="617" alt="Screenshot 2024-01-09 at 10 34 20 PM" src="https://github.com/ColleenJung/Bootstrapping-and-Boosting/assets/119357849/05f9d08f-7a97-4111-8da3-6df3171e9079">

Boosting algorithms work on the idea of first building a model on the training dataset and then building a second model to **correct the faults in the first model**. This technique is **repeated** until the mistakes are reduced and the dataset is accurately predicted.

## Types of Boosting

**1.AdaBoost (Adaptive Boosting)**

<img width="687" alt="Screenshot 2024-01-09 at 11 19 37 PM" src="https://github.com/ColleenJung/Bootstrapping-and-Boosting/assets/119357849/9373ec08-3856-4d6c-8344-a38605b2ef18">

It works by training a sequence of **weak learners**, where each learner focuses on correcting the **mistakes** made by **its predecessor**. 
Adaboost works by **weighting incorrectly classified** instances more heavily so that the subsequent weak learners focus more on the difficult cases.
The final prediction is obtained by combining the weighted predictions of each weak learner.

**2.Gradient Boosting**

<img width="640" alt="Screenshot 2024-01-09 at 11 15 39 PM" src="https://github.com/ColleenJung/Bootstrapping-and-Boosting/assets/119357849/8d8932cf-ad11-41f2-9534-d4fc51b2ca7a">

New models are added to correct the errors made by existing models, using gradient descent to minimize the loss function, making it effective for both regression and classification tasks.

**3.XGBoost (Extreme Gradient Boosting)**

<img width="605" alt="Screenshot 2024-01-09 at 11 12 44 PM" src="https://github.com/ColleenJung/Bootstrapping-and-Boosting/assets/119357849/5020adb0-f142-4508-9bc0-e9c4278e48a4">

XGBoost is an optimized and more efficient implementation of gradient boosting, designed for speed and performance, which provides support for handling missing data, regularization to avoid overfitting, and can be parallelized across clusters.

## Benefits of Boosting
**1. Reduction of bias**
Boosting algorithms combine multiple weak learners in a sequential method, which iteratively improves observations. This approach helps to reduce high bias that is common in machine learning models.


## Challenges of Boosting

**1. Vulnerability to outlier data**
Because each model attempts to correct the faults of its predecessor, outliers can skew results significantly.

**2. Real-time implementation**
You might also find it challenging to use boosting for real-time implementation because the algorithm is more complex than other processes. 


## XGBoosting vs Random Forest

<img width="546" alt="Screenshot 2024-01-10 at 2 56 59 PM" src="https://github.com/ColleenJung/Bootstrapping-and-Boosting/assets/119357849/c2ae73fd-0fe8-4301-9c63-ecd767348a6a">


## Random Forest

<img width="596" alt="Screenshot 2024-01-10 at 2 38 30 PM" src="https://github.com/ColleenJung/Bootstrapping-and-Boosting/assets/119357849/4539ae9d-03be-4af2-bc0c-d21ee57d8c31">

A team of desicion trees each having slightly different specialitues, and the final prediction is like a team decision made after cosidering everyone's input.

**Advantages**

**1. Robust to Overfitting:** Due to the random nature of the Random Forest (random sampling of data points and features), the model is less prone to overfitting than a single decision tree. 

**2. Handles Large Datasets and Feature Spaces:** Random Forest can easily handle datasets with a high dimensionality (many features) and a large number of data points, making it a good choice for complex datasets.

## XGBoost

XGBoost, which stands for **“eXtreme Gradient Boosting,”** is an advanced implementation of the gradient boosting algorithm. Gradient boosting is a machine learning technique where the main idea is to **combine** many simple models, also known as **“weak learners,”** to create an ensemble model that is better at prediction.

The **“Gradient”** in “Gradient Boosting” refers to the fact that the algorithm uses gradient descent optimization to minimize the errors in the predictions. It’s a mathematical way of saying: **“find the best direction to reduce the error.”**

**Advantages**

**1. Performance:**  XGBoost can handle a variety of data types, including **numeric, categorical, and ordinal data**

**Disadvantages**

**1. Prone to Overfitting if Not Properly Tuned:** Although XGBoost has regularization parameters to control overfitting, it can still be prone to overfitting if not properly tuned. Careful tuning of parameters such as the learning rate, the depth of the tree, and the number of trees is necessary.

## When to Use Which Algorithm

1. Use **Decision Trees** when interpretability is highly important. Decision trees are also good when you have categorical data or when you need a quick and simple model.

2. Use **Random Forests** when you need a better balance between interpretability and accuracy. Random Forests are also good when you have large datasets with many features.

4. Use **XGBoost** when your primary concern is performance and you have the resources to tune the model properly. XGBoost is also effective when you have a mix of categorical and numerical features, and when you have a large volume of data.

## Fitting and Tuning Random Forests
  
**R package**
- 'ranger': A Fast Implementation of Random Forests
- 'caret' : short for Classification And REgression Training
  
<img width="572" alt="Screenshot 2024-01-21 at 4 37 38 PM" src="https://github.com/ColleenJung/Bootstrapping-and-Boosting/assets/119357849/0e8d27c1-0c67-4e0a-9a01-954957eac528">

<img width="561" alt="Screenshot 2024-01-21 at 4 38 01 PM" src="https://github.com/ColleenJung/Bootstrapping-and-Boosting/assets/119357849/ae3ccf20-738f-45ed-baef-bea6e4c4a993">

The best tuning parameter is 'mtry'=4, 'min.node.size'=10.

Provide a statement to explain why we want to consider respect.unordered.factors = "partition", and how is it different from its default value.

 'respect.unordered.factors' = TRUE or FALSE should be based on the understanding of the data and the specific requirements of your analysis

- When this parameter(respect.unordered.factors = "partition") is set to FALSE by default, 'ranger' package treats all string-valued variables as if they were ordered. 
This means it doesn't spend time converting these categorical variables into dummy or indicator variables, treating them as numeric variables. 

- This default setting works well when the categorical variables indeed have an ordered relationship with the outcome. However, treating these variables as ordered(categorical variables) might lead to a loss of information and potentially weaker model performance.

- Alternative (respect.unordered.factors = TRUE):tells ranger to handle unordered factors properly by creating dummy variables. This can be more computationally expensive but allows the model to capture more complex relationships between categorical variables and the outcome. 

- It's particularly important when the order of factor levels doesn't have a meaningful relationship with the response variable.

- In this model, given that 'cp', 'thal' doesn't have a meaningful relationship with the outcome 'num', it might be more appropriate to set respect.unordered.factors = TRUE. This will allow the ranger model to more accurately capture the relationship between these categorical variables and the outcome, though at the cost of increased computational complexity.

  <img width="556" alt="Screenshot 2024-01-21 at 4 34 30 PM" src="https://github.com/ColleenJung/Bootstrapping-and-Boosting/assets/119357849/bcec3243-3380-4a56-a9b1-367a3b2276fc">

## Simulation Study 

**Goal : perform simulation studies to analyze the effect of nodesize**

- Your simulation should repeat nsim = 100 times
- Within each simulation, you should generate training and testing data using the following code, and evaluate the prediction mean squared error of random forests
- Set mtry = 1 and ntree = 300 for all simulations
- Use a grid of nodesize values: c(1, 5, 10, 20, 30, 40)
- Leave all other tuning parameters as default

  <img width="556" alt="Screenshot 2024-01-21 at 4 34 30 PM" src="https://github.com/ColleenJung/Bootstrapping-and-Boosting/assets/119357849/bcec3243-3380-4a56-a9b1-367a3b2276fc">
  
The plot is in U shape, the MSE is the smallest when nodesize=20

**Decreasing MSE with Increasing Nodesize (up to a point):**

If the plot shows a decrease in MSE as nodesize increases initially, it suggests that larger nodesize values are helping to reduce overfitting. Smaller nodesize allows trees to grow more complex and can lead to trees that are overly tailored to the training data, capturing noise rather than the underlying pattern.
 
**Increasing MSE with Further Increase in Nodesize:**

Beyond a certain point, if the MSE starts to increase with larger nodesize, it indicates underfitting. When nodesize is too large, the trees in the forest become too simple and lose the ability to capture important patterns in the data, leading to poor performance on test data.


