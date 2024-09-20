# Fashion-MNIST-Clustering
Dimensionality Reduction and Data Clustering using the Fashion MNIST dataset.

# Intro
This project focuses on dimensionality reduction and data clustering using the Fashion MNIST dataset. It explores Principal Component Analysis (PCA) and Autoencoders for reducing the dimensionality of the dataset, followed by k-means clustering on the reduced data.

# How it works
The project consists of two main parts: Dimensionality Reduction and Clustering.

  # 1. Dimensionality Reduction
  - PCA (Principal Component Analysis): The dataset's dimensionality is reduced while preserving 90% of the variance. The resulting dimension M is computed.
  - Autoencoder: A neural network architecture (d – d/4 - M – d/4 – d) is trained to reduce the data dimension to 𝑀, based on the result from the PCA method.
  - The best classification model from ML1 is applied to the reduced-dimensional data to evaluate performance improvements.

  # 2. Clustering
  - k-means Clustering: The data (in reduced dimensions from both PCA and Autoencoder) is clustered using k-means with values of 𝐾 ranging from 10 to 20. The silhouette score is computed to find the optimal number of clusters 𝐾∗.
  - Cluster Visualization: The center of each cluster is visualized as an image in its original dimensions.
  - Clustering Evaluation: The clustering results are evaluated using two metrics:
    - Purity: Measures the percentage of correctly classified data points.
    - F-measure: Based on true positives (TP), false positives (FP), and false negatives (FN), the F-measure is computed for each cluster, and the total F-measure is calculated.
