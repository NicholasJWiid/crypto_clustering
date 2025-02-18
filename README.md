# crypto_clustering

This project uses Python and unsupervised machine learning to predict if cryptocurrencies are affected by 24-hour or 7-day price changes.

## Preparing the Data
  * Use the StandardScaler() module from scikit-learn to normalize the data from the CSV file.
  * Create a DataFrame with the scaled data and set the "coin_id" index from the original DataFrame as the index for the new DataFrame.

## Find the Best Value for k Using the Original Scaled DataFrame
  * Create a list with the number of k values from 1 to 11.
  * Create an empty list to store the inertia values.
  * Create a for loop to compute the inertia with each possible value of k.
  * Create a dictionary with the data to plot the elbow curve.
  * Plot a line chart to visually identify the optimal value for k.
  * What is the best value for k?

## Cluster Cryptocurrencies with K-means Using the Original Scaled Data
  * Initialize the K-means model with the best value for k.
  * Fit the K-means model using the original scaled DataFrame.
  * Predict the clusters to group the cryptocurrencies using the original scaled DataFrame.
  * Create a copy of the original data and add a new column with the predicted clusters.
  * Create a scatter plot using hvPlot.

## Optimize Clusters with Principal Component Analysis
 * Perform a PCA and reduce the features to three principal components.
 * Retrieve the explained variance to determine how much information can be attributed to each principal component.
  * What is the total explained variance of the three principal components?
 * Create a new DataFrame with the PCA data and set the "coin_id" index from the original DataFrame as the index for the new DataFrame.

## Find the Best Value for k Using the PCA Data
* Create a list with the number of k-values from 1 to 11.
* Create an empty list to store the inertia values.
* Create a for loop to compute the inertia with each possible value of k.
* Create a dictionary with the data to plot the Elbow curve.
* Plot a line chart with all the inertia values computed with the different values of k to visually identify the optimal value for k.
 * What is the best value for k when using the PCA data?
 * Does it differ from the best k value found using the original data?

## Cluster Cryptocurrencies with K-means Using the PCA Data
 * Initialize the K-means model with the best value for k.
 * Fit the K-means model using the PCA data.
 * Predict the clusters to group the cryptocurrencies using the PCA data.
 * Create a copy of the DataFrame with the PCA data and add a new column to store the predicted clusters.
 * Create a scatter plot using hvPlot.
 * Combine both sets of elbow and cluster plots for comparison.
  * What is the impact of using fewer features to cluster the data using K-Means?
