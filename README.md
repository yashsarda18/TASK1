# TASK1

Develop a clustering algorithm that effectively groups these data points into meaningful clusters. The choice of clustering algorithm is at your discretion (for example, K-means, DBSCAN, hierarchical clustering, etc.). The implementation can be carried out using either Python or C++.

## CHOSEN APPROACH
[Note: Coded in Google Colab]

- Used the sklearn learn library comprehensively throughout the notebook.
- Used KMeans method for clustering.
- Used elbow method to determine the number of clusters.

### STEP BY STEP APPROACH

- Make sure you have open3d and scikit-learn installed
- if not , Give the following command
```!pip install open3d scikit-learn```

- Use inbuilt colab GPU to run the code faster.

#### DATASET PREPARATION: 
- Extract the point cloud data files using open3d library.
- Convert it into an array.
- Plot a single point
- Inspect the data (to get hands on with the data)

#### APPLYING KMEANS
- There is no significant pre-processing to be done as it is a prepared dataset with X, Y and Z co-ordinates.
- So, we directly apply KMeans algorithm
- To find the number of clusters , we use elbow method.
- We plot mean distance and look for the elbow point where the rate of decrease shifts.
- So , from this plot , we determine the number of clusters to be used in this case.
- For successful running of the KMeans algorithm , you need to have the library imported.
```from sklearn.cluster import KMeans```

#### SAVING THE PCD FILES 
- You need to have open3d library installed in order to save the clustered files



## OUTPUT:
- We got the elbow point beween 3 and 4.
- So, we clustered dataset into 3 clusters in the first part of the notebook and 4 clusters in the second part of the notebook.
  [Note: As the dataset was very large , the code block was taking too much time in running the code , would probably run faster with a better GPU].
- We cannot exactly evaluate a clustering problem as we do not have any true labels.
- Instead we can evaluate it as how well the point is included in the cluster (distance from centroid).
- I wanted to use silhouette_score matrix to determine how well the clustering is done. It gives score between -1 and 1 . The more we are closer to 1, the more better our model is clustering but it takes a very long time to run.

## INSIGHTS:
- The dataset had 994153 columns and 3 rows.
- Features were X,Y and Z co-ordinates.
- We got 4 clusters out of this dateset.
- Cluster 1 has 204755 points , 2 has 285243 points , 3 has 265402 points , 4 has 238753 points.
- All the four clusters are evenly distributed with points.
