# Cryptocurrencies - Cashing in on Digital Currency Technology
The Advisory Services Team at Accountability Accounting, a prominent investment bank is considering offering a new cryptocurrency visual portfolio.  The need arises out of the increasing interest by their customers interested in Digital currencies.  This project is commissioned to create a visual report that is easily understood and predictive in nature to help guide the investor understand the range of cryptos in the market and the Total mined vs. Total Available for a particular currency.

## Resources
Data Source: crypto_data.csv, CryptoCompare
Software: Python 3.7.7, Anaconda Navigator 1.9.12, Conda 4.8.4, Jupyter Notebook 6.0.3
Libraries Utilized: Pandas, scikit-learn, Plotly, plotly.express, hvPlot, Clustering, StandardScaler, inertia

## Methodology/Analysis
Starting with the basis of an unsupervised modeling process the steps undertaken for the project include:
- preprocessing the database,
-reducing the data dimension using Principal Component Analysis,
- clustering cryptocurrencies using K-Means,
- visualizing classification results with 2D and 3D scatter plots.

Data inputs to the preprocessing and cleaning phase included a total of 1252 lines of data with 7 columns of descriptive and numeric datapoints.  The data is read in from Crypto.csv utilizing pandas.  The data was then cleaned to removed unnecessary columns of data and any rows with nulls.  

pic here

Next the data was processed through the PCA (principle component analysis) process utilizing the K-means algorithm and inertia to determine the K value to use.  Output to determine the K-value is shown in the elbow curve below.  The output recommends 4 clusters to categorize the information.

elbow chart here.




Visualizing Cryptocurrencies Results
3D-Scatter plot with clusters


This 3-D scatter plot was obtained using the PCA algorithm to reduce the crytocurrencies dimensions to three principal components.

2D-Scatter plot with clusters


This 2-D scatter plot was obtained using the PCA algorithm to reduce the crytocurrencies dimensions to two principal components.

Both these scatter plots show the distribution and the four clusters of cryptocurrencies.
We can identify the outliers like the unique cryptocurrency in the class #2.

Tradable Cryptocurrencies Table


Most of the cryptocurrencies are part of class #0 and #1.
The snapshot above shows that BitTorrent is the only cryptocurrency in class #2.

2D-Scatter plot with TotalCoinMined vs TotalCoinSupply


Plotting the scatter plot from two cryptocurrency features directly does not efficiently segregate the different classes. Then using the PCA algorithm is the right method for better visualizations.

Summary
We have identified the classification of 532 cryptocurrencies based on similarities of their features.
Particularities of each group need to be analyzed to determined their performance and potential interest for the investment bank's clients.