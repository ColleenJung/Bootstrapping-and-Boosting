# Bootstrapping-and-Boosting

## Table of Contents
- [Bootstrapping](#1.Bootstrapping)
- [Bagging](#2.Bagging)
- [Boosting](#3.Boosting)
- [Types of Boosting](#Types_of_Boosting)
- [Benefits of Boosting](#Benefits_of_Boosting)
- [Challenges of Boosting](#Challenges_of_Boosting)
- [XGBoosting vs Random Forest](#XGBoosting_vs_RandomForest)

  
## 1.Bootstrapping
<img width="545" alt="Screenshot 2024-01-09 at 10 33 22 PM" src="https://github.com/ColleenJung/Bootstrapping-and-Boosting/assets/119357849/0fc1acb6-84cb-41d1-98af-a386e0985042">

This is a resampling method that uses random sampling **with replacement**.


## 2. Bagging (**B**tstrap+**agg**regating )
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
