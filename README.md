# Diabetes-Prediction
Kaggle competition, data provided by Practice Fusion

The goal of this project is to build a model that identifies patients that have a diagnosis of Type 2 diabetes mellitus (T2DM). Diagnosis of T2DM is defined by a set of ICD9 codes: {'250', '250.0', 250.*0, and 250.*2} where 250.*0 means '250.00', '250.10', '250.20', ... '250.90' and 250.*2 means '250.02', '250.12', ... '250.92'. Note that ICD9 codes 250.*1 and 250.*3 are for Type I diabetes mellitus and are not to be classified. ICD9 codes are found in the table SyncDiagnosis. The datasetPracticeFusionDiabetes consist of 17 different files, 2 common files and 15 data set-specific files. They are in comma separated value (csv) format. I have uploaded the data set dictionary for a description of the table elements and for a chart showing how the tables are connected.

Analysis:

1. There were a total of 9,948 patients in the data. I used the first 6,600 patients for training set and the remaining for test set. 

2. The file training_SyncPatient.csv had an indicator column to show who has a diagnosis of Type 2 diabetes mellitus. 
Used training data to do exploratory data analysis (distribution for diabetes based on male/female, smoking/non-smoking, age, and other data)

3. Used training data to build predictive models and used the test data to evaluate the models. Used Brier score to evaluate models performance 
