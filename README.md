# Cryptocurrencies

## Abstract

This project aims to use unsupervised machine learning to discover patterns in a given dataset of cryptocurrencies. Clustering and the K-means algorithm are used with principal component analysis to refine the data further. The following packages were used with Anaconda: Pandas, numpy, sklearn, plotly, hvplot, and re. The project's goals were to clean the data for principal component analysis, predict clusters of cryptocurrencies using the K-means algorithm, and present the clusters using hvplot.

## Discussion

The first step was to clean the data. I was required to remove all cryptocurrencies that were not trading, did not have a defined algorithm, cryptocurrencies with a null value in any column, and cryptocurrencies that have not been mined. During the cleaning process, the cryptocurrency abbreviations were set as the data frame's index. Dummy variables were creating using pandas' .get_dummies function. I standardized the data using StandardScaler from sklearn and reduced the data's dimensions with principal component analysis(PCA) from sklearn for the KMeans algorithm. I created an elbow curve to determine the best value for the K parameter, 25. With the data clustered, the data frame was required to be turned into a tabular form for hvplot. The data was plotted using 'TotalCoinsMined' as the x-value and 'TotalCoinSupply' as the y-value.

## Conclusion

The scatter plot of TotalCoinsMined and TotalCoinSupply showed a trend of increasing supply as more coins were minted. BitTorrent had the largest total of coins mined and the largest supply. Fiii had the smallest mined total and the smallest supply. There were three notable outliers: TurtleCoin, MoonCoin, and EliteCoin, having relatively large coin supplies, but few of the coins had been mined compared to the rest of the data.

![TotalCoinSupply versus TotalCoinsMined Scatter Plot](https://github.com/mkeire/Cryptocurrencies/blob/master/Resources/bokeh_plot.png

![Principal Componened, class, TotalCoinsMined, and TotalCoinSupply Scatter Plot](https://github.com/mkeire/Cryptocurrencies/blob/master/Resources/bokeh_plot2.png