# ML-Clustering-Pipeline
This GitHub repository contains a machine learning pipeline that analyzes a dataset of interests grouped by individuals. It includes data preprocessing, K-Means clustering, and evaluation methods like the Elbow Method and Silhouette Score. The code is designed to provide insights into patterns and relationships among different interest categories.

## Data Loading and Inspection
* The pipeline starts by importing necessary libraries such as NumPy, pandas, Seaborn, and Matplotlib. It then loads a dataset from a CSV file named 'Interests_group.csv' using pd.read_csv(). The first few rows of the dataset are examined using df.head(), and information about the dataset is checked using df.info(). Additionally, the shape of the dataset is obtained using df.shape.

## Handling Missing Values
* Missing values in the dataset are identified and handled. This involves filling missing values with the median of each column using df.fillna(df.median()). Columns where more than 30% of the data is missing are dropped.

## Categorical to Numerical Conversion
* Categorical data is converted into numerical format using Label Encoding with LabelEncoder().

## K-Means Clustering
* The K-Means clustering algorithm is applied to the dataset. Specific columns (such as 'grand_tot_interests' and 'interest215') are selected, and the K-Means model is fitted with n_clusters=5. The resulting clusters and centroids are plotted using Seaborn and Matplotlib. Additionally, the Silhouette Score is calculated to evaluate the quality of the clustering.

## Elbow Method
* The Elbow Method is applied to determine the optimal number of clusters for K-Means. This method helps in finding the appropriate number of clusters by plotting the Within-Cluster Sum of Squares (WCSS) for different numbers of clusters.

This repository serves as a comprehensive guide for implementing a clustering pipeline in machine learning. It provides a structured approach from data preprocessing to evaluation, facilitating easy understanding and implementation of clustering techniques. Feel free to explore the code and adapt it to your specific use cases!
