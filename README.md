# Overview:
This project  is about credit card fraud detection using Random Forest Classifier.

# Description:
The dataset used in this notebook is of 'IEEE-CIS Fraud Detection'.
Data set link:"https://drive.google.com/file/d/1q8SYcjOJULdSkETv5S_gd7xNq1GrBHAO/view"

# Steps Followed:

## Step 1:Loading libraries , dataset and getting basic idea about data.
As shown in the notebook.

## Step 2:Checking missing values and dealing with the missing values.
Here we dropped every column where the percentage of missing values are >=20% and only considered the columns/fetaures having percentage of missing values <20%.
Then we filled up the missing values for numerical fetures with the mean of the respective columns and categorical features with the mode of the respective columns.

## Step 4:One Hot Encoding (Creating dummies for categorical columns)
As shown in the notebook.

## Step 5:Dealing with the imbalance data.
Imbalanced classes are a common problem in machine learning classification where there are a disproportionate ratio of observations in each class. Class imbalance can be found in many different areas including medical diagnosis, spam filtering, and fraud detection.
Here we used SMOTE to deal with the imbalance data and make it balanced.

## Step 6:Building BaseLine Model and Evaluation.
Here we used Random Forest Classifier as our baseline model.

## Step 7:Feature Selection.
Feature selection is the process of reducing the number of input variables when developing a predictive model.It is desirable to reduce the number of input variables to both reduce the computational cost of modeling and, in some cases, to improve the performance of the model.Here we are using 'slectKBest' from 'sklearn.feature_selection' which selects features according to the k highest scores.
Obviously we can notice there is 0.7% decrease in accuracy score. The point to note is that we had got 97.5% accuracy with 250 features, then after that we selected only 10 features of 250 features and still able to get 96.9% accurate results. The conclusion is that we have reduced a lot of computational complexities which is very good as our aim is not only to increase the performance of the model at any cost but also to reduce the computational complexity of our model.

## Step 8:Cross Validation
Even with cross validation we are getting approx 96.9% of accurate results.

## Step 9: Hyper Parameter Tuning and Evaluation
Hyperparameters are important parts of the ML model and can make the model best or worse depending upon how it is used. Here we have discussed one of the popular hyperparameter tunning method i.e. using Grid Search CV.Here we are able to get approx. 96.8% accuracy.

# Conclusion:
1. We observed that the dataset contained missing values. We removed some columns and filled missing values for numerical column with mean and categorical column with mode (i.e. the maximum occuring value).
2. We observed that the dataset was imblanced. We used 'SMOTE' to generate new data to deal with the problem of imbalanced data.
3. We build Random Forest model, got accuracy score of 97.53%.
4. Then we selected only 10 most important features using selectKBest and f_classif. Here the model complexity is reduced a lot (which is very good) with very little decrease in accuracyCross Validation and Hyper 
   parameter tunning gave nearly 96.8% of accurate results which is not bad. Most of the times the default values for hyper parameters of the models are same that we get through the hyper parameter tunning. 
   That's the reason there is not much difference in normal model and tunned model.














