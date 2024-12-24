# Network Traffic Anomaly Detection
This project focuses on detecting anomalies in network traffic data using a K-means clustering algorithm, implemented from scratch. Anomalies in the network traffic can indicate potential malicious behavior or data breaches, and the K-means algorithm allows for grouping data into clusters, helping us identify normal and anomalous patterns.

## Project Overview
The main objective of this project is to classify network traffic into "normal" and "anomalous" groups based on features like the number of bytes transferred, the duration of the connection, flags, and other network-related attributes. Using K-means clustering, we attempt to segment network traffic into clusters, with the assumption that most traffic belongs to a "normal" group and outliers or anomalies form separate clusters.

### Key Steps Implemented:
K-means Algorithm Implementation:

### The K-means algorithm was implemented from scratch, where data points are assigned to one of several clusters based on the proximity to centroids.
In each iteration, centroids are updated as the mean of the data points assigned to each cluster.
Euclidean Distance:

### The Euclidean distance is used to calculate the proximity between data points and cluster centroids.
The distance metric helps to assign each point to the closest centroid during each iteration of the K-means algorithm.
Silhouette Score for Optimal Clusters:

### The Silhouette Score is used to determine the optimal number of clusters.
This metric provides an indication of how similar each point is to its own cluster compared to other clusters. A higher silhouette score indicates well-defined clusters, whereas a lower score suggests potential misclassification.
Identifying Anomaly Threshold with Centroids:

Once K-means clustering is applied, centroids of the clusters are computed. We use the distances from each point to the centroid of its assigned cluster.
The threshold for anomaly detection is set using these distances by identifying the 95th percentile of the minimum distance between points and the closest centroids. Points beyond this threshold are classified as anomalies.
