
# Crypto Clustering

Using Python and Unsupervised Learning to predict if cryptocurrencies are affected by 24-hour or 7-day price changes.

### Installation & Requirements

This project can be run in a Jupyter notebook with the following libraries and dependencies imported pandas, hvplot.pandas, sklearn.cluster KMeans, sklearn.decomposition PCA, sklearn.preprocessing Standard Scaler. 

## Description

Load the `crypto_market_data.csv` into a DataFrame, get the summary statistics, and plot the data to see what the data looks like before proceeding.

<img width="884" alt="Screenshot 2023-10-28 at 12 13 52 PM" src="https://github.com/CJunger/CryptoClustering/assets/131617662/10addea4-4025-4dc4-9253-53b471d6033c">


#### **Prepare the data**

* Use the `StandardScaler()` module from `scikit-learn` to normalize the data from the CSV file.
* Create a DataFrame with the scaled data and set the "coin\_id" index from the original DataFrame as the index for the new DataFrame.

#### Find the Best Value for k Using the Original Scaled DataFrame

<img width="743" alt="Elbow_Plot_Original" src="https://github.com/CJunger/CryptoClustering/assets/131617662/d1dac9c2-556d-4068-a839-71e2fe4147a5">

#### Cluster Cryptocurrencies with K-means Using the Original Scaled Data

<img width="802" alt="Screenshot 2023-10-28 at 12 26 19 PM" src="https://github.com/CJunger/CryptoClustering/assets/131617662/3deae930-de56-4c3f-ba6a-9b705f91a4a9">

#### Optimize Clusters with Principal Component Analysis

* What is the total explained variance of the three principal components? 85%

#### Find the Best Value for k Using the PCA Data

<img width="735" alt="Elbow_Curve_with_PCA" src="https://github.com/CJunger/CryptoClustering/assets/131617662/c19484b1-73a3-4405-bce0-45ecb190c357">

* What is the best value for `k` when using the PCA data? 4
* Does it differ from the best k value found using the original data? No, it is very similar

#### Cluster Cryptocurrencies with K-means Using the PCA Data

<img width="737" alt="Screenshot 2023-10-28 at 12 30 32 PM" src="https://github.com/CJunger/CryptoClustering/assets/131617662/7bce71d3-4bcf-43f8-9b67-6c9e44831878">

* What is the impact of using fewer features to cluster the data using K-Means? We reduced the variance by using the PCA to eliminate outliers.

###### These are the combined elbow original and PCA data plots.

<img width="770" alt="Screenshot 2023-10-28 at 12 31 28 PM" src="https://github.com/CJunger/CryptoClustering/assets/131617662/4dab7fe0-7e56-4442-87df-58d691ebb40d">

###### This is the cluster comparisons.

<img width="1298" alt="Screenshot 2023-10-28 at 12 35 53 PM" src="https://github.com/CJunger/CryptoClustering/assets/131617662/b473d1ac-0894-4df3-91a3-58de497b5796">


### Installation & Requirements

This project can be run in a Jupyter notebook with the following libraries and dependencies imported pandas, hvplot.pandas, sklearn.cluster KMeans, sklearn.decomposition PCA, sklearn.preprocessing Standard Scaler. 

### 
