# Problem Statement:
In business, it is crucial to understand customers'needs and desire in order to provide optimize their customer journey and maximize their potential value to our business. In order to do so, we firstly need to segment our customers into groups that share something in common. With that, only we are able to curate products and services that cater to their needs.

Conventional method practice of customer segmentation includes using RFM analysis, customers are assigned a ranking number of 1,2,3,4, or 5 (with 5 being highest) for each RFM parameter. The three scores together are referred to as an RFM "cell" . The database is sorted to determine which customers were "the best customers" in the past, with a cell ranking of "555" being ideal.

However, in this project uses unsupervised machine learning approach ie DBSCan,KMean clsutering to segment customers into different groups using other features on top of based on customers RFM score .


# Dataset:
Dataset is obtained from *uci machine learning repository* https://archive.ics.uci.edu/ml/datasets/Online+Retail+II

Data Dictionary provided is as below:

|Column |Data Type|Description|
|:------|:------|:------|
|Invoice|Nominal|A 6-digit integral number uniquely assigned to each transaction. If this code starts with the letter 'c', it indicates a cancellation|
|StockCode|Nominal|Product (item) code.A 5-digit integral number uniquely assigned to each distinct product|
|Description|Nominal|Product (item) name|
|Quantity|Numeric|The quantities of each product (item) per transaction|
|InvoiceDate|Numeric|Invice date and time.The day and time when a transaction was generated|
|UnitPrice|Numeric|Unit price.Product price per unit in sterling (Â£).|
|CustomerID|Nominal|Customer numberA 5-digit integral number uniquely assigned to each customer.The name of the country where a customer resides.|
|Country|Nominal|Country name|


# Conclusion and Recommendations

In this project, unsupervised learning method ie DBScan, KMeans and KMeans with PCA has been used and KMeans clustering gives a more intuitive, explainable cluster.

When using Customers' Recency, Frequency and Monetary as Features, the appropriate clusters formed with KMeans at k=5. Clusters formed are Champion/Outliers,Loyal,Rookies/Potential Loyal, Hybernating and Needs Attention/Loosing Soon.

When using all Customers' attribute as Features, the appropriate clusters formed with KMeans at k=6. Clusters formed are Loyal, Potential Loyal, About to Sleep, Needs Attention, Hybernating and Lost Whale.


Based on the above 2 types of clustering, stakeholder should discuss to decide on which attributes and k value to be used. <br>

After this unsupervised machine learning has learnt on features, number of cluster and labeled clusters, supervised machine learning like classification can be done for new data.<br>

Further work can be done on clustering and categorizing products into a few categories and include items purchased as one of the features in KMeans Clustering.


