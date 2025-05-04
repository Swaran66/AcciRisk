# 🚗 Improving Vehicle Crash Severity Prediction using Machine Learning Models

## 📌 Project Overview

Crash severity prediction is crucial for proactive road safety management and emergency planning. However, challenges such as inconsistent data collection and extreme class imbalance reduce the generalizability of traditional models.

This project addresses these issues through:
- A **standardized feature mapping** process
- Advanced **class imbalance handling**
- A **stacked ensemble modeling framework** to enhance prediction accuracy

## 🔍 What Makes This Project Unique

This project distinguishes itself through several innovative approaches:

- **Standardized Feature Mapping**  
  Addressing the inconsistency in crash data collected from various agencies, this project implements a standardized framework for feature mapping. This harmonization ensures that the predictive models are trained on consistent and reliable data, enhancing their generalizability.

- **Advanced Imbalance Handling Techniques**  
  Recognizing the challenge posed by the natural imbalance in crash data—where severe crashes are less frequent—the project employs both minority downsampling and SMOTE (Synthetic Minority Oversampling Technique). These methods effectively balance the dataset, allowing the models to learn from both common and rare events.

- **Stacked Ensemble Modeling**  
  The project leverages a stacked ensemble approach, combining multiple base learners with a meta-learner. This technique captures diverse patterns in the data, leading to improved predictive performance over individual models.

- **Comprehensive Evaluation Metrics**  
  Beyond traditional accuracy, the project utilizes metrics like **Precision**, **Recall**, **F1-Score**, and **Matthews Correlation Coefficient (MCC)** to provide a nuanced assessment of model performance, especially important in imbalanced datasets.

By integrating these methodologies, the project offers a robust and scalable solution for predicting crash severity, contributing valuable insights to the field of traffic safety and emergency response planning.

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


