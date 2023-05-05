# CryptoClustering

## Prepare the Data

Use the StandardScaler() module from scikit-learn to normalize the data from the CSV file.

	Create a DataFrame with the scaled data and set the "coin_id" index from the original DataFrame as the index for the new DataFrame.

## Find the Best Value for k Using the Original Scaled DataFrame

	Use the elbow method to find the best value for k using the following steps:

o	Create a list with the number of k values from 1 to 11.

o	Create an empty list to store the inertia values.

o	Create a for loop to compute the inertia with each possible value of k.

o	Create a dictionary with the data to plot the elbow curve.

	Plot a line chart with all the inertia values computed with the different values of k to visually identify the optimal value for k.

## Cluster Cryptocurrencies with K-means Using the Original Scaled Data
	Use the following steps to cluster the cryptocurrencies for the best value for k on the original scaled data:
o	Initialize the K-means model with the best value for k.
o	Fit the K-means model using the original scaled DataFrame.
o	Predict the clusters to group the cryptocurrencies using the original scaled DataFrame.
o	Create a copy of the original data and add a new column with the predicted clusters.
	Create a scatter plot using hvPlot as follows:
o	Set the x-axis as "price_change_percentage_24h" and the y-axis as "price_change_percentage_7d".
o	Color the graph points with the labels found using K-means.
o	Add the "coin_id" column in the hover_cols parameter to identify the cryptocurrency represented by each data point.
## Optimize Clusters with Principal Component Analysis
	Using the original scaled DataFrame, perform a PCA and reduce the features to three principal components.
	Create a new DataFrame with the PCA data and set the “coin_id” index from the original DataFrame as the index for the new DataFrame.
## Find the Best Value for k Using the PCA Data
	Use the elbow method on the PCA data to find the best value for k using the following steps:
o	Create a list with the number of k-values from 1 to 11.
o	Create an empty list to store the inertia values.
o	Create a for loop to compute the inertia with each possible value of k.
o	Create a dictionary with the data to plot the Elbow curve.
	Plot a line chart with all the inertia values computed with the different values of k to visually identify the optimal value for k.
## Cluster Cryptocurrencies with K-means Using the PCA Data
	Use the following steps to cluster the cryptocurrencies for the best value for k on the PCA data:
o	Initialize the K-means model with the best value for k.
o	Fit the K-means model using the PCA data.
o	Predict the clusters to group the cryptocurrencies using the PCA data.
o	Create a copy of the DataFrame with the PCA data and add a new column to store the predicted clusters.
	Create a scatter plot using hvPlot as follows:
o	Set the x-axis as "price_change_percentage_24h" and the y-axis as "price_change_percentage_7d".
o	Color the graph points with the labels found using K-means.
o	Add the "coin_id" column in the hover_cols parameter to identify the cryptocurrency represented by each data point.
