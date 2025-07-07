# 🩺 Chronic Kidney Disease Detection using Optimized Machine Learning Framework

This project demonstrates an optimized machine learning pipeline for early and accurate detection of Chronic Kidney Disease (CKD). It includes multiple feature selection techniques, classifiers, and ensemble models to achieve the best prediction accuracy.

## 📁 File Structure

- `Detection of Chronic Kidney Disease.py`: Main script containing data preprocessing, feature selection, model training, evaluation, and results.
- `kidney_disease.csv`: CKD dataset from UCI ML repository.
- `requirements.txt`: Python dependencies.
- `README.md`: Project documentation.

## 📊 Dataset

- Source: [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/datasets/Chronic_Kidney_Disease)
- Instances: 400
- Features: 24 medical attributes + 1 class label

## ⚙️ Techniques Used

### Feature Selection:
- Correlation-based Feature Selection (CFS)
- Wrapper-based Feature Selection (WFS)
- LASSO
- Permutation Importance (via ELI5)
- SHAP-based Feature Importance

### Sampling:
- SMOTE
- ADYSON
- Comparison with no balancing

### Classifiers:
- K-Nearest Neighbors (KNN)
- Decision Tree (DT)
- Support Vector Machine (SVM)
- Artificial Neural Network (ANN)

### Ensemble Methods:
- Bagging
- Boosting
- Stacking (with Logistic Regression as Meta-Model)

### 🔍 Feature Importance Analysis:
-Permutation Importance was used to determine the impact of each feature by randomly shuffling feature values and observing model performance drop.
-SHAP was used to visualize and explain feature contributions for complex models. SHAP summary plots help understand global and local interpretability.

## 🏆 Results

| Technique       | Model                 | Accuracy   |
|----------------|------------------------|------------|
| Wrapper FS      | KNN (k=3), DT         | 98.75%     |
| SMOTE + Full FS | DT, SVM (Linear + L1) | 98.75%     |
| Ensemble        | Stacking (LogReg)     | **100%**   |
