# Hospital Readmission Prediction for Diabetic Patients

## Project Overview

This project predicts hospital readmission risk for diabetic patients using machine learning, with a focus on integrating social determinants of health and demographic context to improve upon traditional clinical-only models.

## Workflow

| Stage | Description | File/Link | Done by |
|-------|-------------|-------------|-------------|
| **Data Integration** | Merge UCI dataset with BRFSS demographic health data | [data_merging.ipynb](https://github.com/kristenlowe/hospital-readmission/blob/main/data_merging.ipynb) | Kristen |
| **Data Cleaning and Feature Engineering** | Handle missing values, create literature-based predictive features | [Data Cleaning and Feature Engineering.ipynb](https://github.com/kristenlowe/hospital-readmission/blob/f7d902f05b1ab1850e35eb754b94fa08f3ba0103/Data%20Cleaning%20and%20Feature%20Engineering.ipynb) | Varsha |
| **EDA** | Explore patterns, correlations, and disparities | [AML_EDA.ipynb](https://github.com/kristenlowe/hospital-readmission/blob/main/AML_EDA.ipynb) | Nisha |
| **Modeling and Evaluation** | Logistic regression (L1 penalty), comparison with other models, accuracy, fairness metrics, feature importance | [AML_Modeling_Evaluation.ipynb](https://github.com/kristenlowe/hospital-readmission/blob/main/AML_Modeling_Evaluation.ipynb) | Joseph |
| **Presentation** | In-class Powerpoint presentation | [Texas McCombs MSBA Advanced Machine Learning Fall 2025.pdf](https://github.com/kristenlowe/hospital-readmission/blob/main/Texas%20McCombs%20MSBA%20Advanced%20Machine%20Learning%20Fall%202025.pdf) | Zan |
| **Blog Report** | Blog-based project report | | |

## Objectives

- Predict 30-day hospital readmission risk for diabetic patients
- Identify high-utilization patients for targeted interventions
- Analyze fairness and bias across demographic subgroups
- Provide interpretable features for clinical decision-making

## Datasets

**Primary Dataset:**
- [UCI Diabetes 130-US Hospitals (1999-2008)](https://archive.ics.uci.edu/dataset/296/diabetes+130-us+hospitals+for+years+1999-2008)
- 101,766 admissions across 130 US hospitals
- 47 clinical and demographic features

**Additional Dataset (to be merged):**
- [BRFSS CDC Data](https://www.kaggle.com/datasets/lplenka/brfss-data)
- 491,775 survey responses with demographic and behavioral health data
- Features: BMI, high blood pressure, cholesterol, physical activity, smoking, income, education, healthcare access
- Aggregated by race/age/gender and merged with UCI data

## Literature-Based Features
* Polypharmacy burden (num_medications > threshold)
* Glycemic control proxy (HbA1c test performed yes/no + diabetesMed changes)
* Discharge instability score (urgent admission + high num_procedures + short stay)

