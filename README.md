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
This folder contains all components relevant to running the lambda function on AWS
1. lambda_function.py: This is the script which runs with the event configuration as {}, since we don't require parameters to run this
2. lambda_function.txt: Same script but stored in txt file (Can be ignored for practical purposes)
3. Trigger.txt: Contains details of the trigger, API Gateway which enables getting outputs via a HTTP link
4. IAM roles folder containing necesary IAM policies with respect to lambda, trigger and S3 
## AWS API Gateway Folder
Contains two files - 
1. Details about the API such protocol, integrations, authorization, stage, etc.
2. A text file containing the link which triggers a zip folder to be downloaded on the local machine with the output files
a. Predictions
b. Brief description of the model

# Project Process
## Step 1 - Setting the S3 bucket/folders
Created a S3 bucket with three folders
1. mode-bilding/ :- For training data that would be useful for model building, training and evaluation. Note: The names of the files should be as is, 'train.csv', 'features.csv', 'stores.csv'. Any updated training process (re-training) would involve re-uploading the updated files, with the same name and the same schema
2. to-predict/ :- The necessary predictions required, the name of the file 'test.csv' will contain the same name and schema
3. output/:- This is where the model completes the pred
