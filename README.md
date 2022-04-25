# Cryptocurrencies

## Analysis Overview
In this project we analyzed the market of cryptocurrencies using a database of curreent coins by leveraging unspuervised machine learning to classify coins depending on their features. From these models we were able to build reports on what the machine learning algorithm found via an interactable table, a 3D scatter plot, and a 2D plot of current coins mined relative to total available supply.

The aim is to leverage unsupervised machine learning classification reports to convince a bank or financial investor to invest in cryptocurrency (suggest it to clients) based on current trends, prominance, and successes of currently tradable cryptocurrencies. 

The following methods are used within our analysis:
- Preprocessing and Cleaning via Pandas .isna(), .drop(), and "~",
- Data dimensionality reduction via PCA (Principal Component Analysis),
- Elbow Curve to determine optimal KMeans clusters for our classification model,
- K-Means clustering for our cryptocurrency classification algortithm,
- 3D & 2D scatterplot data visualizaiton of clusters and classifications via hvplot and plotly.express.
<br><br>

## Resources
- Data Source: [crypto_data.csv](https://github.com/sterlingvm/Cryptocurrencies/blob/main/Resources/crypto_data.csv)
- Software: Python 3.8.8, Visual Studio Code 1.66.2, Jupyter Notebook 6.4.5
<br><br>

## Results
After preprocessing, scaling, and cleaning the crypto csv data, we found a total of 532 tradable cryptocurrencies.
<br><br>

### Clustering Cryptocurrencies using K-Means - Elbow Curve
We want to explore the cryptocurrency data and have no specific idea of what outcomes we aere looking for, so we use unsupervised machine learning to explore the relationships between the cryptos and configure an idea of the different groups of cryptos based on their features. In this example, we'll specifically be using a K-Means algorithm.

To determine our ideal k value for our K-Means algorithm, we'll generate an Elbow Curve using an inertia metric and a range of possible k values: 
<p align="center">
    <img src="https://github.com/sterlingvm/Cryptocurrencies/blob/main/Resources/elbow_curve.png"> 
</p>
a k value of 4 clusters seems to be the best as that point clearly serves as the pivot point between vertical and horizontal inertia, meaning it is the pivotal point with the most optimal returns for categorizing our data via its features based on inertia.
<br><br>

### Visualizing Cryptocurrencies Results
#### 3D-Scatter plot with clusters
<p align="center">
    <img src="https://github.com/sterlingvm/Cryptocurrencies/blob/main/Resources/3d.png"> 
</p>
By ising PCA (Principal Component Analysis) to reduce the dimensionality of the dataset to 3 principal components we were able to apply our data to a #D scatter plot graph where our 3 principal components served as the x, y, and z axes. The resulting graph demonstrates the 4 distinct clusters of cryptocurrencies, A.K.A. the 4 distinct types of cryptocurrencies in the data.
<br><br>

#### Tradable Cryptocurrencies Table
<p align="center">
    <img src="https://github.com/sterlingvm/Cryptocurrencies/blob/main/Resources/coin_table.png"> 
</p>
Above is an interactable table that displays a classification report for all of the 532 tradable cryptocurrencies from the data. Most of the data is from classes 1 or 0.
<br><br>

#### 2D-Scatter plot with TotalCoinMined vs TotalCoinSupply
<p align="center">
    <img src="https://github.com/sterlingvm/Cryptocurrencies/blob/main/Resources/2d_totalmined_totalsupply.png"> 
</p>
This is a display of cryptocurrencies based on how much available supply has been mined and is thus available to the public. As coins continue to be mined, supply will rise so price will fluxuate; however, once the supply has reached its cap (the total coin supply) then the supply will stagnate and price will rise as finite scarity takes its economic affect. As a result, leveraging this plot against our 3D scatterplot derived from 3 principal components can help financial stakeholders interested in invisting in cryptocurrency choose a favorable coin and understand where it stands within the total market of cryptocurrency effectively. Cryptocurrency is still young though, so it would probably be suggested to follow cryptocurrencies that are the same type as popular and well-sustained coins such as Bitcoin, Ethereum, LiteCoin, etc.
<br><br>

## Summary
Our Unsupervised machine learning KMeans algorithm has classified 532 tradable cryptocurrencies based on the features and data in the crypto_data.csv.
Investment clients and stakeholders should use this project and the classification reports as a starting point for understanding which cryptocurrencies pique their interest before doing more extensive research intor those crypto candidates later on.