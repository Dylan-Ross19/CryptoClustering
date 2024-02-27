# CryptoClustering
---
## 1. Load and Prepare the Data:

-Load the CSV file into a DataFrame and set the index to "coin_id".
-Use StandardScaler to normalize the data.
-Create a DataFrame with the scaled data, using "coin_id" as the index.

## 2. Find the Best Value for k Using the Original Scaled DataFrame:

-Implement the elbow method algorithm to find the best value for k.
-Visualize the inertia values for different k values and identify the optimal k.
-Answer the question regarding the best value for k.

## 3. Cluster Cryptocurrencies with K-Means Using the Original Scaled Data:

-Initialize the K-means model with the best value for k.
-Fit the model using the original scaled DataFrame.
-Predict the clusters and add a new column to the DataFrame with the predicted clusters.
-Create a scatter plot using pandas' plot.

## 4. Optimize Clusters with Principal Component Analysis (PCA):

-Create a PCA model instance with n_components=3.
-Reduce the features to three principal components.
-Calculate and interpret the explained variance.
-Create a new DataFrame with the PCA data.

## 5. Find the Best Value for k Using the PCA Data:

-Apply the elbow method using the PCA data to find the best value for k.
-Visualize the inertia values and identify the optimal k.
-Answer the questions regarding the best value for k compared to the original data.

## 6. Cluster Cryptocurrencies with K-Means Using the PCA Data:

-Initialize the K-means model with the best value for k.
-Fit the model using the PCA data.
-Predict the clusters and add a new column to the DataFrame with the predicted clusters.
-Create a scatter plot using pandas' plot.

## 7. Determine the Weights of Each Feature on Each Principal Component:

-Create a DataFrame showing the weights of each feature for each principal component.
-Analyze which features have the strongest positive or negative influence on each component.

## 8. Coding Conventions and Formatting:

-Ensure proper placement of imports, naming conventions, DRY principles, concise logic, and creative engineering.

## 9. Deployment and Submission:

-Create a GitHub repository containing the project files.
-Add files to the repository using the command line with appropriate commit messages.

## 10. Code Comments:

-Add concise and relevant comments throughout the code to aid understanding for other developers.