# Regression Model Analysis in Python
### Comparison of different Regression models for Prediction of Target

## Introduction

The rapidly evolving field of Machine Learning provides a great opportunity to help solve the problems that seem complex and persistent. The complex algorithms in the machine enable us to perform tasks in domains which were tricky and confounding for predicting the results by drawing inferences from the past results.

Various powerful models are present for performing Regression predictions and some of the popular models are:

1. Linear/Logistic Regression
2. KNN
3. Adaboost
4. Random Forest and
5. SVM

# Project Objective

**To conduct prediction analysis on the regression dataset to compare model performance**

- **i** Correlation matrix of features, 
- **ii** Comparison on MSE, R2 for different models

**II. Cross Validation:** for the models


# Rationale for Data Selection

The data has been taken from US Data on Unemployment, Education, Population and Poverty for the year 2017. The rationale was to test if the poverty estimates could be predicted for a county if other parameters like its demography, education levels and urbanization are given. It is known that there exists a cause and effect relationship, but how strong could it be?

| **Description** | **Dataset ** |
| --- | --- | 
| **Modelling Type** | Regression | 
| **Target Description** | Poverty Rate |
| **Number of Features** | 30 | 
| **Number of Observation** | 3137 |

Variable Features - The feature variables range from continuous, categorical and nominal. In the actual data, numeric coding of the data was done along with mapping of values with the label for the categorical and nominal variables. The target variable of &#39;poverty rate&#39; is a continuous variable

# Data Processing and Transforming

The datasets had rows in thousands with around 30 features. To clean the data following techniques were done:

1. Dropping the null values: The rows that had null values in target variable were dropped
2. Since the features were present in different dataframes, they were all joined on the basis of unique id of counties

# Findings from Regression Dataset

The project was executed in Jupyter Notebook. We tested for correlation between the tables and performed backward feature elimination, shown in the figure below:

 ![alt text](https://github.com/kshitijmamgain/Regression/edit/master/Correlationmatrix.png?raw=true "Title")

As seen in the figure above the features has high collinearity with each other. It became essential to eliminate the features to get the optimized OLS regression table. The graph on the right side represents the table after BFE. The pvalues of the features is shown in the figure below.

The features were eliminated only for Linear Regression. For Adaboost and Random Forest all features were used.

 ![](data:image/

The result table for regression data set is shown below:

| Regression Type | Mean Squared Error | R2 - Test vs Predict | R2 - Train vs Predict | CV Value |
| --- | --- | --- | --- | --- |
| Linear Regression | 7.33 | 0.81 | 0.77 | 0.74 |
| KNN Regression | 9.5 | 0.75 | 0.79 | 0.68 |
| SVM Regression | 0.14 | 0.86 | 0.89 | 0.77 |
| Adaboost Regression | 8.42 | 0.78 | 0.82 | 0.77 |
| Random Forest Regression | 3.94 | 0.9 | 0.98 | 0.86 |


