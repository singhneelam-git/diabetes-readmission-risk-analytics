# Diabetes Patient Outcomes & Hospital Readmission Risk

## Project Overview

This project analyses hospital encounters for patients with diabetes and develops machine learning models to predict the likelihood of hospital readmission.

The project combines **Python, exploratory data analysis, machine learning and Power BI** to investigate patient characteristics, clinical factors and readmission patterns.

The overall objective is to demonstrate how healthcare data can be transformed into analytical insights and predictive risk information that could support hospital resource planning and patient-risk monitoring.

---

## Business / Healthcare Scenario

Hospitals need to understand which patients may be at higher risk of returning to hospital after discharge.

A better understanding of readmission patterns can help healthcare organisations:

* Identify patients who may require additional follow-up
* Understand factors associated with readmission
* Support targeted discharge planning
* Prioritise patients for additional monitoring
* Improve resource allocation
* Explore opportunities to reduce avoidable readmissions

This project demonstrates how an analytics workflow could support these objectives.

---

## Dataset & Source

The dataset used in this project was obtained from **Kaggle**.

**Dataset:** Diabetes 130-US Hospitals for Years 1999–2008

The dataset contains hospital encounter information for patients with diabetes across 130 US hospitals over the period 1999–2008.

The original dataset includes information relating to:

* Patient demographics
* Hospital encounters
* Admission and discharge information
* Medical specialties
* Diagnoses
* Medications
* Procedures
* Laboratory tests
* Previous hospital visits
* Diabetes-related information
* Readmission outcomes

**Source:** Kaggle

The dataset is used for educational and portfolio analysis. The data source is external; the data preparation, exploratory analysis, feature engineering, machine learning modelling, risk analysis and visualisation performed in this project are part of this portfolio project.

> **Data privacy note:** The dataset is a publicly available de-identified healthcare dataset. No personally identifiable patient information is intentionally used in this project.

---

## Project Objectives

The project aims to:

* Understand the characteristics of the patient population
* Explore patterns associated with hospital readmission
* Identify important patient and clinical features
* Prepare healthcare data for machine learning
* Build classification models to predict readmission risk
* Compare different machine learning approaches
* Identify important predictive features
* Segment patients according to predicted risk
* Communicate findings through Power BI
* Translate analytical findings into practical healthcare insights

---

## Project Workflow

```text
Kaggle Dataset
      ↓
Data Cleaning & Preparation
      ↓
Exploratory Data Analysis
      ↓
Feature Engineering
      ↓
Machine Learning
      ↓
Model Evaluation
      ↓
Readmission Risk Prediction
      ↓
Feature Importance
      ↓
Power BI Dashboard
      ↓
Healthcare Insights & Recommendations
```

---

## Data Cleaning & Exploratory Analysis

The first stage combines data cleaning, preparation and exploratory analysis.

Key activities include:

* Dataset inspection
* Missing-value investigation
* Data-quality checks
* Data type handling
* Feature preparation
* Categorical variable analysis
* Numerical variable analysis
* Readmission distribution analysis
* Patient demographic analysis
* Clinical feature exploration
* Identification of potential predictors of readmission

The dataset used for modelling contained approximately:

**101,766 patient encounters**

The modelling dataset contained approximately:

**40 features**

---

## Readmission Analysis

The project investigates hospital readmission as the main target outcome.

The analysis considers the relationship between readmission and factors such as:

* Age
* Gender
* Race
* Admission type
* Discharge disposition
* Previous inpatient visits
* Previous emergency visits
* Previous outpatient visits
* Number of diagnoses
* Number of medications
* Medical specialty
* Diabetes-related indicators
* Clinical and hospital encounter characteristics

The analysis is intended to identify patterns that could be useful for patient-risk assessment.

---

# Machine Learning

Three classification models were developed:

* Logistic Regression
* Random Forest
* Gradient Boosting

The models were evaluated using:

* Accuracy
* Precision
* Recall
* F1 Score
* ROC-AUC

---

## Model Performance

The recorded model results were:

| Model               | Accuracy |    ROC-AUC |
| ------------------- | -------: | ---------: |
| Logistic Regression |   63.60% |     68.27% |
| Random Forest       |   62.80% |     67.33% |
| Gradient Boosting   |   63.78% | **68.87%** |

### Best Model

Based on ROC-AUC, **Gradient Boosting** achieved the strongest overall performance:

**ROC-AUC: 68.87%**

This indicates that the model provides useful predictive signal, although performance is moderate and there is considerable scope for improvement before any real-world clinical application.

---

## Why ROC-AUC Matters

ROC-AUC measures how well a model can distinguish between patients who experience the target outcome and those who do not across different classification thresholds.

For a healthcare risk-prediction problem, evaluating more than accuracy is important because the costs of false negatives and false positives may differ.

Therefore, this project considers several evaluation metrics rather than relying on accuracy alone.

---

# Feature Importance

The machine learning analysis includes feature-importance analysis to investigate which variables contribute most strongly to model predictions.

Feature importance can help translate a machine learning model into more interpretable business and healthcare insights.

The analysis focuses on identifying variables that may be useful when assessing patient readmission risk.

> Feature importance should not be interpreted as proof that a variable directly causes readmission. Predictive importance and causal importance are different concepts.

---

# Patient Risk Prediction

The machine learning stage generates predicted readmission risk for patients.

Patients can then be grouped into different risk categories to support easier interpretation and prioritisation.

A risk-based approach could allow healthcare teams to focus additional attention on patients identified as potentially higher risk.

The model should be treated as a **decision-support and analytical demonstration**, rather than an autonomous clinical decision-making system.

---

# Power BI Dashboard

The planned Power BI dashboard translates the analytical and machine learning results into an interactive healthcare reporting solution.

The dashboard is designed around several business questions.

### 1. Executive Overview

Provides high-level KPIs such as:

* Total patient encounters
* Readmission rate
* High-risk patients
* Patient demographics
* Overall readmission distribution

### 2. Patient Demographics

Explores:

* Age distribution
* Gender
* Race
* Patient population
* Admission characteristics

### 3. Readmission Analysis

Investigates:

* Readmission by age
* Readmission by admission type
* Readmission by discharge disposition
* Readmission by number of diagnoses
* Readmission by previous hospital utilisation

### 4. Risk Analysis

Focuses on:

* Patient risk categories
* High-risk patient counts
* Risk distribution
* Predicted readmission probability
* Important predictive features

### 5. Clinical Insights

Explores relationships between:

* Diagnoses
* Medications
* Previous encounters
* Hospital utilisation
* Readmission outcomes

### 6. Model Performance

Communicates:

* Model comparison
* Accuracy
* Precision
* Recall
* F1 Score
* ROC-AUC
* Feature importance
* Model limitations

---

# Healthcare Insights

The analysis demonstrates how patient history and hospital utilisation data can be used to identify patterns associated with readmission.

Potential areas for intervention could include:

### Targeted Follow-Up

Patients predicted to have elevated readmission risk could potentially receive additional post-discharge follow-up.

### Discharge Planning

Higher-risk patients could be considered for more structured discharge planning and follow-up pathways.

### Resource Prioritisation

Risk scoring could potentially help healthcare teams prioritise limited follow-up resources.

### Monitoring Previous Utilisation

Previous inpatient, emergency and outpatient encounters may provide useful information when assessing future readmission risk.

### Data-Driven Patient Monitoring

A predictive analytics workflow could support earlier identification of patients who may require additional attention.

These recommendations are analytical suggestions and should not be interpreted as clinical guidance.

---

# Tools & Technologies

| Tool                 | Purpose                                    |
| -------------------- | ------------------------------------------ |
| Python               | Data cleaning, EDA and machine learning    |
| Pandas               | Data manipulation                          |
| NumPy                | Numerical analysis                         |
| Matplotlib / Seaborn | Data visualisation                         |
| Scikit-learn         | Machine learning                           |
| Jupyter Notebook     | Analytical workflow                        |
| Power BI             | Dashboard and reporting                    |
| GitHub               | Version control and portfolio presentation |

---

# Key Skills Demonstrated

This project demonstrates practical experience with:

* Data cleaning
* Exploratory data analysis
* Healthcare analytics
* Data preparation
* Feature engineering
* Classification modelling
* Logistic Regression
* Random Forest
* Gradient Boosting
* Model evaluation
* ROC-AUC analysis
* Feature importance
* Risk prediction
* Data visualisation
* Power BI
* Business and healthcare storytelling

---

# Project Limitations

This project has several important limitations.

### Dataset Limitations

The dataset covers hospital encounters from **1999–2008**, so the healthcare environment represented may not reflect modern clinical practice.

The dataset is also externally sourced from Kaggle and is being used for educational portfolio purposes.

### Modelling Limitations

The model performance is moderate, with the best recorded ROC-AUC being **68.87%**.

Further work could investigate:

* Hyperparameter optimisation
* Feature selection
* Class imbalance strategies
* Probability calibration
* Cross-validation
* Alternative modelling approaches
* Explainable AI techniques
* External validation

### Clinical Limitations

This model is **not a clinical decision-making tool**.

Before a predictive model could be considered for real healthcare use, it would require extensive validation, clinical review, governance, fairness assessment, monitoring and regulatory consideration.

---

# Project Outcome

This project demonstrates an end-to-end healthcare analytics workflow:

**Kaggle Dataset → Data Cleaning → EDA → Feature Engineering → Machine Learning → Risk Prediction → Model Evaluation → Power BI → Healthcare Insights**

The project shows how historical healthcare data can be transformed into descriptive and predictive insights while recognising the limitations and responsibilities associated with healthcare analytics.



## Author

**Neelam Singh**


