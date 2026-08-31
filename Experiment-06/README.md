# Experiment 6 – Dimensionality Reduction and Model Evaluation (With and Without PCA)

## Aim

To study the effect of dimensionality reduction using Principal Component Analysis (PCA) on the performance of different machine learning classification models.

## Dataset

The Breast Cancer dataset was used for the experiment. The dataset contains 569 samples with 30 numerical features. The target consists of two classes: malignant and benign.

## Models Used

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

## Implementation

- Loaded and preprocessed the dataset.
- Checked the dataset for missing values and duplicate rows.
- Standardized the features using StandardScaler.
- Split the dataset into training and testing sets.
- Applied PCA while retaining 95% of the variance.
- Trained all the models using the original feature space.
- Trained the same models after applying PCA.
- Performed hyperparameter tuning for the models.
- Used 5-fold cross-validation for model validation.
- Compared the performance of models with and without PCA.

## Evaluation

The models were evaluated using:

- Accuracy
- Precision
- Recall
- F1 Score
- ROC-AUC
- Confusion Matrix
- ROC Curve
- Precision-Recall Curve

The cross-validation results were recorded for both No-PCA and With-PCA settings and compared to observe the effect of dimensionality reduction on model performance.

## Learning Outcomes

- Understood the working and purpose of Principal Component Analysis.
- Learned how dimensionality reduction affects machine learning models.
- Performed hyperparameter tuning and 5-fold cross-validation.
- Compared model performance with and without PCA.
