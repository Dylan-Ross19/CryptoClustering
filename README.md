# CryptoClustering
## Dylan Ross
---
## 1. Load and Prepare the Data:

-Load the CSV file into a DataFrame and set the index to "coin_id".
 - [x]Provided for in source_coude
-Use StandardScaler to normalize the data.
 - [x]
-Create a DataFrame with the scaled data, using "coin_id" as the index.
 - [x]

## 2. Find the Best Value for k Using the Original Scaled DataFrame:

-Implement the elbow method algorithm to find the best value for k.
 - [x]
-Visualize the inertia values for different k values and identify the optimal k.
 - [x]
-Answer the question regarding the best value for k.
 - [x]

## 3. Cluster Cryptocurrencies with K-Means Using the Original Scaled Data:

-Initialize the K-means model with the best value for k.
 - [x]
-Fit the model using the original scaled DataFrame.
 -[x]
-Predict the clusters and add a new column to the DataFrame with the predicted clusters.
 - [x]
-Create a scatter plot using pandas' plot.
 - [x]

## 4. Optimize Clusters with Principal Component Analysis (PCA):

-Create a PCA model instance with n_components=3.
 - [x]
-Reduce the features to three principal components.
 - [x]
-Calculate and interpret the explained variance.
 - [x]
-Create a new DataFrame with the PCA data.
 - [x]

## 5. Find the Best Value for k Using the PCA Data:

-Apply the elbow method using the PCA data to find the best value for k.
 - []
-Visualize the inertia values and identify the optimal k.
 - []
-Answer the questions regarding the best value for k compared to the original data.
 - []

## 6. Cluster Cryptocurrencies with K-Means Using the PCA Data: 

-Initialize the K-means model with the best value for k.
 - []
-Fit the model using the PCA data.
 - []
-Predict the clusters and add a new column to the DataFrame with the predicted clusters.
 - []
-Create a scatter plot using pandas' plot.
 - []

## 7. Determine the Weights of Each Feature on Each Principal Component:

-Create a DataFrame showing the weights of each feature for each principal component.
 - []
-Analyze which features have the strongest positive or negative influence on each component.
 - []

## 8. Coding Conventions and Formatting:

-Ensure proper placement of imports, naming conventions, DRY principles, concise logic, and creative engineering.
 - []

## 9. Deployment and Submission:

-Create a GitHub repository containing the project files.
 - []
-Add files to the repository using the command line with appropriate commit messages.
 - []

## 10. Code Comments:

-Add concise and relevant comments throughout the code to aid understanding for other developers.
 - []