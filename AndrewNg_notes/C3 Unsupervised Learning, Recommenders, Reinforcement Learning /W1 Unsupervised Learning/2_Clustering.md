# Clustering

---

## What is clustering?

Clustering is a type of unsupervised learning in machine learning where the goal is to group a set of objects in such a way that objects in the same group (called a cluster) are more similar to each other than to those in other groups. It is used to find structure in unlabeled data by identifying natural groupings or patterns.

### Common clustering algorithms include:
* K-means clustering
* Hierarchical clustering
* DBSCAN (Density-Based Spatial Clustering of Applications with Noise)

### Applications of clustering
* Grouping similar news
* Market segmentation
* DNA analysis
* Astronomical data analysis

Applications of clustering include customer segmentation, image compression, and anomaly detection.

---

## K-means intuition 

K-means clustering is one of the simplest and most popular unsupervised machine learning algorithms. The intuition behind K-means is to partition the data into K distinct clusters based on distance to the centroid of a cluster.

### Steps involved in K-means clustering:
1. **Initialization**: Choose K initial centroids randomly from the dataset.
2. **Assignment**: Assign each data point to the nearest centroid, forming K clusters.
3. **Update**: Calculate the new centroids as the mean of all data points assigned to each cluster.
4. **Repeat**: Repeat the assignment and update steps until the centroids no longer change significantly or a maximum number of iterations is reached.

### Key points:
* The number of clusters, K, must be specified beforehand.
* The algorithm aims to minimize the within-cluster variance (sum of squared distances from each point to its centroid).
* K-means is sensitive to the initial placement of centroids and may converge to a local minimum.

### Example:
Consider a dataset with points in a 2D space. The K-means algorithm will:
1. Randomly initialize K centroids.
2. Assign each point to the nearest centroid.
3. Recalculate the centroids based on the assigned points.
4. Repeat the process until the centroids stabilize.

### Visual Example:

Here are some visual examples of K-means clustering:

![Example 1](./img/1.png) ![Example 2](./img/2.png)

![Example 3](./img/3.png) ![Example 4](./img/4.png)

![Example 5](./img/5.png) ![Example 6](./img/6.png)

K-means is widely used in various applications such as customer segmentation, image compression, and pattern recognition due to its simplicity and efficiency.

---

## K-means algorithm

### Steps

1. Randomly initialize K cluster centroids µ<sub>1</sub>, µ<sub>2</sub>, ... ,µ<sub>k</sub>

2. 
Repeat {  
    **Assign points to cluster centroids**  
    for i = 1 to m  
        c<sup>(i)</sup> := index(from 1 to k) of cluster centroid closest to x<sup>(i)</sup>  
    **Move cluster centroids**  
    for k = 1 to K  
        µ<sub>k</sub> := average(mean) of points assigned to cluster k  
}  

**Note:** Sometimes a cluster may have zero training examples, in that case, we can remove that cluster. (k = k-1)


### K-means for clusters that are not well seperated

For example, consider a t-shirt manufacturing company that decides to cluster customer sizes into three categories: S, M, and L. They collect data on customers' height and weight, plot it on a 2D graph, and find that the data points are not well separated. However, they can still cluster the data into three groups, as shown in the figure below.

![Example 7](./img/7.png)

---

## Optimization objective

---

### k-means optimization objective 

c<sup>(i)</sup> = index of cluster (1,2,...,k) to which example x<sup>(i)</sup> is currently assigned  
µ<sub>k</sub> = cluster centroid k  
µ<sub>c</sub> = cluster centroid of cluster  to which example x<sup>(i)</sup> has been assigned  

### Cost function 

![cost function](./img/8.png)







