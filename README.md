# Bootstrapping-and-Boosting

## 1. Bootstrapping
<img width="545" alt="Screenshot 2024-01-09 at 10 33 22 PM" src="https://github.com/ColleenJung/Bootstrapping-and-Boosting/assets/119357849/0fc1acb6-84cb-41d1-98af-a386e0985042">

This is a resampling method that uses random sampling **with replacement**.


## 2. Bagging (**B**tstrap+**agg**regating )
<img width="599" alt="Screenshot 2024-01-09 at 10 33 35 PM" src="https://github.com/ColleenJung/Bootstrapping-and-Boosting/assets/119357849/a540bf6b-d5b7-4510-86f8-261bf2fefcde">

Bagging, which is short for bootstrap aggregating, is an ensemble learning technique that helps to improve the performance and accuracy of machine learning algorithms.
<img width="731" alt="Screenshot 2024-01-09 at 10 38 02 PM" src="https://github.com/ColleenJung/Bootstrapping-and-Boosting/assets/119357849/771d4afa-80b4-49f4-9d18-cd00403b71a2">


## 3. Boosting
<img width="617" alt="Screenshot 2024-01-09 at 10 34 20 PM" src="https://github.com/ColleenJung/Bootstrapping-and-Boosting/assets/119357849/05f9d08f-7a97-4111-8da3-6df3171e9079">

In this process, each individual model is built sequentially by iterating over the previous model. 
Boosting algorithms are a type of ensemble technique that combines the predictions of several weak learners to generate a more accurate and robust model. 
The main idea behind boosting is to iteratively train weak learners, adjusting the weights of misclassified instances at each step to focus on difficult examples.

## Types of Boosting

**1.AdaBoost (Adaptive Boosting)**
It works by training a sequence of weak learners, where each learner focuses on correcting the mistakes made by its predecessor. 
The final prediction is obtained by combining the weighted predictions of each weak learner.

**2.Gradient Boosting**
new models are added to correct the errors made by existing models, using gradient descent to minimize the loss function, making it effective for both regression and classification tasks.

**3.XGBoost (Extreme Gradient Boosting)**
XGBoost is an optimized and more efficient implementation of gradient boosting, designed for speed and performance, which provides support for handling missing data, regularization to avoid overfitting, and can be parallelized across clusters.

## Benefits of Boosting

## Challenges of Boosting


## XGBoosting vs Random Forest
