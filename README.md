# ✈️ Flight Delay Prediction on European Airspace using Machine Learning

## 📌 Project Overview
This project focuses on predicting **flight delays** using **machine learning techniques** on a real-world flight dataset.  
The objective is to identify whether a flight is likely to be delayed based on operational, route, and time-related features.

Flight delays are a major challenge for airlines, airports, and passengers.  
By applying machine learning models, this project aims to support better planning, decision-making, and operational efficiency.

---

## 🎯 Objective
The main aim of this project is to build and compare machine learning models that can predict whether a flight will be delayed.

### Research Question
**How effectively can machine learning models predict flight delays using airline, route, and temporal features?**

---

### Key Features Used
- `AIRLINE_CODE`
- `ORIGIN`
- `DEST`
- `CRS_ELAPSED_TIME`
- `DISTANCE`
- `DIVERTED`
- `YEAR`
- `MONTH`
- `DAY`
- `DAY_OF_WEEK`
- `IS_WEEKEND`
- `CRS_DEP_HOUR`
- `CRS_ARR_HOUR`

### Target Variable
- `IS_DELAYED`
- A flight is labelled as delayed if **arrival delay > 15 minutes**

---

## ⚙️ Project Workflow

### 1. Data Loading
The dataset was imported into Python using **Pandas** for analysis and preprocessing.

### 2. Data Preprocessing
The following preprocessing steps were carried out:
- Converted date columns into proper datetime format
- Extracted temporal features such as:
  - year
  - month
  - day
  - day of week
  - weekend indicator
- Converted scheduled departure and arrival time into minutes/hours
- Removed cancelled flights
- Created a binary target variable (`IS_DELAYED`)
- Handled categorical and numerical variables using preprocessing pipelines
- Applied encoding techniques for categorical features
- Managed missing values using imputers

### 3. Exploratory Data Analysis (EDA)
EDA was performed to understand:
- dataset structure
- numeric feature statistics
- feature distributions
- delay patterns
- correlations between variables
- important factors contributing to delays

### 4. Model Building
Three machine learning models were developed and compared:
- **Logistic Regression**
- **Decision Tree Classifier**
- **XGBoost Classifier**

### 5. Model Evaluation
The models were evaluated using:
- Accuracy
- Precision
- Recall
- F1 Score
- ROC-AUC

### 6. Feature Importance
Feature importance analysis was performed to identify the most influential variables affecting delay prediction.

---

## 🤖 Models Used

### 1. Logistic Regression
A baseline classification model used to understand the relationship between features and delay prediction.

### 2. Decision Tree Classifier
A tree-based model that captures non-linear patterns and provides better interpretability.

### 3. XGBoost Classifier
An advanced boosting model used to improve predictive performance and handle complex data relationships.

---

## 📊 Evaluation Metrics
The following metrics were used to measure model performance:

- **Accuracy** – overall correctness of predictions
- **Precision** – proportion of predicted delays that were actually delayed
- **Recall** – proportion of actual delayed flights correctly identified
- **F1 Score** – balance between precision and recall
- **ROC-AUC** – ability of the model to distinguish between delayed and non-delayed flights

---

## 🏆 Best Model
Based on model comparison, the best-performing model was selected using classification metrics such as **F1-score** and **ROC-AUC**.

The project also includes:
- model comparison table
- confusion matrix
- feature importance chart

---

## 📈 Key Insights
- Temporal factors such as departure time, arrival time, month, and day of week play an important role in delay prediction
- Route-based factors such as origin, destination, and distance influence flight delays
- Airline-related operational patterns also affect the likelihood of delay
- Tree-based and boosting models performed better than simple linear models for this problem

