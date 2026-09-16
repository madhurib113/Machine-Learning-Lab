# Experiment 5 – Classification using Decision Tree and Random Forest

## Aim

To classify breast cancer cases as benign or malignant using Decision Tree and Random Forest classifiers and compare their performance.

## Dataset

Wisconsin Diagnostic Breast Cancer dataset with 569 samples and 30 numerical features.

- Benign: 357
- Malignant: 212

The dataset was split into 80% training data and 20% testing data using stratification.

- Training samples: 455
- Testing samples: 114

## Models Used

- Decision Tree Classifier
- Random Forest Classifier

## Work Done

- Loaded and preprocessed the dataset
- Removed the ID column
- Encoded the diagnosis values
- Checked the class distribution
- Performed basic exploratory data analysis
- Split the dataset using stratification
- Implemented Decision Tree
- Implemented Random Forest
- Performed hyperparameter tuning using GridSearchCV
- Used five-fold Stratified K-Fold cross-validation
- Evaluated accuracy, precision, recall and F1-score
- Compared training and testing performance
- Generated confusion matrices
- Compared ROC curves
- Calculated ROC-AUC scores

## Hyperparameter Tuning

### Decision Tree

Best parameters:

- Criterion: `entropy`
- Max Depth: `5`
- Min Samples Split: `10`
- Min Samples Leaf: `2`
- Best CV Accuracy: `93.63%`

### Random Forest

Best parameters:

- Number of Estimators: `200`
- Max Depth: `5`
- Max Features: `sqrt`
- Bootstrap: `False`
- Best CV Accuracy: `97.14%`

## Cross-Validation Results

| Model | Fold 1 | Fold 2 | Fold 3 | Fold 4 | Fold 5 | Average |
|---|---:|---:|---:|---:|---:|---:|
| Decision Tree | 90.11% | 95.60% | 91.21% | 95.60% | 95.60% | 93.63% |
| Random Forest | 95.60% | 100.00% | 94.51% | 96.70% | 98.90% | 97.14% |

## Results

| Metric | Decision Tree | Random Forest |
|---|---:|---:|
| Accuracy | 0.9649 | 0.9649 |
| Precision | 1.0000 | 1.0000 |
| Recall | 0.9048 | 0.9048 |
| F1 Score | 0.9500 | 0.9500 |
| ROC-AUC | 0.9744 | 0.9937 |

Both models achieved the same test accuracy of 96.49%. The Random Forest obtained a higher ROC-AUC of 0.9937 compared to 0.9744 for the Decision Tree.

## Training and Testing Accuracy

| Model | Training Accuracy | Testing Accuracy |
|---|---:|---:|
| Decision Tree | 0.9758 | 0.9649 |
| Random Forest | 0.9912 | 0.9649 |

## Files

- `ML_05.ipynb` – Jupyter Notebook containing the implementation
- `ML_05.pdf` – Report containing the experiment details and results
- `requirements.txt` – Python dependencies required to run the notebook

## Dependencies

The following Python libraries are required:

```text
numpy
pandas
matplotlib
seaborn
scikit-learn
