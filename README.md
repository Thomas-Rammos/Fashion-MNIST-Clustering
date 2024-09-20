# Fashion-MNIST-Clustering
Dimensionality Reduction and Data Clustering using the Fashion MNIST dataset.

# Intro
This project focuses on dimensionality reduction and data clustering using the Fashion MNIST dataset. It explores Principal Component Analysis (PCA) and Autoencoders for reducing the dimensionality of the dataset, followed by k-means clustering on the reduced data.

# How it works
The project consists of two main parts: Dimensionality Reduction and Clustering.

  # 1. Dimensionality Reduction
  - PCA (Principal Component Analysis): The dataset's dimensionality is reduced while preserving 90% of the variance. The resulting dimension M is computed.
  - Autoencoder: A neural network architecture (d – d/4 - M – d/4 – d) is trained to reduce the data dimension to 𝑀, based on the result from the PCA method.
  - The best classification model from Fashion-MNIST-Classifiers is applied to the reduced-dimensional data to evaluate performance improvements.

  # 2. Clustering
  - k-means Clustering: The data (in reduced dimensions from both PCA and Autoencoder) is clustered using k-means with values of 𝐾 ranging from 10 to 20. The silhouette score is computed to find the optimal number of clusters 𝐾∗.
  - Cluster Visualization: The center of each cluster is visualized as an image in its original dimensions.
  - Clustering Evaluation: The clustering results are evaluated using two metrics:
    - Purity: Measures the percentage of correctly classified data points.
    - F-measure: Based on true positives (TP), false positives (FP), and false negatives (FN), the F-measure is computed for each cluster, and the total F-measure is calculated.

# How to use
To run the code:

  1. Install required libraries: The notebook uses libraries such as TensorFlow, Keras, scikit-learn, and matplotlib.
  2. Preprocess the data: Randomly select a subset of the Fashion MNIST dataset (e.g., 1000 or 2000 images per category), and normalize it.
  3. Run the models: The notebook contains cells to perform dimensionality reduction (PCA, Autoencoder), clustering (k-means), and evaluation.
  4. View Results: The notebook will generate plots for the silhouette score, cluster centers, and evaluation metrics (Purity and F-measure).
