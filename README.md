# Diabetes-Prediction
Kaggle competition, data provided by Practice Fusion

The goal of this project is to build a model that identifies patients that have a diagnosis of Type 2 diabetes mellitus (T2DM). Diagnosis of T2DM is defined by a set of ICD9 codes: {'250', '250.0', 250.*0, and 250.*2} where 250.*0 means '250.00', '250.10', '250.20', ... '250.90' and 250.*2 means '250.02', '250.12', ... '250.92'. Note that ICD9 codes 250.*1 and 250.*3 are for Type I diabetes mellitus and are not to be classified. ICD9 codes are found in the table SyncDiagnosis. The datasetPracticeFusionDiabetes consist of 17 different files, 2 common files and 15 data set-specific files. They are in comma separated value (csv) format. I have uploaded the data set dictionary for a description of the table elements and for a chart showing how the tables are connected.

# Analysis:

1. There were a total of 9,948 patients in the data. I used the first 6,600 patients for training set and the remaining for test set. 
![Alt text](ETL.png?raw=true "ETL.png")

2. The file training_SyncPatient.csv had an indicator column to show who has a diagnosis of Type 2 diabetes mellitus. 
Used training data to do exploratory data analysis (distribution for diabetes based on male/female, smoking/non-smoking, age, and other data)
![Alt text](EDA.png?raw=true "EDA.png")

3. Used training data to build predictive models and used the test data to evaluate the models. Used Brier score to evaluate models performance 
![Alt text](Modelling.png?raw=true "Modelling.png")

# Insights:

1. Diabetes Mellitus mostly affects patients in age group 55-75, predominant in males with age group 70

2. Type 2 diabetes occurs most to Inactive people who are obese/overweight. Weight gain is a major cause and hence our models indicate that maxBMI has a higher predictive power.

3. The ICD9 data is rich. There is information in the hierarchy of the codes that provides information regarding the health of the individual's family and information regarding the individual's behavior, the diagnosis conditions that are associated with each of the codes.
 
4. An initial look at raw data indicates diabetes was much more prevalent in female than male but when fitting the model, the gender didn’t have a greater impact (no high predictive power). This could have been due to the comorbidities associated to gender.
