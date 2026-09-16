# Experiment 4 – Classification using Logistic Regression and SVM

## Aim

To classify emails as spam or non-spam using Logistic Regression and Support Vector Machine (SVM) and compare their performance.

## Dataset

The Spambase dataset was used for this experiment.

- Samples: 4601
- Features: 57
- Target: Spam or Ham
- Missing values: None

The dataset contains word frequency, character frequency and capital letter related features used to classify emails. :contentReference[oaicite:2]{index=2}

## Models Used

- Logistic Regression
- Support Vector Machine (SVM)

Different SVM kernels were also tested:

- Linear
- Polynomial
- RBF
- Sigmoid

## Work Done

- Loaded and examined the dataset
- Checked the dataset shape and columns
- Checked for missing values
- Separated features and target
- Standardized the features using StandardScaler
- Performed basic EDA
- Visualized the class distribution
- Plotted the correlation heatmap
- Split the dataset into training and testing sets
- Implemented Logistic Regression
- Implemented SVM with different kernels
- Performed hyperparameter tuning using GridSearchCV
- Used 5-fold cross-validation
- Evaluated accuracy, precision, recall and F1-score
- Compared training time and model complexity
- Generated confusion matrices
- Compared the classifiers

## Hyperparameter Tuning

### Logistic Regression

Best parameters:

- C: `10`
- Solver: `liblinear`
- Best CV Accuracy: `92.58%`

### SVM

Best parameters:

- Kernel: `rbf`
- C: `1`
- Gamma: `scale`
- Best CV Accuracy: `93.13%`

## SVM Kernel Comparison

| Kernel | Accuracy | F1 Score |
|---|---:|---:|
| Linear | 0.9251 | 0.9091 |
| Polynomial | 0.7644 | 0.6291 |
| RBF | 0.9349 | 0.9206 |
| Sigmoid | 0.8893 | 0.8665 |

## Results

### Logistic Regression

- Accuracy: 0.9197
- Precision: 0.9317
- Recall: 0.8744
- F1 Score: 0.9021
- Training Time: 0.0323 seconds

### Best SVM

- Accuracy: 0.9349
- F1 Score: 0.9206
- Training Time: 0.3518 seconds

## Cross-Validation Results

| Fold | Logistic Regression | SVM |
|---|---:|---:|
| Fold 1 | 0.9186 | 0.9327 |
| Fold 2 | 0.9283 | 0.9337 |
| Fold 3 | 0.9293 | 0.9500 |
| Fold 4 | 0.9402 | 0.9489 |
| Fold 5 | 0.8402 | 0.8500 |
| Average | 0.9113 | 0.9231 |

## Comparison

| Criterion | Logistic Regression | SVM |
|---|---|---|
| Accuracy | 0.9197 | 0.9349 |
| Model Complexity | Low | High |
| Training Time | 0.0323 s | 0.3518 s |
| Interpretability | High | Low |

## Files

- `ML_04.ipynb` – Jupyter Notebook containing the implementation
- `ML_04.pdf` – Report containing the experiment details and results
- `requirements.txt` – Python dependencies required to run the notebook

## Dependencies

The following Python libraries are required:

```text
numpy
pandas
matplotlib
scikit-learn
