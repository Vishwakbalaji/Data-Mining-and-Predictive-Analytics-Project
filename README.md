# 🔥 Employee Burnout Prediction

This project was developed for my final semester course **Data Mining and Predictive Analytics**. The objective was to build predictive models that estimate employee burnout scores based on demographic, role-based, and mental health-related features. By leveraging both **Linear Regression** and **K-Nearest Neighbors (KNN)** algorithms, I explored how both linear and non-linear models perform in a real-world HR analytics use case.

---

## 📂 Dataset
- Source: [Kaggle - Employee Burnout Dataset](https://www.kaggle.com/code/mazharjamdar/employee-burnout/input?select=train.csv)
- Edited down to ~10,000 entries to meet licensing and platform constraints
- Includes features like **Gender**, **Designation**, **Mental Fatigue Score**, **Resource Allocation**, **WFH Setup**, and more
- Target variable: **Burn_Rate**

---

## 🛠️ Tools & Libraries
- Microsoft Excel with **Analytics Solver**
- Models: **KNN Regression** and **Linear Regression**
- Data cleaning, PCA, dummy variable conversion performed manually and using Excel functions

---

## 🔄 Workflow

### 1. Data Cleaning & Preprocessing
- Dropped non-informative columns like `Employee_ID`, `Date_of_Joining`
- Filled missing values:
  - Numerical: mean imputation
  - Categorical: mode imputation
- Removed rows with missing target (`Burn_Rate`)
- Converted categorical variables into dummy variables

### 2. Feature Selection and Dimensionality Reduction
- Applied **Principal Component Analysis (PCA)** to reduce dimensions
- Top 5 components used:
  - `Mental_Fatigue_Score`
  - `WFH_Setup_Available_Yes`
  - `Gender_Female`
  - `Company_Type_Service`
  - `Designation`
- Explained variance >98%

### 3. Model Development
- Two algorithms applied: **Linear Regression** and **KNN Regression**

#### Linear Regression:
- 6 different models trained using various train/test splits
- Best model selected based on highest Validation R² and lowest RMSE

#### KNN Regression:
- Tried with 3NN and 5NN
- Partitioned using 60/40, 70/30, 80/20 splits
- Evaluated all six combinations and selected the best

### 4. Model Evaluation
- Metrics used:
  - **R² (Coefficient of Determination)**
  - **Root Mean Squared Error (RMSE)**
- Best Linear Regression: **86% accuracy**
- Best KNN: **83% accuracy**

### 5. Model Scoring on New Data
- Both selected models were deployed on a separate test dataset with 50 rows
- Predictions compared to actual scores

---

## 📈 Results Summary

| Algorithm         | Validation R² | Validation RMSE | Accuracy on New Data |
|------------------|----------------|------------------|------------------------|
| Linear Regression| High (0.86)    | Low              | **86%**                |
| KNN Regression   | Moderate (0.83)| Moderate         | **83%**                |

---

## 📌 Key Takeaways

- **Linear Regression** performed better overall in both training and testing stages.
- **KNN** worked well in capturing non-linear behavior but was more sensitive to noisy features.
- **PCA** greatly reduced complexity without sacrificing accuracy.
- Handling missing values and categorical encoding were crucial steps before modeling.

---

## 📆 Project Folder Structure
```
project/
├── Employee Burnout Dataset KNN.xlsx
├── Employee Burnout Dataset LR.xlsx
├── Model Table.xlsx
├── PROJECT - Data Mining Report.docx
└── README.md
```

---

## 📢 Contact
If you're interested in HR analytics, predictive modeling, or applied regression techniques, feel free to connect with me on [LinkedIn](https://www.linkedin.com/in/vishwak-balaji-8a384018a/).
