# CryptoClustering-

## **Objective**

To use Python and Unsupervised Learning to predict if cryptocurrencies are affected by 24-hour or 7-day price changes.

---

## **Instructions**

1. The 'Crypto_Clustering_starter_code.ipynb' file was provided; the file was renamed to `Crypto_Clustering.ipynb'.
   
2. Loaded the crypto_market_data.csv into a DataFrame.
   
3. Got the summary statistics and plotted the data to see what the data looked like before proceeding.

---

## **Prepared the data**

- Use the StandardScaler() module from scikit-learn to normalize the data from the CSV file.
- Create a DataFrame with the scaled data and set the "coin_id" index from the original DataFrame as the index for the new DataFrame.
   * The first five rows of the scaled DataFrame should appear as follows:

---

## **Find the Best Value for `k` Using the Original Scaled DataFrame**

Use the elbow method to find the best value for `k` using the following steps:

  - Create a list with the number of k values from 1 to 11.
    
  - Create an empty list to store the inertia values.
    
  - Create a `for` loop to compute the inertia with each possible value of `k`.
    
  - Create a dictionary with the data to plot the elbow curve.
    
  - Plot a line chart with all the inertia values computed with the different values of `k` to visually identify the optimal value for `k`.
    
  - Answer the following question in your notebook: _What is the best value for `k` ?_

---

## **Cluster Cryptocurrencies with K-means Using the Original Scaled Data**

Use the following steps to cluster the cryptocurrencies for the best value for k on the original scaled data:

- Initialise the K-means model with the best value for `k`.

- Fit the K-means model using the original scaled DataFrame.

- Predict the clusters to group the cryptocurrencies using the original scaled DataFrame.

- Create a copy of the original data and add a new column with the predicted clusters.

- Create a scatter plot using hvPlot as follows:

   * Set the x-axis as "PC1" and the y-axis as "PC2".

   * Colour the graph points with the labels found using K-means.

   * Add the "coin_id" column in the `hover_cols` parameter to identify the cryptocurrency represented by each data point.
















