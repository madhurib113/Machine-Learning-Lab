# Experiment 6 – Ensemble Learning and Model Evaluation

## Aim

To study different ensemble learning methods and compare their performance on the Breast Cancer dataset.

## Dataset

The Breast Cancer dataset from scikit-learn was used for the experiment.

- Samples: 569
- Features: 30
- Classes: Malignant and Benign
- Features are numerical
- Malignant: 212
- Benign: 357

The dataset was divided into training and testing sets using an 80:20 stratified split.

- Training samples: 455
- Testing samples: 114

## Models Used

- Bagging
- AdaBoost
- Gradient Boosting
- Stacking

For Stacking, SVM, Naive Bayes and Decision Tree were used as base models and Logistic Regression was used as the meta learner.

## Implementation

- Loaded the Breast Cancer dataset
- Checked the dataset and class distribution
- Checked for missing values
- Split the dataset into training and testing sets
- Performed hyperparameter tuning using GridSearchCV
- Used 5-fold cross-validation
- Implemented Bagging
- Implemented AdaBoost
- Implemented Gradient Boosting
- Implemented Stacking
- Compared the models using test set performance
- Generated confusion matrices
- Generated ROC curves
- Generated classification report for the Stacking model

## Hyperparameter Tuning

GridSearchCV was used to find suitable parameters for the ensemble models.

### Bagging

- Number of estimators: 100
- Maximum samples: 0.8
- Maximum features: 0.5
- Best CV Accuracy: 96.04%

### AdaBoost

- Number of estimators: 100
- Learning rate: 1.0
- Best CV Accuracy: 97.36%

### Gradient Boosting

- Number of estimators: 100
- Learning rate: 0.2
- Maximum depth: 1
- Best CV Accuracy: 98.02%

## Evaluation

The models were evaluated using:

- Accuracy
- Precision
- Recall
- F1 Score
- Confusion Matrix
- ROC-AUC
- ROC Curve
- 5-fold Cross-Validation

## Results

The test set results were:

| Model | Accuracy | Precision | Recall | F1 Score |
|-------|----------|-----------|--------|----------|
| Bagging | 94.74% | 95.83% | 95.83% | 95.83% |
| AdaBoost | 95.61% | 94.67% | 98.61% | 96.60% |
| Gradient Boosting | 96.49% | 95.95% | 98.61% | 97.26% |
| Stacking | 97.37% | 97.26% | 98.61% | 97.93% |

The Stacking model gave an accuracy of 97.37% on the test set.

## Stacking

The Stacking model used:

- Base models: SVM, Naive Bayes and Decision Tree
- Meta learner: Logistic Regression
- Average CV Accuracy: 96.26%
- Average CV F1 Score: 97.03%

The confusion matrix and classification report were also generated for the Stacking model.

## Files

- `ML_06.ipynb` – Python implementation and results
- `ML_06.pdf` – Experiment report

## Dependencies

The following Python libraries are required:

- NumPy
- Pandas
- Matplotlib
- Scikit-learn
