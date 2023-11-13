# Crypto Clustering Challenge

In this task, you will employ your expertise in Python and unsupervised learning to forecast whether cryptocurrencies are influenced by alterations in prices over a 24-hour or 7-day period.

### Prepare the Data
* Utilize the StandardScaler() module from scikit-learn to standardize the data obtained from the CSV file.

* Generate a DataFrame containing the standardized data and designate the "coin_id" index from the original DataFrame as the index for the new DataFrame.

### Determine the Optimal k Value Using the Original Scaled DataFrame <br>
Employ the elbow method to identify the optimal k value through the following steps: <br>

1. Formulate a list encompassing k values ranging from 1 to 11.
2. Establish an empty list to accumulate the inertia values.
3. Employ a for loop to calculate inertia for each conceivable k value.
4. Construct a dictionary containing data for plotting the elbow curve.
5. Generate a line chart depicting all inertia values computed with varying k values, facilitating visual identification of the optimum k value.
6. Pose the question in your notebook: What is the most suitable k value?

### Cluster Cryptocurrencies with K-means Using the Original Scaled Data <br>
Apply the subsequent steps to cluster cryptocurrencies for the optimal k value on the originally scaled data: <br>

1. Initialize the K-means model with the determined optimal k value.
2. Train the K-means model using the initially scaled DataFrame.
3. Utilize the model to predict clusters, grouping cryptocurrencies based on the initial scaled DataFrame.
4. Duplicate the original data, appending a new column with predicted clusters.
5. Formulate a scatter plot using hvPlot with the x-axis as "PC1" and the y-axis as "PC2".
6. Color the graph points according to the labels derived from K-means.
7. Include the "coin_id" column in the hover_cols parameter to identify each cryptocurrency represented by a data point. <br>

### Enhance Clusters with Principal Component Analysis
Using the original scaled DataFrame, conduct Principal Component Analysis (PCA) to condense features into three principal components.

Retrieve the explained variance to gauge the information attributed to each principal component and answer the following question in your notebook: <br>

What is the total explained variance of the three principal components? <br>

Generate a novel DataFrame with PCA data, designating the "coin_id" index from the initial DataFrame as the index for this new DataFrame.<br>

### Determine the Optimal k Value Using the PCA Data <br>
Apply the elbow method to the PCA data to identify the best k value through the following steps: <br>

1. Create a list containing k-values ranging from 1 to 11.
2. Establish an empty list to compile the inertia values.
3. Utilize a for loop to calculate inertia for each conceivable k value.
4. Formulate a dictionary with the data needed to plot the Elbow curve.
5. Generate a line chart displaying all inertia values calculated with different k values, aiding in the visual identification of the optimal k value.
6. Answer the subsequent question in your notebook: What is the most suitable k value when utilizing the PCA data?
7. Assess whether it differs from the optimal k value identified using the original data.

### Cluster Cryptocurrencies with K-means Using the PCA Data <br>
Implement the subsequent steps to cluster cryptocurrencies for the optimal k value on the PCA data:

1. Initialize the K-means model with the determined optimal k value.
2. Train the K-means model using the PCA data.
3. Employ the model to predict clusters, grouping cryptocurrencies based on the PCA data.
4. Duplicate the DataFrame with PCA data, appending a new column to store predicted clusters.
5. Create a scatter plot using hvPlot with the x-axis as "price_change_percentage_24h" and the y-axis as "price_change_percentage_7d".
6. Color the graph points according to labels derived from K-means.
7. Include the "coin_id" column in the hover_cols parameter to identify each cryptocurrency represented by a data point.
8. Address the following question: What is the influence of using fewer features to cluster the data with K-Means?

## How to Install and Run the script

To run this script:
1. Copy the git link in your local git repository
2. Ensure *Resources* directory and *Crypto_Clustering.ipynb* file are present
3. Ensure the respective csv datasets are present in the *Resources* folder
4. Run the script using **Jupyter Notebook** from *CryptoClustering* directory and view results
5. Be sure to run the entire script using *Restart & Run All option* from *Kernel* in *Jupyter Notebook* to get error free results
6. Or, you could alternatively run each block of code individually starting from the very top 

![Elbow Curve](images/Elbow_curve.png)

![Scatter Plots](images/Scatter_plot.png)

---
## Credits

To write this script, I used the starter code provided and followed the challenge requirements meticulously <br> 

---
## References
https://holoviz.org/tutorial/Composing_Plots.html
