# Experiment 3 – Regression Analysis using Linear and Regularized Models

## Aim

To implement Linear Regression, Ridge Regression, Lasso Regression and Elastic Net Regression for predicting loan amounts and compare their performance.

## Dataset

The loan dataset was used for this experiment.

- Samples: 4269
- Initial features: 12
- Target variable: Loan Amount
- Numerical and categorical features are present
- No missing values

The dataset contains information such as income, loan term, CIBIL score and different asset values. :contentReference[oaicite:1]{index=1}

## Models Used

- Linear Regression
- Ridge Regression
- Lasso Regression
- Elastic Net Regression

## Work Done

- Loaded and examined the dataset
- Checked the dataset shape and data types
- Checked for missing values
- Removed the loan ID column
- Encoded categorical variables using LabelEncoder
- Separated features and target variable
- Standardized the features using StandardScaler
- Performed basic EDA
- Visualized the loan amount distribution
- Plotted income vs loan amount
- Split the dataset into training and testing sets
- Implemented Linear Regression
- Implemented Ridge Regression
- Implemented Lasso Regression
- Implemented Elastic Net Regression
- Performed hyperparameter tuning using GridSearchCV
- Used 5-fold cross-validation
- Evaluated the models using MAE, MSE, RMSE and R² score
- Compared training time
- Compared training and validation errors
- Plotted actual vs predicted values
- Plotted residuals
- Compared model coefficients

## Data Split

- Training samples: 3415
- Testing samples: 854
- Features used: 11 :contentReference[oaicite:2]{index=2}

## Hyperparameter Tuning

### Ridge Regression

- Best alpha: `1`
- Best CV R²: `0.863150`

### Lasso Regression

- Best alpha: `10`
- Best CV R²: `0.863148`

### Elastic Net Regression

- Best alpha: `0.01`
- Best l1_ratio: `0.8`
- Best CV R²: `0.863126`

## Results

| Model | MAE | MSE | RMSE | R² Score |
|---|---:|---:|---:|---:|
| Linear Regression | 2598631 | 1.175502e+13 | 3428560 | 0.853401 |
| Ridge Regression | 2598169 | 1.174876e+13 | 3427646 | 0.853479 |
| Lasso Regression | 2598630 | 1.175502e+13 | 3428559 | 0.853401 |
| Elastic Net | 3008482 | 1.439849e+13 | 3794535 | 0.820434 |

The results were calculated using MAE, MSE, RMSE and R² score. :contentReference[oaicite:3]{index=3}

## Training Time

| Model | Training Time |
|---|---:|
| Linear Regression | 0.024 s |
| Ridge Regression | 0.008 s |
| Lasso Regression | 0.019 s |
| Elastic Net | 0.005 s |

## Cross-Validation Results

| Model | Average R² |
|---|---:|
| Linear Regression | 0.861004 |
| Ridge Regression | 0.861004 |
| Lasso Regression | 0.861004 |
| Elastic Net | 0.860974 |

## Files

- `ML_03.ipynb` – Jupyter Notebook containing the implementation
- `ML_03.pdf` – Report containing the experiment details and results
- `requirements.txt` – Python dependencies required to run the notebook

## Dependencies

The following Python libraries are required:

```text
numpy
pandas
matplotlib
scikit-learn
