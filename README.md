# Gradient Descent from Scratch: A Practical Comparison of Batch, SGD, and Mini-Batch GD

## Project Overview
This project demonstrates how different optimization algorithms train a Linear Regression model to predict employee salaries based on years of experience.

Rather than relying only on Scikit-Learn's built-in models, the project implements Gradient Descent algorithms from scratch to better understand the mathematics behind machine learning optimization.

The primary objective is not only to build a prediction model but also to understand **how machine learning models learn their parameters** through iterative optimization.


                    Linear Regression Optimization

                          Salary Dataset
                                │
                                ▼
                      Train / Test Split
                                │
                                ▼
                       Feature Standardization
                                │
          ┌─────────────────────┼──────────────────────┐
          ▼                     ▼                      ▼
 LinearRegression          Batch GD              SGD (Scratch)
      (Sklearn)            (Scratch)              (Scratch)
          │                     │                      │
          └──────────────┬──────┴──────────────┬───────┘
                         ▼                     ▼
                 Mini-Batch GD          Sklearn SGD
                    (Scratch)
                         │
                         ▼
             Compare R² • Loss • Time • Parameters



## Business Problem

Suppose an HR department wants to estimate the salary of a new employee based on their years of experience.
Instead of manually deciding salaries, historical employee data can be used to learn the relationship between experience and salary.

This project answers questions such as:
- Does experience significantly influence salary?
- How much does salary increase as experience increases?
- Can we estimate the salary of future employees using historical data?

## Project Objectives
In this project, I:
- Built a baseline Linear Regression model using Scikit-Learn.
- Implemented **Batch Gradient Descent** from scratch.
- Implemented **Stochastic Gradient Descent (SGD)** from scratch.
- Implemented **Mini-Batch Gradient Descent** from scratch.
- Compared the custom implementations with Scikit-Learn implementations.
- Evaluated model performance using R².
- Compared training time.
- Visualized and interpreted loss curves.
- Explained the mathematical intuition behind Gradient Descent.

## Dataset

**Dataset:** Salary Dataset
**Features**
- Years of Experience
**Target**
- Salary
The dataset is intentionally simple so the focus remains on understanding optimization rather than complex feature engineering.

## Optimization Algorithms Compared

### 1. Linear Regression (Scikit-Learn)
Uses the analytical least-squares solution (Normal Equation / Linear Algebra).

### 2. Batch Gradient Descent (Scratch)
Updates model parameters after calculating the gradient using the entire training dataset.

### 3. Stochastic Gradient Descent (Scratch)
Updates model parameters after processing one training example at a time.

### 4. Mini-Batch Gradient Descent (Scratch)
Updates parameters after processing small batches of observations.

### 5. Scikit-Learn SGDRegressor
Used as a benchmark implementation of Stochastic Gradient Descent.

## Workflow

1. Load dataset
2. Perform exploratory analysis
3. Split data into training and testing sets
4. Standardize features
5. Train Linear Regression model
6. Implement Batch Gradient Descent
7. Implement Stochastic Gradient Descent
8. Implement Mini-Batch Gradient Descent
9. Compare all optimization methods
10. Analyze loss curves
11. Interpret results in both technical and business contexts

## Results
| Model | R² Score |
|---------|----------|
| Linear Regression | 0.8887 |
| Batch Gradient Descent | 0.8887 |
| Scratch SGD | 0.8845 |
| Scikit-Learn SGD | 0.8883 |
| Scratch Mini-Batch GD | 0.8831 |
| Scikit-Learn Mini-Batch GD | 0.8802 |

The results show that all optimization techniques successfully learned nearly the same relationship between years of experience and salary.

## Key Findings

- Batch Gradient Descent produced results almost identical to Scikit-Learn's Linear Regression model, validating the custom implementation.
- Stochastic Gradient Descent achieved comparable predictive performance while updating parameters one observation at a time.
- Mini-Batch Gradient Descent provided a balance between the stability of Batch GD and the speed of SGD.
- Although the optimization paths differed, all methods converged to similar model parameters.
- The loss curves clearly illustrate how different optimization algorithms approach the minimum loss.

## Understanding the Loss Curves

The loss curve tracks the Mean Squared Error (MSE) during training.
- All algorithms begin with a high loss because the initial model parameters are poor.
- As training progresses, the loss decreases, indicating that the model is learning.
- Batch Gradient Descent shows a smooth and stable convergence.
- Stochastic Gradient Descent exhibits more fluctuations because it updates the model after every individual observation.
- Mini-Batch Gradient Descent balances convergence speed and stability.
- Eventually, all algorithms converge to a similar minimum loss.

## Business Interpretation

This project demonstrates that years of experience is a strong predictor of salary.

The trained model indicates:
- Employees with more experience generally earn higher salaries.
- Approximately **89%** of salary variation can be explained by years of experience alone.
- The model can assist HR teams in estimating salaries for new employees using historical data.

## Skills Demonstrated
- Linear Regression
- Optimization Algorithms
- Batch Gradient Descent
- Stochastic Gradient Descent (SGD)
- Mini-Batch Gradient Descent
- Machine Learning Mathematics
- Loss Functions
- Model Evaluation
- NumPy
- Pandas
- Matplotlib
- Scikit-Learn
- Object-Oriented Programming (OOP)

## Future Improvements

Possible extensions to this project include:
- Implement Momentum Gradient Descent
- Implement RMSProp
- Implement Adam Optimizer
- Apply optimization algorithms to Multiple Linear Regression
- Compare convergence on larger real-world datasets
- Deploy the trained model using Streamlit
- 
## Author
**Naiya Khalid**

This project was created as part of my machine learning learning journey to understand optimization algorithms beyond simply using Scikit-Learn.
