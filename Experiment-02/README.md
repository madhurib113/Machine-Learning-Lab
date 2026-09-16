# Experiment 2 – Email Spam/Ham Classification using Naive Bayes and KNN

## Aim

To classify emails as spam or ham using different Naive Bayes classifiers and K-Nearest Neighbors (KNN) and compare their performance.

## Dataset

The Spambase dataset was used for this experiment.

- Samples: 4601
- Features: 57
- Target: Spam or Ham
- Missing values: None
- Duplicate rows: 391

The dataset contains word frequency, character frequency and capital letter related features. :contentReference[oaicite:0]{index=0}

## Models Used

- Gaussian Naive Bayes
- Multinomial Naive Bayes
- Bernoulli Naive Bayes
- K-Nearest Neighbors (KNN)

## Work Done

- Loaded and examined the Spambase dataset
- Checked missing values and duplicate records
- Performed basic data analysis and visualization
- Normalized the features using MinMaxScaler
- Split the dataset into training and testing sets
- Implemented Gaussian, Multinomial and Bernoulli Naive Bayes
- Implemented KNN with different values of k
- Performed GridSearchCV for KNN
- Performed RandomizedSearchCV for KNN
- Compared KDTree and BallTree
- Used five-fold cross-validation
- Evaluated accuracy, precision, recall, F1-score and ROC-AUC
- Generated confusion matrices
- Plotted ROC and Precision-Recall curves
- Compared training and prediction time

## Data Split

- Training samples: 3680
- Testing samples: 921 :contentReference[oaicite:1]{index=1}

## Naive Bayes Results

| Model | Accuracy | Precision | Recall | F1 Score | ROC-AUC |
|---|---:|---:|---:|---:|---:|
| Gaussian NB | 0.8219 | 0.7233 | 0.9385 | 0.8170 | 0.8374 |
| Multinomial NB | 0.8719 | 0.9503 | 0.7359 | 0.8295 | 0.8538 |
| Bernoulli NB | 0.8806 | 0.9046 | 0.8026 | 0.8505 | 0.8702 |

## KNN Results

Different values of k were tested.

| k | Accuracy | Precision | Recall | F1 Score |
|---:|---:|---:|---:|---:|
| 1 | 0.8817 | 0.8504 | 0.8744 | 0.8622 |
| 3 | 0.8806 | 0.8723 | 0.8410 | 0.8564 |
| 5 | 0.8838 | 0.8773 | 0.8436 | 0.8601 |
| 7 | 0.8849 | 0.8797 | 0.8436 | 0.8613 |
| 9 | 0.8773 | 0.8880 | 0.8128 | 0.8487 |
| 11 | 0.8827 | 0.8961 | 0.8179 | 0.8552 |

## KNN Hyperparameter Tuning

### GridSearchCV

Best parameters:

- Number of neighbors: `5`
- Weights: `distance`
- Algorithm: `auto`
- Best CV Accuracy: `0.9141`

### RandomizedSearchCV

Best parameters:

- Number of neighbors: `5`
- Weights: `distance`
- Algorithm: `kd_tree`
- Best CV Accuracy: `0.9141`

Both searches obtained the same cross-validation accuracy. RandomizedSearchCV took less execution time. :contentReference[oaicite:2]{index=2}

## KDTree and BallTree Comparison

| Algorithm | Accuracy | Training Time | Prediction Time |
|---|---:|---:|---:|
| KDTree | 0.8838 | 0.041 s | 0.264 s |
| BallTree | 0.8838 | 0.020 s | 0.229 s |

## Cross-Validation

| Fold | Naive Bayes | Best KNN |
|---|---:|---:|
| Fold 1 | 0.8512 | 0.8762 |
| Fold 2 | 0.8663 | 0.8924 |
| Fold 3 | 0.8543 | 0.9185 |
| Fold 4 | 0.8435 | 0.9098 |
| Fold 5 | 0.6957 | 0.7630 |
| Average | 0.8222 | 0.8720 |

## Final Classifier Comparison

| Classifier | Accuracy |
|---|---:|
| Gaussian NB | 0.8219 |
| Multinomial NB | 0.8719 |
| Bernoulli NB | 0.8806 |
| KNN | 0.8838 |

## Training and Prediction Time

| Algorithm | Training Time | Prediction Time |
|---|---:|---:|
| Gaussian NB | 0.008 s | 0.002 s |
| Multinomial NB | 0.007 s | 0.001 s |
| Bernoulli NB | 0.012 s | 0.002 s |
| Best KNN | 0.002 s | 0.111 s |

## Files

- `ML_02.ipynb` – Jupyter Notebook containing the implementation
- `ML_02.pdf` – Report containing the experiment details and results

## Dependencies

The following Python libraries are required:

```text
numpy
pandas
matplotlib
scikit-learn
