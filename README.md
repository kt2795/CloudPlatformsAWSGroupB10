# CloudPlatformsAWSGroupB10
This repository contains all files relevant to AWS final project for Group 10 MIBA Section B.

# Navigating the Github repository
All files in folder 'All Final Project Files Group B10'
## AWS S3
Contains the folder 'aws-ml-groupb10' which is a bucket on S3, which also has three folders
### model-building
The folder contains all data for training the forecasting model - 
1. train.csv
2. features.csv
3. stores.csv
### to-predit
The folder contains files that require predictions, i.e., future dates -
1. test.csv
### output
The folder contains the output from the model post-predictions, which is
1. predictions_{current_date,current_time}.csv: Contains all our predictions
2. output_{current_date,current_time}.txt: Contains brief description such as model, MAE and cross validation average error
## AWS Sagemaker
Contains - 
1. The ipynb file, 'AWS-Final-Project-GroupB10-VerFinal-Updated.ipynb' - This is the file through which our data flows, gets train, cross validated, evaluated. Following which we run our predictions. Currently the file runs LightGBM (Light Gradient Boosting Machine) model but we have placeholder code to run KNN, ExtraTreeRegressor,RandomForestRegressor, SVM, neural networks, lasso and ridge regression.
2. IAM folder contains all the json files related to the notebook instance with respect to permissions
## AWS lambda

## AWS API Gateway Folder
Contains two files - 
1. Details about the API such protocol, integrations, authorization, stage, etc.
2. A text file containing the link which triggers a zip folder to be downloaded on the local machine with the output files
a. Predictions
b. Brief description of the model
# Project Process 
