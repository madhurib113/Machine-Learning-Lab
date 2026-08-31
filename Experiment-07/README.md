# Experiment 7 – Dimensionality Reduction and Model Evaluation

## Aim

To study the effect of dimensionality reduction using Principal Component Analysis (PCA) on the performance of different machine learning classifiers.

## Dataset

Wisconsin Diagnostic Breast Cancer dataset from scikit-learn.

- Samples: 569
- Features: 30
- Classes: Malignant and Benign
- Features are numerical
- Class distribution:
  - Benign: 357
  - Malignant: 212

## Preprocessing

The dataset was divided into training and testing sets using an 80:20 stratified split. The features were standardized using `StandardScaler`.

For the PCA case, PCA was applied after standardization with a target of 95% explained variance. This resulted in 10 components.

## Models Used

The following models were trained and compared:

- Support Vector Machine (SVM)
- Naive Bayes
- K-Nearest Neighbors (KNN)
- Logistic Regression
- Decision Tree
- Random Forest
- AdaBoost
- Gradient Boosting
- XGBoost
- Stacking

For Stacking, SVM, Naive Bayes and Decision Tree were used as base learners, with Logistic Regression as the meta learner.

## Method

Each model was trained in two settings:

1. Without PCA
2. With PCA

GridSearchCV was used for hyperparameter tuning and 5-fold cross-validation was used for model validation.

## PCA

PCA was applied after feature standardization.

- Variance target: 95%
- Components selected: 10
- Explained variance: 95.27%

A scree plot was also generated to show the explained variance.

## Evaluation

The models were evaluated using:

- Accuracy
- Precision
- Recall
- F1 Score
- ROC-AUC

Confusion matrices, ROC curves and Precision-Recall curves were also generated for selected models.

## Result

The performance of all models was compared between the original feature space and the PCA-reduced feature space.

The results show that PCA reduced the number of features while retaining most of the information. Its effect was different for different models. SVM and KNN were more affected by the change in feature space, while tree-based models could work directly with the available features.

## Files

- `ML_07.ipynb` – Python implementation and results
- `ML_07.pdf` – Experiment report
