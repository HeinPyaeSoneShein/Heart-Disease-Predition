# Heart Disease Prediction: A Data Mining Approach

![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)
![Scikit-Learn](https://img.shields.io/badge/Library-Scikit--Learn-orange.svg)
![Data Mining](https://img.shields.io/badge/Field-Healthcare%20Analytics-red.svg)

## 📌 Project Overview
This project implements a machine learning pipeline to predict heart disease using clinical and biochemical markers. Utilizing the **Medical Dataset** (1,319 records), the study focuses on automating the detection process to assist clinicians in early-stage diagnosis, potentially reducing the mortality rate associated with cardiac events.

## 📊 Dataset Analysis
The dataset contains 9 columns reflecting real-world clinical data:
* **Demographics:** Age, Gender.
* **Vitals:** Heart Rate, Systolic & Diastolic Blood Pressure.
* **Biochemical Markers:** Blood Sugar, **CK-MB**, and **Troponin**.
* **Target:** `Result` (Positive/Negative).

### **Key Data Insights**
* **Distribution:** 810 positive cases vs. 509 negative cases.
* **Correlation:** High correlation observed between **Troponin/CK-MB** levels and positive heart disease outcomes.
* **Integrity:** Zero missing values across all 1,319 entries.

## 🛠️ Technical Workflow

### **1. Data Preprocessing & Cleaning**
* **Outlier Mitigation:** Implemented **Interquartile Range (IQR) Capping** on all numerical features to prevent extreme clinical readings from biasing the models.
* **Feature Scaling:** Applied `StandardScaler` to ensure features like *Age* and *Blood Pressure* are on the same scale for gradient-based algorithms.
* **Categorical Encoding:** Successfully mapped Gender and diagnostic outcomes into numerical formats for model compatibility.

### **2. Exploratory Data Analysis (EDA)**
* Generated **Correlation Heatmaps** to identify multicollinearity.
* Utilized **Boxplots** to visualize Troponin distribution across disease results.
* Analyzed feature frequency using **Histograms** to understand the variance in patient vitals.

### **3. Machine Learning Implementation**
I evaluated four distinct classification algorithms to determine the most reliable diagnostic tool:
* **Logistic Regression** (Max iterations: 1000)
* **Decision Tree Classifier** (Gini Impurity)
* **Random Forest Classifier** (100 Estimators)
* **Support Vector Machine (SVM)** (Linear Kernel)

