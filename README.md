https://github.com/balaji-2021/Capstone3/blob/main/images/Screen%20Shot%202021-08-24%20at%207.00.36%20PM.png

# Customer segmentation

Customer Segmentation is the strategy that is used to find discrete customer groups that share similar characteristics. The idea behind customer segmentation is to split the user-base into smaller groups that can be targeted with specialized content and offers.
The purpose of the project is to understand:
* How can the data be preprocessed in order to correctly segment users into groups of similar people?
* What is a reasonable cluster size?
* What insights can we get from these cluster segments?
* How can the created clusters be used in the application to target users with specialized content e.g. item recommendations? 

## Data Used

The data used is a public dataset from the UCI Machine Learning Repository on transactions occurring between 01/12/2010 and 09/12/2011 for a UK-based and registered non-store online retail. 

The company mainly sells unique all-occasion gifts. Many customers of the company are wholesalers.

## Approach

In the context of customer segmentation, cluster analysis is the use of a mathematical model to discover groups of similar customers based on finding the smallest variations among customers within each group.

k-means cluster analysis is a common cluster analysis method used in customer segmentation.

Since the dataset is limited to the sales records, and does not include any other information about our customers, I used a RFM,*Recency, Frequency and Monetary Value, based model of customer value for finding customer segments.

The following techniques were used to identify the optimal number of clusters.
* Elbow method
* Gap Statistic
* Silhouette Coefficient

The best value for number of clusters from these methods was 3.


## Conclusion

Discovery and the quality of clustering can be improved by adding other customer information and purchase details in this dataset.
For example:
* New indicators, such as customer relationship time, based on the date of first purchase of the client.
* Some group or category of product to be obtained through the SKUs.

Another dimension to explore can be trying out different algorithms for performing the segmentation for instance hierarchical clustering.

# Recommendation System

Find out how we can use the collaborative filtering, i.e. the user is recommended items that people with similar tastes and preferences liked in the past. In other words, how we can predict unknown ratings by using the similarities between users.

## Approach

The same UCI Machine Learning Repository on online retail transactions was used to develop recommendation system algorithms, with the Surprise library. 

Surprise package has been specially developed to make recommendation based on collaborative filtering easy and has default implementation for a variety of CF algorithms.

Surprise requires the data frame to  have three columns, corresponding to the user ids, the item ids, and the ratings in this order. Each row thus corresponds to a given rating.

The transaction dataset did  not have any ratings and had to be built based on the number of times an item was ordered by a user.

## Conclusion

Surprise makes it easy to implement neighborhood and Similarity based recommendation algorithms. There are more sophisticated algorithms based on deep learning that can be used.

Apart from KNN based there are also other types of algorithms like matrix factorization based algorithms that are supported by surprise package for collaborative filtering.

# Market Basket Analysis

Market basket analysis is a set of calculations meant to help businesses understand the underlying patterns in their sales. 
The sales of certain goods are complementary, they are often bought together and Apriori Algorithm can uncover them. 


## Approach

Used Apriori an association Rule-based algorithm and generated:

Frequent Itemset Generation: All frequent itemsets with support >= predetermined min_support count.

Rule Generation: Listed all Association Rules from frequent itemsets. Calculated support and Confidence for all rules. Pruned the rules that fail min_support and min_confidence thresholds.









