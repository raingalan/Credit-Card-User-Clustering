# Credit-Card-User-Clustering

In this project, my group performed data cleaning & EDA on a credit card transaction history dataset covering 2020-2021 transactions. Following this, we further analyzed customer behavior by performing a Revenue-Frequency-Monetary (RFM) Analysis to determine the length of time since a unique customer's last purchase, frequency of card usage, and total amount spent by customers. Furthermore, the labels derived from the RFM Analysis was used to segment the customers using K-Means clustering.

For EDA, we accomplished the following:
1. Compared total transaction value and count on a monthly basis for 2020-2021
2. Determined the demographic of the credit card users in terms of age, gender and location.
3. Identified the top 5 categories that contributed the highest transaction count and value in 2021.

For the K-means clustering, the data was prepared as follows: 
1. Obtained metrics for Recency, Frequency and Monetary for each unique customer
2. Evaluated the skewness of the distribution and performed log transformation and standardization
3. Applied K-means clustering and best number of clusters was determined using the elbow method on Intertia and Silhouette scores
4. Segmentation of best clusters was evaluated using a Snake plot

Overall, the resulting clustering is as follows: 
- **Cluster 0** is defined by the "Best Customers" segment which has recent purchases, are the most frequent buyers, and spent the most.
- The **Cluster 1** customers are the "Low Spenders" segment as they have several recent purchases for some time(R=3), but has less frequently frequent purchases and lower total amount spent.
- Customers in **Cluster 2** can be interpreted as customers at risk of churning as their last purchase is long ago (R=4),purchased very few (F=4) and spent little (M=4).Company has to come up with new strategies to make them permanent members.   
- **Cluster 3** customers are "Average Spenders" who made recent purchases and are in between the customers in Cluster 0 and 1 in terms of frequency of transactions and total amount spend.
- Notably, Clusters 0, 1 and 3 are mainly differentiated by the levels of frequency and total amount spent. These groups are mostly similar in terms of recency as they all have made recent purchases.
