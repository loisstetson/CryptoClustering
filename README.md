# CryptoClustering

Here is an overview of the steps I took to complete this challenge: 

The data preparation stage entailed normalizing the data using StandardScaler from scikit-learn. A new DataFrame with the normalized data was created, preserving the "coin_id" index from the original data.

To determine the optimal number of clusters (k), the elbow method was applied to the scaled data. This involved plotting inertia values for k ranging from 1 to 11 and visually determining the most suitable k.

For clustering, the K-Means algorithm was initialized with the optimal k and fitted to the original scaled data. The predicted clusters were then added to a copy of the original DataFrame.

Visualization was performed by plotting a scatter plot using hvPlot with principal components on the axes and the clusters represented in different colors.

Principal Component Analysis (PCA) was subsequently used to reduce the feature space to three principal components, and the explained variance was examined to understand the information retention of these components.

The elbow method was reapplied on the PCA-reduced data to ascertain the best k, which was found to be consistent with the one obtained from the original data.

The K-Means model was then fitted to the PCA data, and cryptocurrencies were clustered again. The resulting clusters were stored in a new DataFrame column, and a scatter plot was created to visualize the clustering on the PCA-reduced feature space.

Finally, the impact of using fewer features for K-Means clustering was assessed. The conclusion drawn was that using PCA leads to tighter clusters, with more data points grouped into certain clusters compared to the original dataset. This suggests that PCA can improve the clarity of the clustering pattern by reducing the dimensionality of the data.
