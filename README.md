Vehicle Crash Severity Prediction using Machine Learning
This repository contains the source code, data processing steps, and results for a predictive modeling project titled "Improving Vehicle Crash Severity Prediction Using Machine Learning Models". The project was developed as part of the course DATA 532 under the guidance of Dr. Rajesh Godasu at the University of North Dakota.

📌 Project Overview
Accurately predicting crash severity plays a critical role in enhancing road safety and guiding emergency response. However, inconsistencies in crash data formats and severe class imbalance hinder the effectiveness and generalizability of most ML models.

This project proposes:

A standardized feature mapping framework for crash data.

Robust handling of data imbalance using SMOTE and minority downsampling.

A novel stacked ensemble model combining multiple weak learners with meta-learners to improve classification performance.

🧰 Methodology
1. Data Collection and Preprocessing
Raw crash report dataset: 147,615 rows and 43 features

Cleaned dataset: 56,105 rows and 27 features

Preprocessing included:

Feature engineering

Handling missing values

Encoding categorical features

Scaling numeric values

2. Imbalance Handling Techniques
Minority Downsampling: Reduces the majority class (PDO) to match minority classes (fatal/injury), risking data loss.

SMOTE: Synthetic oversampling for minority classes, preserving original data.

3. Machine Learning Models Tested
Logistic Regression

Random Forest

K-Nearest Neighbors

Decision Tree

Gradient Boosting

Extra Trees

Bagging Classifier

4. Stacked Ensemble Model
Combines probabilistic predictions from base learners using a meta-model (e.g., Logistic Regression or Extra Trees).

Implements a two-level learning pipeline using Scikit-learn.

Provides more accurate and balanced performance compared to individual models.

5. Evaluation Metrics
Precision

Recall

F1-Score

Matthews Correlation Coefficient (MCC)

📈 Results
SMOTE provided better performance than downsampling for minority class representation.

Stacked Model outperformed all individual classifiers in both accuracy and balance.

Reproducibility was achieved by integrating Scikit-learn pipelines and fixing random seeds.

📁 Files
data/: Processed and raw crash datasets (if included or simulated).

notebooks/: Jupyter notebooks with model development, training, and evaluation.

models/: Serialized best-performing models (e.g., .pkl).

presentation/: Final presentation slides (Data532_Presentation_SwaranjitRoy.pptx).

README.md: Project summary and documentation.

🔍 Key Takeaways
A well-designed preprocessing and feature standardization workflow can significantly reduce model subjectivity.

Hybrid stacking architectures are highly promising for imbalanced classification problems like crash severity prediction.

Proper pipeline integration enhances reproducibility and modularity in ML workflows.
