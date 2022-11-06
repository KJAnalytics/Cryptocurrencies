# Cryptocurrencies - Cashing in on Digital Currency Technology
The Advisory Services Team at Accountability Accounting, a prominent investment bank is considering offering a new cryptocurrency visual portfolio.  The need arises out of the increasing interest by their customers interested in Digital currencies.  This project is commissioned to create a visual report that is easily understood and predictive in nature to help guide the investor understand the range of cryptos in the market and the Total mined vs. Total Available for a particular currency.

## Resources
Data Source: crypto_data.csv, CryptoCompare
Software: Python 3.7.7, Anaconda Navigator 1.9.12, Conda 4.8.4, Jupyter Notebook 6.0.3
Libraries Utilized: Pandas, scikit-learn, Plotly, plotly.express, hvPlot, Clustering, StandardScaler, inertia, gitdummies

## Methodology/Analysis
Starting with the basis of an unsupervised modeling process the steps undertaken for the project include:
- preprocessing the database,
-reducing the data dimension using Principal Component Analysis,
- clustering cryptocurrencies using K-Means,
- visualizing classification results with 2D and 3D scatter plots.

Data inputs to the preprocessing and cleaning phase included a total of 1252 lines of data with 7 columns of descriptive and numeric datapoints.  The data is read in from Crypto.csv utilizing pandas.  The data was then cleaned to removed unnecessary columns of data and any rows with nulls.  Next it was fed through the #getdummies" in order to convert text to encoded numerial values.  Data is then scaled utilizing StandardScaler. "   Finally, utilizing the K-means algorithm and inertia  the K value  to use.  Output to determine the K-value is shown in the elbow curve below.  4 clusters is recommended.
https://github.com/KJAnalytics/Cryptocurrencies/blob/main/images/K-means_Elbowchart.png

In Deliverable 4 visualizations are created with 3D-Scatter plots.  Data for the plots is generated by processing the data through the PCA process utilizing inertia in order to reduce the crypto dimensions down to 3 principal components.

Outputs of this process include the following:
- A Table of Tradable Cryptocurrencies
        https://github.com/KJAnalytics/Cryptocurrencies/blob/main/images/Tradable_Currencies.png

- A 3D scatter plot output from the PCA process - Principle Component (PC1, PC2, PC3) versus Coinname
        https://github.com/KJAnalytics/Cryptocurrencies/blob/main/images/3Dhvplot-%20Algorithm-vs-coinname.png

- A 3D scatter plot  - Coinsupply-vs-coinsmined
        https://github.com/KJAnalytics/Cryptocurrencies/blob/main/images/3Dhvplot-Coinsupply-vs-coinsmined.png


## Summary
532 cryptocurrencies have been classified and plotted based on similarities of their features. Graphical representations are interactive with popups available to determine which crypto name is positioned within the 3D models to allow investors to maneuver through the carts based on their individual interests.

## Summary
Future improvements could include 
- improving the database from static to one that is updated daily with current information through a cloud server/repository such as AWS/RDS that can integrate the database updates.  This information could then be linked to a web page and refreshed automatically on a daily basis.
Particularities of each group need to be analyzed to determined their performance and potential interest for the investment bank's clients.
- reevaluating the factors include in the model.  Validation of the factor choices.