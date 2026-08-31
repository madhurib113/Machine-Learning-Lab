# Experiment 3 – Naive Bayes and KNN

## Aim

To implement and compare Naive Bayes and K-Nearest Neighbors (KNN) classifiers for email spam and ham classification.

## Dataset

Spambase dataset containing email-related features used to classify emails as spam or non-spam.

## Models Used

- Gaussian Naive Bayes
- Multinomial Naive Bayes
- Bernoulli Naive Bayes
- K-Nearest Neighbors (KNN)

## Work Done

- Loaded and examined the dataset
- Checked missing values and duplicate records
- Performed basic data analysis and visualization
- Normalized the features using MinMaxScaler
- Split the dataset into training and testing sets
- Implemented different Naive Bayes classifiers
- Implemented KNN with different values of k
- Performed GridSearchCV and RandomizedSearchCV for KNN
- Compared KDTree and BallTree
- Used five-fold cross-validation
- Compared accuracy, precision, recall, F1-score and ROC-AUC
- Plotted confusion matrices, ROC curves and Precision-Recall curves
- Compared training and prediction time

## Files

- `ML_02.ipynb` – Jupyter Notebook containing the implementation
- `ML_02.pdf` – Report containing the experiment details and results

## Tools Used

- Python
- NumPy
- Pandas
- Matplotlib
- Scikit-learn
- Jupyter Notebook
