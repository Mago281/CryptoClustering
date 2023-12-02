# CryptoClustering

## **Objective**

To use Python and Unsupervised Learning to predict if cryptocurrencies are affected by 24-hour or 7-day price changes.

---

## **Instructions**

1. The `Crypto_Clustering_starter_code.ipynb` file was provided and this file was renamed as `Crypto_Clustering.ipynb`.
   
2. The `crypto_market_data.csv` was loaded into a DataFrame and the sample data was displayed:

   ![image](https://github.com/Mago281/CryptoClustering/assets/131424690/3e635b09-d9a0-4631-92ad-796be9b0ef37)
    
3.  Generated the summary statistics:

     ![image](https://github.com/Mago281/CryptoClustering/assets/131424690/cfe8217b-b8df-4ddc-9f16-c15cca15be3e)
   
4. Plotted the data to see what was in the DataFrame:

   ![image](https://github.com/Mago281/CryptoClustering/assets/131424690/ad932e55-01ff-46e8-bfa0-0685567cca1d)

---

## **Prepared the data**

- The `StandardScaler()` module from `scikit-learn` was used to normalize the data from the CSV file.

- Created a DataFrame with the scaled data and set the "_coin_id_" index from the original DataFrame as the index for the new DataFrame.

   * Please refer to the image below for the first five rows of the scaled DataFrame:
     
    ![image](https://github.com/Mago281/CryptoClustering/assets/131424690/ca8947a4-4101-45f1-9d5d-8598da67218c)


---

## **Found the Best Value for `k` Using the Original Scaled DataFrame**

Used the elbow method to find the best value for `k` using the following steps:

  - Created a list with the number of `k` values from 1 to 11.
    
  - Created an empty list to store the inertia values.
    
  - Created a `for` loop to compute the inertia with each possible value of `k`.
    
  - Created a dictionary with the data to plot the elbow curve.
    
  - Plotted a line chart with all the inertia values computed with the different values of `k` to visually identify the optimal value for `k`.

     <img src="https://github.com/Mago281/CryptoClustering/assets/131424690/bd3f4052-6d7f-4594-b4dd-a425ff556df0" width="700" height="300">
    

  - Answered the following question:
   ** _What is the best value for `k` ?_**
    ### 4

---

## **Clustered Cryptocurrencies with K-means using the original scaled data**

Performed the following steps to cluster the cryptocurrencies for the best value for `k` on the original scaled data:

- Initialised the K-means model with the best value for `k`.

- Fit the K-means model using the original scaled DataFrame.

- Predicted the clusters to group the cryptocurrencies using the original scaled DataFrame.

- Created a copy of the original data and added a new column with the predicted clusters:

  ![image](https://github.com/Mago281/CryptoClustering/assets/131424690/bbd4055d-4a53-4def-8e91-c9965c0a4fb8)

- Created a scatter plot using hvPlot as follows:

   * Set the x-axis as _"PC1"_ and the y-axis as _"PC2"_.

   * Coloured the graph points with the labels found using K-means.

   * Added the _"coin_id"_ column in the `hover_cols` parameter to identify the cryptocurrency represented by each data point.
 
  ![image](https://github.com/Mago281/CryptoClustering/assets/131424690/6c00b1ee-869c-4f87-925f-40d1bb686ba8)


---

## **Optimised Clusters with Principal Component Analysis (PCA)**

- Using the original scaled DataFrame, perform a PCA and reduce the features to three principal components.

- Retrieve the explained variance to determine how much information can be attributed to each principal component and then answer the following question in your notebook:

    * _**What is the total explained variance of the three principal components?**_
    * 
      

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

















