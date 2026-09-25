📌 Overview

This project covers two important machine-learning techniques: Linear Regression and Principal Component Analysis (PCA).

📈 Linear Regression

Linear Regression is a supervised machine-learning algorithm used to model the relationship between one or more independent variables (features) and a dependent variable (target).

For simple linear regression, the equation is:

𝑦
=
𝑚
𝑥
+
𝑐

Where:

y = Dependent variable (output or predicted value)

x = Independent variable (input feature)

m = Slope of the line

c = Intercept

The objective of Linear Regression is to find the best-fitting line that represents the relationship between the input and output variables.

Ordinary Least Squares (OLS)

Ordinary Least Squares (OLS) is a method used to estimate the coefficients of a linear regression model.

OLS finds the line that minimises the sum of the squared differences (residuals) between the actual values and the predicted values.

In matrix form, the coefficients can be calculated using the Normal Equation:

𝛽
=
(
𝑋
𝑇
𝑋
)
−
1
𝑋
𝑇
𝑦

🔬 Principal Component Analysis (PCA)

Principal Component Analysis (PCA) is an unsupervised dimensionality-reduction technique.

PCA is mainly performed to reduce the number of features in a dataset while retaining as much important information (variance) as possible.

Instead of selecting existing features, PCA creates new features called principal components. These components are combinations of the original features and are ordered according to the amount of variance they capture.

Steps for PCA

a) Prepare the data
Prepare the dataset by selecting the relevant features and handling any necessary preprocessing.

b) Standardise the data
Standardise the features so that variables with larger numerical scales do not dominate the PCA.

The standardised data has approximately:

Mean = 0

Standard deviation = 1

c) Calculate the covariance matrix
Calculate the covariance matrix to examine how the features vary together and understand the relationships between the features.

d) Calculate the eigenvectors and eigenvalues
Calculate the eigenvectors and eigenvalues from the covariance matrix.

Eigenvectors represent the directions of the principal components.

Eigenvalues represent the amount of variance captured by each principal component.

e) Sort the principal components
Sort the principal components according to their eigenvalues, from largest to smallest.

The component with the largest eigenvalue captures the most variance.

f) Select the number of components
Select the number of principal components to retain based on how much of the original variance needs to be preserved.

For example:

pca = PCA(n_components=3)


This keeps the first three principal components.

g) Transform the data
Transform the original data into the new principal-component space using fit_transform().

X_pca = pca.fit_transform(X)


This produces the reduced dataset.

h) Analyse the explained variance
Analyse the amount of variance captured by each principal component.

pca.explained_variance_


The explained variance ratio shows the proportion of the total variance captured by each component:

pca.explained_variance_ratio_


For example:

PC1 → 60%
PC2 → 25%
PC3 → 10%


The first three components therefore retain:

60% + 25% + 10% = 95%


of the total variance.

🔄 Overall Workflow
Linear Regression
Input Features
      ↓
Linear Regression
      ↓
Best-Fit Line
      ↓
Predicted Output
      ↓
Model Evaluation

PCA
Original Dataset
      ↓
Prepare Data
      ↓
Standardise Data
      ↓
Covariance Matrix
      ↓
Eigenvalues & Eigenvectors
      ↓
Sort Components
      ↓
Select Components
      ↓
Transform Data
      ↓
Reduced Dataset
      ↓
Analyse Explained Variance
