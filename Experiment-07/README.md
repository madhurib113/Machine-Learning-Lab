# Experiment 7 – Dimensionality Reduction and Model Evaluation

## Aim

To study the effect of dimensionality reduction using Principal Component Analysis (PCA) on the performance of different machine learning classifiers.

## Dataset

Wisconsin Diagnostic Breast Cancer dataset from scikit-learn.

- Samples: 569
- Features: 30
- Classes: Malignant and Benign
- Features are numerical
- Benign: 357
- Malignant: 212

## Preprocessing

The dataset was divided into training and testing sets using an 80:20 stratified split.

- Training samples: 455
- Testing samples: 114
- Features were standardized using `StandardScaler`
- Missing values: 0
- Duplicate rows: 0

For the PCA case, PCA was applied after standardization with a target of 95% explained variance. This resulted in 10 components with 95.27% explained variance.

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

For Stacking, SVM, Naive Bayes and Decision Tree were used as base learners and Logistic Regression was used as the meta learner.

## Method

Each model was trained in two settings:

1. Without PCA
2. With PCA

GridSearchCV was used for hyperparameter tuning and 5-fold Stratified K-Fold cross-validation was used for validation.

## PCA

PCA was applied after standardizing the features.

- Variance target: 95%
- Components selected: 10
- Explained variance: 95.27%

A cumulative explained variance plot was generated to select the number of components.

## Evaluation

The models were evaluated using:

- Accuracy
- Precision
- Recall
- F1 Score
- ROC-AUC

Confusion matrices, ROC curves and Precision-Recall curves were also generated.

## Results

The test set performance was compared between the original feature space and the PCA-reduced feature space.

| Model | No-PCA Accuracy | With-PCA Accuracy |
|-------|-----------------|-------------------|
| SVM | 98.25% | 96.49% |
| Naive Bayes | 92.98% | 92.11% |
| KNN | 96.49% | 95.61% |
| Logistic Regression | 98.25% | 97.37% |
| Decision Tree | 94.74% | 92.98% |
| Random Forest | 95.61% | 93.86% |
| AdaBoost | 95.61% | 94.74% |
| Gradient Boosting | 94.74% | 93.86% |
| XGBoost | 94.74% | 94.74% |
| Stacking | 97.37% | 93.86% |

The PCA version used only 10 components while retaining 95.27% of the variance. The effect of PCA was different for different models.

## Cross-Validation

5-fold cross-validation was also performed for both No-PCA and With-PCA settings.

The average validation accuracy was compared to check the model performance across different folds.

## Result

PCA reduced the number of features from 30 to 10 while retaining 95.27% of the variance.

The effect of PCA was different for different classifiers. In the test results, SVM and Logistic Regression gave high accuracy in both settings. XGBoost gave the same accuracy with and without PCA.

The best test accuracy in the experiment was obtained by SVM and Logistic Regression in the No-PCA setting with 98.25%.

## Files

- `ML_07.ipynb` – Python implementation and results
- `ML_07.pdf` – Experiment report

## Dependencies

The following Python libraries are required:

- NumPy
- Pandas
- Matplotlib
- Scikit-learn
- XGBoost
