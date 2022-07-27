---
date created: Tuesday, May 3rd 2022, 8:29:47 am
date modified: Wednesday, May 4th 2022, 12:09:19 pm
---

# Week 9

## Clustering Analysis Induction

### K-means Clustering

1. determine how many clusters we want (e.g. K = 5)
2. randomly pick K cluster centroids
3. for each data point, find out which centroids they are close to
4. each cluster find a new centroid from its data points
5. repeat 3-5 until no further changes

limitations:

- result quality based on size and density
- not strong for non-globular shapes

Within Cluster Sum of Square distance (WCSS): $$WCSS(k) = \sum^k_{c = 1} \sum_{x_i \in c} ||x_i - \bar{x_c}||^2, \text{$\bar{x_c}$ is the centroid of cluster $c$}$$

> also referred as SSE (Sum of Square Error)

### Visual Analysis of Clustering Tendency (VAT)

1. first, plot a dissimilarity matrix. (calculate every objects' Euclidean distance with other objects);
2. plot the dissimilarity matrix as a heat map;
3. reorder the columns of the heat map to reveal clusters.

> not effective in every situation (complex shapes or significant overlap)

### Hierarchical Clustering

Strengths:

- no assumption of any particular number of clusters
- may correspond to meaningful taxonomies

2 main types:

- Agglomerative
    - start with the points as individual clusters
    - at each step, merge the closest pair of clusters until only 1 (or k) clusters left
- Divisive
    - start with 1 cluster (include all data points)
    - at each step, split a cluster until each cluster contains only 1 point (or k clusters left)

Distance between clusters:

- MIN distance (Single Linkage)
    - can handle non similar shapes
    - but sensitive to noise and outliers
- MAX distance (Complete Linkage)
    - less sensitive to noise and outliers
    - but tend to create spherical clusters with consistent diameter and break large cluster

### PCA Dimensionality Reduction

To reduce Dimensionality, perform **feature selection**.

Perform **feature extraction** to transform N features to n feature (n < N)

- Transformation should preserve the characteristics of the data, i.e. distances between pair of objects (distance represent whether objects are similar or dissimilar)
- If the objects are close to each other, it should be still close after transformation
- If the objects are far away, it should be still far away after transformation
- Ideally, the set of closest neighbors should be the same

#### Principal Components Analysis (PCA)

Find a new set of features that better captures the variability of the data

- first choose a dimension to capture as much of variability as possible
- second dimension is orthogonal to the first, captures as much of the remaining variability

Pros:

- avoid the curse of dimensionality
- reduce the time and memory required by the algorithms
- allow data to be more easily visualized
- may help eliminate irrelevant features or reduce noise
    - fewer features → smaller machine learning models → faster answer
    - better feature set → more accurate answer
- principal components are independent

Limitations:

- may be unintuitive to interpret the principal components
- some information loss
- assume linear combinations of the features
- may not help with classification
- sensitive to scale (need standardization)
- sensitive to outliers
