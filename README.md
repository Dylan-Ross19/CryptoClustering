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

-Initialize the K-means model with the best value for k.
 - [x]
-Fit the model using the PCA data.
 - [x]
-Predict the clusters and add a new column to the DataFrame with the predicted clusters.
 - [x]
-Create a scatter plot using pandas' plot.
 - [x]

## 7. Determine the Weights of Each Feature on Each Principal Component:

-Create a DataFrame showing the weights of each feature for each principal component.
 - [x]
-Analyze which features have the strongest positive or negative influence on each component.
 - [x]

## 8. Coding Conventions and Formatting:

-Ensure proper placement of imports, naming conventions, DRY principles, concise logic, and creative engineering.
 - [x]

## 9. Deployment and Submission:

-Create a GitHub repository containing the project files.
 - [x]
-Add files to the repository using the command line with appropriate commit messages.
 - [x]

## 10. Code Comments:

-Add concise and relevant comments throughout the code to aid understanding for other developers.
 - [x]