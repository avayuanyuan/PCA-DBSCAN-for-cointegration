# PCA-DBSCAN-for-cointegration

1. Idea of locating data:

Stocks that share loadings to common factors (defined below) in the past should be related in the future.

Stocks of similar market caps should be related in the future.

We should exclude stocks in the industry group "Conglomerates"(industry code 31055) since Morningstar analysts classify stocks into industry groups primarily based on similarity in revenue lines. 
"Conglomerates" is a catch-all industry. 

Creditworthiness in an important feature in future company performance. Morningstar analysts calculate a tustworthy model for credit.

2. Data we are using comes from Quantopian. We use all of stock stickers shown in quantopian. Use history price as database.


3. Instead of calculating alpha factors, we can use PCA to reduce the dimensionality of the returns data and extract the historical latent common factor loadings for each stock.

4. Then use DBSCAN to leaves out stocks which do not neatly fit into a cluster

5. Finally, we have sensible clusters of common stocks. We can validate the cointegration relationships to get the strong cointegrated pairs and do mean reverting strategy.
