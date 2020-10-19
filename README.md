# New-York-Bus-Clustering

Clustering New York City Buses to learn if there is a way to pick out patterns of late busses. The data was obtained from a New York City MTA buses data stream service and can be located in [This Kaggle Link](https://www.kaggle.com/stoney71/new-york-city-transport-statistics?select=mta_1710.csv). 

To determine the best method of clustering, PCA and t-SNE was applied to KMeans and Agglomerative Clustering. KMeans with t-SNE proved to be the best way to cluster the New York City Buses dataset.

## Methodology

### KMeans Clustering

K values of 3-10 were chosen and compared to decide what the most accurate amount of clusters should be. PCA and t-SNE was applied to each cluster, and the silhouette scores were calculated. 

### Agglomerative Clustering

Three different measurements of linkage for Agglomerative Clustering were used:
* Complete
* Average
* Ward

Once again, PCA and t-SNE was applied to each cluster and n_clusters was set to 4-10 for each linkage measurement.

### Comparing Dimensionality Reduction Methods

To determine the amount of components used for PCA, the cumulative sum was calculated to equate to 90% variance. This resulted in 10 components and explains why n_components = 10 was chosen when using PCA. As for t-SNE, a more global approach was taken to try to group up the data, and therefore a perplexity of 50 was used. 

Scatterplots were created for t-SNE and PCA when applied to the data. Comparing the two charts, t-SNE was able to separate and group up the data much more efficiently than PCA.

![Plot](t_SNE.png)
![Plot](pca.png)
