📌 Overview

# Linear Regression-: 
It is used to find the relationship between Independent variables and dependent variables. The equation of the linear regression is y = mx + c. 
Where,  
  y = dependent variable (the outcome or the output)
  m = slope 
  x = independent variable (the input)
  c = intercept.

In Linear regression, OLS (Ordinary Least Square) Algorithm is used to find the best fit linear for our model. OLS is also called a Normal Equation.

# PCA -:
Principal Components Analysis is performed mainly to reduce the number of features in a dataset while retaining as much important information (variance) as possible. 

The steps for the PCA is -:
a) Prepare the data
b) Standardised the data so that features with larger numerical scales don't dominate the PCA (mean = 0, std = 1).
c) Calculate the co-variance matrix (examine how feature vary together, and describe the relationship between features).
d) Calculate the eigen vector and eigen values -> Vector for the direction of the principal components and values amount of variance capture for each components.
e) Sort the principal components -: Sorted the principal from largest to smallest.
f) Select the number of components.
g) Transform the data using the fit_transform.
h) Analyze the explained variance.
