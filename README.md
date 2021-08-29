## Customer segmentation and recommendation system using the Online Retail dataset

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




