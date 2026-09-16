# Experiment 8 – Clustering using K-Means, DBSCAN and Hierarchical Agglomerative Clustering

## Aim

To perform clustering using K-Means, DBSCAN and Hierarchical Agglomerative Clustering and compare the results using different evaluation metrics.

## Dataset

Human Activity Recognition Using Smartphones (UCI HAR) dataset with 10,299 observations and 561 features.

The dataset contains sensor measurements collected from smartphones for different human activities.

## Models Used

- K-Means Clustering
- DBSCAN
- Hierarchical Agglomerative Clustering

## Work Done

- Loaded and explored the dataset
- Checked for missing values and duplicate rows
- Preprocessed the data
- Applied PCA for dimensionality reduction
- Visualized the data using PCA
- Applied K-Means clustering
- Tested different values of K
- Used WCSS and Silhouette Score for K-Means
- Applied DBSCAN with different parameter values
- Applied Hierarchical Agglomerative Clustering using Ward linkage
- Compared the clustering results
- Calculated Silhouette Score, Davies-Bouldin Index and Calinski-Harabasz Index
- Compared the clusters with the actual activity labels using ARI and NMI

## Results

### K-Means

- Number of clusters: 2
- Silhouette Score: 0.4815
- Davies-Bouldin Index: 0.8543
- Calinski-Harabasz Index: 11770.86
- ARI: 0.3296
- NMI: 0.5455

### DBSCAN

- The tested parameter values resulted in all 10,299 samples being classified as noise.
- No clusters were formed for the tested settings.

### Hierarchical Agglomerative Clustering

- Number of clusters: 2
- Silhouette Score: 0.4811
- Davies-Bouldin Index: 0.8552
- Calinski-Harabasz Index: 11735.79
- ARI: 0.3324
- NMI: 0.5561

## Files

- `ML_08.ipynb` – Jupyter Notebook containing the implementation
- `ML_08.pdf` – Report containing the experiment details and results

## Dependencies

The following Python libraries are required to run the notebook:

```text
numpy
pandas
matplotlib
scikit-learn
