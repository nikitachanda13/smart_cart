# Smart Cart System 🛒

A machine learning based Smart Cart system that analyzes customer purchase behavior and groups customers using clustering techniques.

## Overview

Retail businesses generate large amounts of customer purchase data.  
This project uses machine learning to analyze shopping patterns and group customers into clusters.

These clusters help in improving:
- Personalized recommendations
- Marketing strategies
- Customer segmentation

---

## Technologies Used

- Python
- Pandas
- NumPy
- Scikit-learn
- Matplotlib
- KMeans Clustering
- PCA (Principal Component Analysis)

---

## Machine Learning Workflow

1. Data preprocessing
2. Feature scaling
3. PCA for dimensionality reduction
4. K-Means clustering
5. Elbow Method to determine optimal clusters

---

## Example Code

```python
from sklearn.cluster import KMeans
import matplotlib.pyplot as plt

wcss = []

for k in range(1,11):
    kmeans = KMeans(n_clusters=k, random_state=42)
    kmeans.fit(X_pca)
    wcss.append(kmeans.inertia_)

plt.plot(range(1,11), wcss, marker="o")
plt.xlabel("Number of Clusters")
plt.ylabel("WCSS")
plt.title("Elbow Method")
plt.show()