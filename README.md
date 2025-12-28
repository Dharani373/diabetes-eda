#  Exploratory Data Analysis on Diabetes Dataset

This project performs an in-depth **Exploratory Data Analysis (EDA)** on the popular diabetes dataset to understand how different health factors relate to diabetes risk.  

The notebook walks through data cleaning, visualization, correlation analysis, and building a basic predictive model.

---

##  Objectives

✔️ Understand structure and distribution of the dataset  

✔️ Identify missing/incorrect values (hidden zeros)

✔️ Detect and analyze outliers 

✔️ Explore relationships between features and Outcome  

✔️ Visualize trends using informative plots  

✔️ Build a baseline K-Nearest Neighbors (KNN) model and evaluate performance  

---

##  Dataset

The dataset contains medical measurements of patients, including:

| Feature | Description |
|--------|-------------|
| Pregnancies | Number of pregnancies |
| Glucose | Plasma glucose concentration |
| BloodPressure | Diastolic blood pressure |
| SkinThickness | Triceps skinfold thickness |
| Insulin | Serum insulin (mu U/ml) |
| BMI | Body Mass Index |
| DiabetesPedigreeFunction | Family history score |
| Age | Age (years) |
| Outcome | 1 = Diabetic, 0 = Non-diabetic |

> Some columns may contain **0 values that are not biologically valid**, so they are treated as missing and handled accordingly.

---

##  Key EDA Steps

###  Data Inspection
- Checked dimensions, datatypes, summary statistics
- Verified missing values and duplicates
- Identified invalid zero-entries in medical fields

###  Data Cleaning
- Replaced biologically impossible zeros in the dataset
- Handled them using median imputation

###  Visualization
- Outcome distribution plots  
- Histograms of features  
- Boxplots (outlier inspection)  
- Pair plots for relationships  
- Correlation heatmap

### Insights (Highlights)
- Higher **Glucose** and **BMI** are strongly associated with diabetes  
- Weak pairwise correlations → diabetes is multi-factor  
- Outliers exist but many represent real health extremes  

---

##  Modeling (Baseline)

A simple **K-Nearest Neighbors (KNN)** classifier was built:

- Data split into train/test (with stratification)
  
- Standard scaling applied **after** splitting
  
- Tuned optimal `k`
  
- Evaluated using:
- Accuracy
- Confusion matrix
- Precision / Recall
- Classification report

>  Special focus on **recall**, since missing diabetic cases is more harmful than false positives.

---

##  Tech Stack

- Python
- Pandas, NumPy
- Matplotlib, Seaborn
- Scikit-learn

---
*Author* <br>
Dharani - Dharani373
