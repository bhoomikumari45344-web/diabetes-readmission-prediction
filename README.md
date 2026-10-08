# Diabetes Readmission Prediction

## Week-1 : Project Overview

This project focuses on using healthcare data analytics and machine learning to identify diabetic patients who may be at high risk of hospital readmission within 30 days of discharge.

## Problem Statement

Develop a predictive analytics framework to identify diabetic patients at high risk of readmission within 30 days of hospital discharge, enabling healthcare providers to plan timely interventions and improve patient outcomes.

## Dataset

The project will use the Diabetes 130-US Hospitals for Years 1999-2008 dataset from the UCI Machine Learning Repository. The dataset contains 101,766 hospital encounters and 47 features related to diabetic patients, including demographic information, diagnoses, medications, laboratory tests, and previous healthcare utilization.

## Project Objectives

- Identify factors associated with 30-day hospital readmission.
- Clean and preprocess the healthcare dataset.
- Perform exploratory data analysis and visualization.
- Identify important features related to readmission risk.
- Develop and evaluate machine learning classification models.
- Provide meaningful insights and recommendations based on the results.

## Methodology

The project will follow a structured data science workflow:

1. Data understanding and collection
2. Data cleaning and preprocessing
3. Exploratory data analysis
4. Feature preparation and selection
5. Machine learning model development
6. Model evaluation
7. Interpretation of results and recommendations

## Tools and Technologies

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Jupyter Notebook / Google Colab

## Project Timeline

| Week | Planned Work |
|---|---|
| Week 1 | Project planning and strategic analysis |
| Week 2 | Data extraction, cleaning and preprocessing |
| Week 3 | Exploratory data analysis and visualization |
| Week 4 | Predictive model development and evaluation |
| Week 5 | Reporting, interpretation and future strategies |

## Expected Impact

The project aims to support the early identification of diabetic patients who may have a higher risk of 30-day readmission. Such insights could help healthcare providers plan appropriate follow-up and post-discharge support.

## Limitations

The dataset represents historical healthcare records from 1999-2008 and is based on hospitals in the United States. Therefore, the findings may not directly generalize to current healthcare settings or other countries. The predictive model will be considered a decision-support tool and not a replacement for clinical judgment.

## Week 2: Data Extraction and Cleaning

In Week 2, I worked on data extraction, cleaning, and preprocessing of the diabetes healthcare dataset using Python, Pandas, NumPy, and Google Colab.

### Work Completed
- Loaded the diabetes healthcare dataset using Pandas.
- Dataset contained 101,766 records and 50 columns.
- Identified missing and unknown values.
- Converted `?` values into `NaN`.
- Removed 5 highly incomplete columns:
  - `weight`
  - `max_glu_serum`
  - `A1Cresult`
  - `medical_specialty`
  - `payer_code`
- Handled remaining missing values using `Unknown`.
- Checked duplicate records and found 0 duplicates.
- Created a binary target variable `readmitted_30`.
- Final cleaned dataset contains 101,766 rows and 46 columns.
- Final missing values: 0.
- Final duplicate rows: 0.
- 
- ### Target Distribution
- Class 0: 90,409
- Class 1: 11,357

- The cleaned dataset is ready for exploratory data analysis and visualization in Week 3.

- ## Week 3: Exploratory Data Analysis & Visualization

In Week 3, I performed Exploratory Data Analysis (EDA) and visualization on the cleaned diabetes healthcare dataset using Python, Pandas, Matplotlib, and Seaborn in Google Colab.

### Work Completed
- Analyzed the dataset containing 101,766 records and 46 columns.
- Performed descriptive statistics and data inspection.
- Analyzed the distribution of 30-day hospital readmission.
- Studied age groups and their 30-day readmission rates.
- Analyzed the distribution of hospital stay duration.
- Compared hospital stay with 30-day readmission.
- Studied previous inpatient visits and their relationship with readmission.
- Created a correlation matrix and heatmap for numerical variables.
- Created a scatter plot for hospital stay and number of medications.
- Compared 30-day readmission rates by gender.

### Key Findings
- Overall 30-day readmission rate was about 11.16%.
- Previous inpatient visits showed an increasing observed readmission-rate pattern.
- The correlation between previous inpatient visits and 30-day readmission was 0.17.
- Hospital stay and number of medications had a correlation of 0.47.
- Female and male readmission rates were very close: 11.25% and 11.06%.

The EDA results will be used for the next stage of predictive modelling.


## Week 4: Predictive Modeling and Machine Learning

In Week 4, I developed and evaluated machine learning models to predict 30-day hospital readmission risk among diabetic patients using Python, Scikit-learn, and Google Colab.

### Work Completed
- Loaded the cleaned healthcare dataset containing 101,766 records and 46 columns.
- Created the binary target variable `readmitted_30`.
- Removed identifier columns such as `encounter_id` and `patient_nbr`.
- Removed the original `readmitted` column to prevent data leakage.
- Converted categorical features using one-hot encoding.
- Split the data into 80% training and 20% testing sets using stratified sampling.
- Trained three machine learning models:
  - Logistic Regression
  - Decision Tree
  - Random Forest
- Evaluated the models using Accuracy, Precision, Recall, and ROC-AUC.
- Compared model performance using a results table and ROC curve.
- Considered class imbalance, overfitting, missing data, outliers, bias, and ethical issues.

### Model Results

| Model | Accuracy | Precision | Recall | ROC-AUC |
|---|---:|---:|---:|---:|
| Logistic Regression | 64.17% | 16.58% | 54.82% | 64.25% |
| Decision Tree | 61.19% | 16.80% | 62.70% | 65.59% |
| Random Forest | 62.66% | 16.27% | 56.58% | 64.46% |

### Key Findings
- Logistic Regression achieved the highest accuracy of 64.17%.
- Decision Tree achieved the highest recall of 62.70% and ROC-AUC of 65.59%.
- The Decision Tree showed the strongest overall performance among the three models based on recall and ROC-AUC.
- The results indicate that the models have moderate predictive ability and would require further tuning and validation before any real-world healthcare use.
- The model can potentially support identification of patients who may need closer follow-up after discharge.

The Week 4 results provide the foundation for the next stage of the project: interpreting the findings and developing practical healthcare recommendations.


## Week 5: Reporting, Interpretation & Future Strategies

In Week 5, I consolidated the complete healthcare data analytics project into a final report. The project focused on predicting 30-day hospital readmission risk among diabetic patients.

### Work Completed
- Consolidated the work completed from Week 1 to Week 4.
- Summarized the project planning, data cleaning, exploratory data analysis, and predictive modeling stages.
- Interpreted important patterns and findings from the dataset.
- Compared the performance of Logistic Regression, Decision Tree, and Random Forest models.
- Discussed data cleaning challenges, class imbalance, data leakage, missing values, outliers, and model limitations.
- Discussed the practical implications of the findings for healthcare analytics.
- Provided recommendations for future analytics projects and healthcare data management.
- Included ethical considerations and future improvement strategies.

### Final Key Findings
- The dataset contained 101,766 patient records.
- The final cleaned dataset contained 46 columns.
- The overall 30-day readmission rate was 11.16%.
- Previous inpatient visits showed an increasing observed pattern in 30-day readmission rates.
- The correlation between previous inpatient visits and 30-day readmission was 0.17.
- Hospital stay and number of medications had a correlation of 0.47.
- Logistic Regression achieved 64.17% accuracy.
- Decision Tree achieved the highest Recall of 62.70% and ROC-AUC of 65.59%.
- Random Forest achieved 62.66% accuracy and 64.46% ROC-AUC.

The final analysis suggests that machine learning can provide a baseline framework for identifying patients who may require closer follow-up after discharge. However, further feature engineering, model tuning, validation, fairness analysis, and clinical evaluation would be required before real-world healthcare deployment.

### Final Report
The complete Week 5 final report is available in this repository as:

`Week_5_Final_Healthcare_Data_Analytics_Report.docx`



