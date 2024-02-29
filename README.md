# CryptoClustering
## Dylan Ross
---
## 1. Load and Prepare the Data:

-Load the CSV file into a DataFrame and set the index to "coin_id".
 - [x]Provided for in source_coude
-Use StandardScaler to normalize the data.
 - [x] Used `StandardScaler()` from scikit-learn to scale the data in the `market_data_df` DataFrame, which presumably contains  cryptocurrency market data.
 The scaled data is stored in a new DataFrame called `df`, with columns and index inherited from `market_data_df`.
-Create a DataFrame with the scaled data, using "coin_id" as the index.
 - [x] Copied the cryptocurrency names from the original data into a new DataFrame called `cryptos`.
 It prints a message indicating that the `'coin_id`' column is already set as the index.
 Finally, it displays the first 10 rows of the scaled DataFrame `df`.

## 2. Find the Best Value for k Using the Original Scaled DataFrame:

-Implement the elbow method algorithm to find the best value for k.
 - [x] The code computed the inertia values for different numbers of clusters (k) using KMeans clustering. It created a list of k-values  to try and an empty list to store the inertia values. Inside a loop, it iterated through each k-value, created a KMeans model, fit the  model to the scaled data, and appends the inertia value to the list. Memory Leak Fix and Warning Suppression: This section fixes a known memory leak issue in KMeans clustering on Windows with MKL and suppresses the associated warning.
-Visualize the inertia values for different k values and identify the optimal k.
 - [x] The inertia values computed for different k-values are stored in a DataFrame. The DataFrame is then used to plot a line chart (Elbow curve) using matplotlib. This curve helps visualize the inertia values and identify the optimal number of clusters.
-Answer the question regarding the best value for k.
 - [x]

## 3. Cluster Cryptocurrencies with K-Means Using the Original Scaled Data:

- Model Fit Predict
 - [x]
-Create a scatter plot using pandas' plot.
 - [x] `kind='scatter'`: Specifies the type of plot as a scatter plot.
`x='price_change_percentage_24h'`: Set the values for the x-axis based on the price_change_percentage_24h column.
`y='price_change_percentage_7d'`: Set the values for the y-axis based on the price_change_percentage_7d column.
`c='Cluster':` Determined the color of each data point based on the values in the `Cluster` column.
`colormap='rainbow'`: Specified the color map to use for the data points, with the "rainbow" option providing a visually appealing color scheme.

## 4. Optimize Clusters with Principal Component Analysis (PCA):

-Create a PCA model instance with n_components=3.
 - [x] `pca = PCA(n_components=3)`
-Reduce the features to three principal components.
 - [x] `pca.fit_transform(df)`: Fit the PCA model to the scaled DataFrame (df) and transformed the data into the new principal component space.
-Calculate and interpret the explained variance.
 - [x] `explained_variance`: This variable stores the explained variance ratio, which indicates the proportion of the dataset's variance that lies along each of the principal components. It is obtained by accessing the explained_variance_ratio_ attribute of the PCA model.
 `pca.explained_variance_ratio_`: This attribute of the PCA model returns an array containing the explained variance ratio of each principal component.
-Create a new DataFrame with the PCA data.
 - [x] Initialized a new DataFrame named `pca_df` using the PCA features obtained from the PCA model. It  includes three principal components labeled as 'PCA1', 'PCA2', and 'PCA3'. The index of this DataFrame is set to match the index of the original DataFrame (df), which is the `coin_id`.

## 5. Find the Best Value for k Using the PCA Data:

-Apply the elbow method using the PCA data to find the best value for k.
 - [x] A dictionary elbow_data_pca is created to store the k-values and their corresponding inertia values.  The data from elbow_data_pca dictionary is used to create a DataFrame elbow_df_pca for plotting the Elbow curve.
-Visualize the inertia values and identify the optimal k.
 - [x] Created a line plot to determine that 4 was the opt k.
-Answer the questions regarding the best value for k compared to the original data.
 - [x]

## 6. Cluster Cryptocurrencies with K-Means Using the PCA Data: 

- Model Fit Predict
 - [x]
-Create a scatter plot using pandas' plot.
 - [x] `The hvplot.scatter()` function generated a scatter plot.
`x='PCA1' and y='PCA2'` specified the columns to be plotted on the x and y axes, respectively.
`by='Cluster'` colored the data points based on the values in the `'Cluster'` column.
`hover_cols=['coin_id']` adds additional information (coin_id) to the hover tooltip when hovering over data points.

 ###  Create Scatter Plot displaying All 3 PCAs
 - `fig = plt.figure()` created a new figure object.
`ax = fig.add_subplot(projection='3d')` added a 3D subplot to the figure.
`ax.scatter3D()` generated a 3D scatter plot.
`pca_data_copy['PCA1']`, `pca_data_copy['PCA2']`, and `pca_data_copy['PCA3']` specified the values for the x, y, and z axes, respectively.
`c=pca_data_copy['Cluster']` colored the data points based on the values in the 'Cluster' column.
cmap='rainbow' specified the color map to be used for coloring the data points.
`plt.colorbar(plot_3D, label='Cluster', pad=0.2)` added a colorbar to the plot, indicating the mapping of cluster values to colors.

## 7. Determine the Weights of Each Feature on Each Principal Component:

-Create a DataFrame showing the weights of each feature for each principal component.
 - [x] `pca_data_copy.set_index(df.index, inplace=True)` matched the index of the original DataFrame, the rows of `pca_data_copy` will now correspond to the same rows as the original DataFrame, ensuring alignment of data on future analyses.
-Analyze which features have the strongest positive or negative influence on each component.
 - [x]