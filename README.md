# Predicting Traffic Crash Severity Using Machine & Deep Learning

## Project Overview

This project aims to predict traffic crash severity using advanced machine learning and deep learning models. The dataset used is obtained from the North Dakota Department of Transportation (NDDOT) website. Crash data collection follows a structured process carried out by police departments and other official agencies. However, this data is often unstructured, requiring extensive preprocessing, feature engineering, and handling of missing values before it becomes usable for predictive modeling.

The project provides a **comprehensive, step-by-step framework** that demonstrates how raw crash data can be transformed into a structured dataset suitable for predictive modeling. It explores the impact of various factors such as **lighting conditions, weather, road surface conditions, speed of vehicles, driver demographics (age, gender), and alcohol/drug involvement** on crash severity. 

## **Methodology**

The project follows a rigorous data preprocessing and model development pipeline, including the following steps:

### **1. Data Preprocessing & Feature Engineering**
- The raw dataset consists of multiple categorical and numerical features that require significant transformation.
- Extensive feature engineering is performed to merge, categorize, and optimize features to improve model performance.
- Certain feature categories, such as **driver behavior, environmental conditions, vehicle speed, and violation type**, are transformed into meaningful variables.
- The final structured dataset consists of **150,000 rows**, representing individual crash incidents.

### **2. Handling Class Imbalance**
- The dataset has an inherent class imbalance, meaning that certain crash severity levels (e.g., fatal crashes) are significantly underrepresented.
- Various resampling techniques are applied to balance the classes:
  - **Undersampling:** Removing excessive majority class samples to create a balanced dataset.
  - **SMOTE (Synthetic Minority Over-sampling Technique):** Creating synthetic samples to increase the representation of minority classes.
- **SMOTE oversampling** is found to be the most effective, improving model prediction accuracy by over **45% compared to undersampling**.

### **3. Model Development**
- A novel **hybrid classification model** is developed, combining state-of-the-art machine learning algorithms.
- The hybrid model follows a **self-developed stacking ensemble structure**, integrating multiple models to achieve better predictive performance.
- The following models are trained and evaluated:
  - **Traditional ML Models:** Decision Trees, Random Forest, Gradient Boosting, XGBoost, and Support Vector Machines (SVM).
  - **Deep Learning Model:** Artificial Neural Network (ANN), which captures complex patterns in crash data.
  - **Hybrid Model:** A stacking ensemble approach combining multiple ML models to improve generalization and robustness.

### **4. Hyperparameter Tuning with Keras Tuner**
- The **ANN model is optimized using Keras Tuner**, which automates the search for the best hyperparameters.
- The hyperparameter tuning process optimizes:
  - **Number of layers & neurons**
  - **Learning rate & batch size**
  - **Activation functions**
- Using Keras Tuner significantly improves the ANN’s **classification accuracy, stability, and generalization**.

### **5. Model Evaluation Metrics**
- Model performance is assessed using multiple evaluation metrics:
  - **Precision, Recall, and F1-score:** To measure the balance between false positives and false negatives.
  - **ROC-AUC Curve:** To evaluate the classifier’s ability to distinguish between crash severity levels.
  - **Confusion Matrix Analysis:** To identify misclassifications and their impact on prediction accuracy.

## **Results & Insights**

- **SMOTE oversampling** significantly improves prediction performance by ensuring minority class representations are well-learned, resulting in a **45% increase in accuracy compared to undersampling**.
- The **hybrid stacking model outperforms traditional ML models by 12%**, demonstrating the effectiveness of combining multiple models for crash severity prediction.
- **Artificial Neural Networks (ANN) outperform traditional ML models**, showcasing the power of deep learning in handling complex datasets. However, it **performs slightly worse than the hybrid model**, indicating that a combination of traditional and deep learning techniques offers the best results.
- **Keras Tuner optimization** enhances ANN performance, but **the ANN model shows uneven accuracy across different severity classes**, especially for underrepresented categories such as fatal crashes.

## **Installation & Usage**
To replicate this project, install the necessary dependencies:

```bash
pip install numpy pandas scikit-learn imbalanced-learn tensorflow keras-tuner matplotlib seaborn
