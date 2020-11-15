# Overview Of Supervised Learning
The goal is to use inputs to predict the values of outputs. 

Inputs:
* Predictors
* Independent variables
* Features

Ouputs
* Responses
* Dependent variables

## Variable types and terminology
### Quantitative
The prediction task is named regression. 
### Qualitative
* Also named:
  * Categorical
  * Discrete
  * Factors

* The prediction task is named classification. 
* Usually represented numerically by codes. 
In a binomial distribution, they are represented by 0 or 1, -1 o 1.

When there are more than 2 categories, there are several alternatives. 
* Dummy variables
  * K-level qualitative variables is represented by a vector of K vinary variables, or bits, only one is "on" at a time.   
### Ordered Categorical
  * Ordering between the values, but no metric notion. 

We will typically denote an input variable by $X$. If $X$ is a vector, its components can be accessed by $X_j$. Quantitative outputs will be denoted by $Y$, and qualitative outputs by $G$ (for group). Uppercase refer to the generic aspects of a variable. Observed values are written in lowercase; 

Given the value of an input vector $X$, make a good prediction of the output $Y$, denoted by $\hat{Y}$. If $Y$ takes values in $\real$ then so should $\hat{Y}$; likewise for categorical outputs, $\hat{G}$ should take values in the same set $G$ associated with G. 

For two-class $G$, one approach is to denote the binary coded target as $Y$, then treat it as a quantitative output. The prediction $\hat{Y}$ will typically lie in $[0,1]$, and we can assign to $\hat{G}$ the classs label wether $\hat{y}>0.5$. 

We need data to construct prediction rules, often a lot of it. We thus suppose we have available a set of measurements $(x_1,y_1)$ or $(x_1,g_1)$, $i=1,...,N$, known as training data, with which to contruct our prediction rule. 

## Two simple approaches to prediction: Least Squares and Nearest Neighbors
### Linear models and Least Squares
Given a vector of inputs $X^T=(X_1, X_2,...,X_p)$, we predict the output of $Y$ with the model. 
> $\hat{Y}=\hat{\beta_0}+\sum_{j=1}^{p} X_j \hat{\beta_j}$

The term $\hat{\beta_0}$ is the intercept, also known as the bias in ML. Often it is convenient to include the constant variable 1 in $X$, include $\hat{\beta_0}$, and then write the linear model in vector for as an inner product 
> $\hat{Y}=X^T\hat{\beta}$

where $X^T$ denotes vector or matrix transpose ($X$ is being a column vector). 