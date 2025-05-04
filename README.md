# 🚗 Vehicle Crash Severity Prediction using Machine Learning

This repository contains the source code, data processing steps, and results for the course project **"Improving Vehicle Crash Severity Prediction Using Machine Learning Models"** developed for **DATA 532** at the University of North Dakota under the instruction of **Dr. Rajesh Godasu**.

---

## 📌 Project Overview

Crash severity prediction is crucial for proactive road safety management and emergency planning. However, challenges such as inconsistent data collection and extreme class imbalance reduce the generalizability of traditional models.

This project addresses these issues through:
- A **standardized feature mapping** process
- Advanced **class imbalance handling**
- A **stacked ensemble modeling framework** to enhance prediction accuracy

---

## 🧰 Methodology

### 1. Data Collection and Preprocessing
- **Raw dataset**: 147,615 rows × 43 features
- **Cleaned dataset**: 56,105 rows × 27 features
- **Steps involved**:
  - Data cleaning
  - Feature engineering and selection
  - Encoding and scaling

### 2. Class Imbalance Handling
- **Minority Downsampling**: Reduces majority class (PDO), but risks information loss
- **SMOTE**: Generates synthetic samples for underrepresented classes

### 3. Machine Learning Models Tested
- Logistic Regression (LR)
- Random Forest (RF)
- K-Nearest Neighbors (KNN)
- Decision Tree (DT)
- Gradient Boosting (GB)
- Extra Trees (ET)
- Bagging Classifier

### 4. Stacked Model Architecture
- **Base Learners**: Provide class probabilities
- **Meta Learner**: Trains on base model outputs to improve accuracy
- **Final Pipeline**: Combines preprocessing, base learners, and meta-model using Scikit-learn pipeline

### 5. Evaluation Metrics
- **Precision**
- **Recall**
- **F1-Score**
- **Matthews Correlation Coefficient (MCC)**

---

## 📈 Results Summary

- **SMOTE** outperforms downsampling in preserving data while balancing classes
- **Stacked model** achieves highest accuracy and balanced performance
- **Pipeline integration** ensures reproducibility and consistent execution

---

## 📁 Repository Structure

