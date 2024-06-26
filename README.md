# CryptoClustering Project

## Introduction

The CryptoClustering project aimed to analyze cryptocurrency market data using unsupervised learning techniques, primarily focusing on K-Means clustering. The goal was to predict if cryptocurrencies are affected by 24-hour or 7-day price changes. The project utilized Python, Pandas, NumPy, scikit-learn, and hvPlot for data manipulation, analysis, and visualization.

## Data Preparation

The project started by loading the crypto_market_data.csv file into a Pandas DataFrame. The data was then explored using summary statistics and visualizations to understand its structure and distribution.

## Clustering with K-Means

Finding the Best Value for k

To determine the optimal number of clusters (k), the Elbow Method was employed. This involved creating a range of k values from 1 to 11 and computing the inertia (sum of squared distances of samples to their closest cluster center) for each k. A line chart was plotted to visualize the inertia values, and the "elbow point," where the inertia starts to decrease more slowly, was identified. The analysis revealed that the optimal k value for the dataset was 4.

Cluster Analysis

With k=4, K-Means clustering was applied to the original scaled data. Each cryptocurrency was assigned a cluster label, and a scatter plot was created to visualize the clusters. The analysis showed that most clusters were concentrated in the -1 to 0 range for both 7-day and 24-hour price changes.

## Dimensionality Reduction with PCA

Principal Component Analysis (PCA) was performed on the original scaled data to reduce the features to three principal components. The explained variance of each principal component was analyzed to understand how much information each component retained. The total explained variance of the three components was approximately 89.5%, indicating that these components captured a significant amount of information from the original data.

## Clustering with PCA Data

Finding the Best Value for k

Using the PCA-transformed data, the Elbow Method was again used to find the optimal k value. A line chart of inertia values for different k values was plotted, and the elbow point was identified. The analysis showed that the optimal k value remained 4, consistent with the analysis on the original data.

Cluster Analysis

K-Means clustering with k=4 was applied to the PCA-transformed data. A scatter plot was created to visualize the clusters, which showed that the clusters were more compact and interpretable compared to the original data.

## Visualizing and Comparing Results

Composite plots were created to compare the clustering results from the original data and the PCA-transformed data. These plots included the elbow curves and cluster visualizations for both datasets. The analysis highlighted the impact of using fewer features on the clustering results, showing that PCA transformation led to more distinct and clustered groups.

## Conclusion

The CryptoClustering project demonstrated the use of unsupervised learning techniques and dimensionality reduction to analyze cryptocurrency market data. The analysis provided insights into how cryptocurrencies are affected by price changes and underscored the importance of feature selection and dimensionality reduction in clustering analysis. The project's findings can be valuable for understanding cryptocurrency market trends and making informed investment decisions.

## References

Data for this dataset was generated by edX Boot Camps LLC, and is intended for educational purposes only.




