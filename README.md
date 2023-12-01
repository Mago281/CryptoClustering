# CryptoClustering

## **Objective**

To use Python and Unsupervised Learning to predict if cryptocurrencies are affected by 24-hour or 7-day price changes.

---

## **Instructions**

1. The `Crypto_Clustering_starter_code.ipynb` file was provided; the file was renamed to `Crypto_Clustering.ipynb`.
   
2. Loaded the `crypto_market_data.csv` into a DataFrame.
   
3. Got the summary statistics and plotted the data to see what the data looked like before proceeding.

---

## **Prepared the data**

- Use the `StandardScaler()` module from `scikit-learn` to normalize the data from the CSV file.

- Create a DataFrame with the scaled data and set the "_coin_id_" index from the original DataFrame as the index for the new DataFrame.

   * The first five rows of the scaled DataFrame should appear as follows:
 
     

---

## **Find the Best Value for `k` Using the Original Scaled DataFrame**

Use the elbow method to find the best value for `k` using the following steps:

  - Create a list with the number of `k` values from 1 to 11.
    
  - Create an empty list to store the inertia values.
    
  - Create a `for` loop to compute the inertia with each possible value of `k`.
    
  - Create a dictionary with the data to plot the elbow curve.
    
  - Plot a line chart with all the inertia values computed with the different values of `k` to visually identify the optimal value for `k`.
    
  - Answer the following question in your notebook: **_What is the best value for `k` ?_**

---

## **Cluster Cryptocurrencies with K-means Using the Original Scaled Data**

Use the following steps to cluster the cryptocurrencies for the best value for k on the original scaled data:

- Initialise the K-means model with the best value for `k`.

- Fit the K-means model using the original scaled DataFrame.

- Predict the clusters to group the cryptocurrencies using the original scaled DataFrame.

- Create a copy of the original data and add a new column with the predicted clusters.

- Create a scatter plot using hvPlot as follows:

   * Set the x-axis as _"PC1"_ and the y-axis as _"PC2"_.

   * Colour the graph points with the labels found using K-means.

   * Add the _"coin_id"_ column in the `hover_cols` parameter to identify the cryptocurrency represented by each data point.

---

## **Optimise Clusters with Principal Component Analysis**

- Using the original scaled DataFrame, perform a PCA and reduce the features to three principal components.

- Retrieve the explained variance to determine how much information can be attributed to each principal component and then answer the following question in your notebook:

    * **What is the total explained variance of the three principal components?**
      

- Create a new DataFrame with the PCA data and set the _"coin_id"_ index from the original DataFrame as the index for the new DataFrame.

    * The first five rows of the PCA DataFrame should appear as follows:



---

## **Find the Best Value for k Using the PCA Data**

Use the elbow method on the PCA data to find the best value for `k` using the following steps:

- Create a list with the number of k-values from 1 to 11.

- Create an empty list to store the inertia values.

- Create a `for` loop to compute the inertia with each possible value of `k`.

- Create a dictionary with the data to plot the Elbow curve.

- Plot a line chart with all the inertia values computed with the different values of `k` to visually identify the optimal value for `k`.

- Answer the following question in your notebook:

   * _**What is the best value for `k` when using the PCA data?**_
     

   * _**Does it differ from the best k value found using the original data?**_




---

## **Cluster Cryptocurrencies with K-means Using the PCA Data**

Use the following steps to cluster the cryptocurrencies for the best value for `k` on the PCA data:

- Initialise the K-means model with the best value for `k`.

- Fit the K-means model using the PCA data.

- Predict the clusters to group the cryptocurrencies using the PCA data.

- Create a copy of the DataFrame with the PCA data and add a new column to store the predicted clusters.

- Create a scatter plot using hvPlot as follows:

   * Set the x-axis as _"price_change_percentage_24h"_ and the y-axis as _"price_change_percentage_7d"_.

   * Colour the graph points with the labels found using K-means.

   * Add the _"coin_id"_ column in the `hover_cols` parameter to identify the cryptocurrency represented by each data point.

- Answer the following question:

   * **What is the impact of using fewer features to cluster the data using K-Means?**

















