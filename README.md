# Retail Customer Segmentation

![segmentation](https://user-images.githubusercontent.com/103363862/189271251-aa827de8-3aee-4a3d-9b07-5e6016485fe4.jpeg)

ABSTRACT:	
Customer segmentation is the process by which you divide your customers into segments up based on common characteristics – such as demographics or behaviors, so you can market to those customers more effectively. 

These customer segmentation groups can also be used to begin discussions of building a marketing persona. we have to divide customers in appropriate segments in this project.



# PROBLEM STATEMENT:

![problem](https://user-images.githubusercontent.com/103363862/189127153-eec195d7-1c32-4bfd-ba9c-1af4eb58a092.png)

Target Customers for various marketing campaign, provide information about new lunch products by estimating the buying capacity of customers.

The main goal of the project is to:

Creating group of customers having similar properties and targeting various segmentes of customers for various product.

To build a string relationship with customers which are most valuable for the store.

To convert irregular customers into regular by offering good deals.



# Introduction :
Businesses all over the world are growing every day. With the help of technology, they have access to a wider market and hence, a large customer base. 

Customer segmentation refers to categorizing customers into different groups with similar characteristics.

Customer segmentation can help businesses focus on each customer group in a different way, in order to maximize benefits for customers as well as the business

This project mainly deals in segmenting customers of an online business store in the UK.



# Data Description 

Invoice No : Number uniquely assigned to each transaction. If this code starts with letter 'c', it indat-es a cancellation

StockCode: Product (item) code 5digit integral number uniquely assigned to each distinct product.

Description: Product (item) name. Nominal.

Quantity: The quantities of each product (item) per transaction. Numeric.

Invoice Date: Invoice Date and time. Numeric, the day and time when each transaction was generated.

Unit Price: Unit price. Numeric, Product price per unit in sterling.

CustomerID: Customer number. Nominal, a 5-digit integral number uniquely assigned to each customer.

Country: Country name. Nominal, the name of the country where each customer resides.


# Steps involved

![steps involved](https://user-images.githubusercontent.com/103363862/189127558-96967164-20af-4a7e-802c-e5ac31861328.jpg)




Handling null values – Data contains lots of null values we have to drop all those null values because we don’t have any strategical intuition to handling those values all canceled order values are also dropped in order to perform segmentation appropriately.


Removing Outliers – We removed outliers which are present in quantity and Unit price in order to group customers appropriately.


Feature Extraction – We Extract features from Invoice Date that is day , days name , week , quarter and years which will be very helpful for exploratory data analysis.


Exploratory Data Analysis – We Explore data and built some meaningful insights such as top 10 most selling items .top 10 most potential customers , Sales generated per year , per month , per quarter ,per day name.


RFM Modeling – We extract feature like Recency , Frequency and Monetory and delvelop RFM score with respect to each customer and cluster customer by using these RFM score we group customers in three segments Diamond, Platinum and  Gold . 

From these we can conclude that Diamond customers are most valuable customers for store after that platinum customers are more important and gold customers are least important as compare two those two.


Implimention K-Means Clustering- We  have chosen K_means clustering algorithm to cluster all these customers into 3 segments  also we use elbow method , Silhouette score and Dedogram to estimate appropriate value of number of customers.

# Data Cleaning

![dc 1](https://user-images.githubusercontent.com/103363862/189263901-cd0984f6-30e3-4150-8244-7212331aa8a8.jpg)

In this step, the main focus will be to handle the null values and other errors in the data. Columns that are not required will also be dropped.

There are 1454 null values in the description column. There are 4223 different products in the dataset. It is not possible to fill the null values in a strategical manner. Hence, we will drop the null values of the description column.

There are 4372 unique customers in the dataset, there are also 133626 null values in the column. There is no particular method to fill these huge number of points. We cannot use median, mean or mode to fill these values. It is close to impossible that one customer ID can fill 133626 rows. Hence, we will drop the rows containing null values.

Before handling null values data contains 541909 but after dropping null values present in 2 columns which are description and customer id now data contains 406829 records.

Unfortunately 135080 Records have been lost in the process.

As customer ID is a 5 digit number, we can convert it from a float type to an integer type.

# Feature Engineering


Extraction some fetures from Invoice date column such as day , month , year ,day_name ,Quarter ,Hour and week 


these column would be very important to generate some meaningfull insights from the data.


# Exploratory Data Analysis

![eda 2](https://user-images.githubusercontent.com/103363862/189264711-e220b654-d996-49cb-8766-ca5efd03bf45.png)

# Top 10 most repeatedly sold items And generated highest revenue

WHITE HANGING HEART T-LIGHT HOLDER is the most reapetedly sold items. Hence company should generate stratergies to increase the supply of all those 10 most frequently sold items.

From the above barplot we can clearly seen that top 10 most frequent customer hence company need to maintain good relationship with that customers

From the above bar plot these are the customers who has bought more products also boughts in a mass valume soo those customers are likely to be wholesellers or distributors.

Because that compant should provide more discounts to those customers also provide grete deals in order to make more profit from that customers.


Countries that were sold different items the most

From the above bar plot we can clealy seen that most of the itema has been sold in united kingdom.

Because of that company need to perform marketing campaign in united kingdom in order to expand there business in that company.


From the above bar plot we can see that most items has been sold in the 2011.

From the above bar plot we can clearly seen that the most revenue generate by the company is 8338694 in the year of 2011.

from the above bar plot we can clearly seen that in the month of seprtember,octomber and november most number of fromduct has been sold .

Hence company needs to provide more discounts and offers on there product to generate more revenue in that months.

Now in the months of december,january and february least items are sold therefore company needs to develop strategies and plan to seel more product in that months.

From the barplot we can clearly seen that in the month of novermber ,september and octomeber company made more revenue than other month.

There is a possibility that in those three months more number of special events and feativals are occured beacause of that most number of product are bought by the customer and revenue made by the company is at the most.

In the month of january customer had not bought items frequently but in this bar plot company generate better revenue in these month this could be done because customer bought very expensive items in january month.

from the above bar plot we can clearly seen that in the 'Afternoon' time slot most number of customer like to bought items because of the in this time slot most number of iteams has been sold and company able to generate most of the revenue in that time slot.

hence for that company needs to provide more man power in that time slot to sell items to there customers and provide customer satisfaction also provide some gift vouchers to the customer who bought there products in this time slot to gnerate more revenue in that time slot.

From the above bar plot we can clearly seen that when theweek day is Thuursday , Tuesday and Monday most number of customer prefers to bought items beacause of that most number of sales are generated in those 3 days.

company needs to apply some startegies to generate more and more revenue in these days.

from the above bar plot we can see that as the quarter increases customer prefers to bought more items.

At the end of the year most number of product has been bought by the customers.

But company generate high sales in quarter 3 soo we can estimate that most of the distributor and retailers bought items in huge quatity in the quarter 3 to supply the items to their customer for quarter 4.

From the above statement we can conclude that company recuire to maintain supply in quarter 3 beacause most of the retailers and distributor bought items in quarter 3.

Quarter 3 have to be very important for company to made profit in whole year.

# Co-relation

![rfm co](https://user-images.githubusercontent.com/103363862/189266477-37133cc9-c212-4ebc-befb-1b124554572b.png)



From the above co-relation plot we can see that most of the features are highly co-relation but we require only few features to cluster our customers.

so we can ignore this co-relation matrix.


# RFM MOdeling

![fresh](https://user-images.githubusercontent.com/103363862/189270918-529f9551-fe26-4c84-b175-409d80f3117e.png)

# Conclusion
From the above RFM customer segmentation we can cluster customers into 3 categories according to there RFM score. we can build customers segmentation into gold,platinum and diamond class.

![rfm table](https://user-images.githubusercontent.com/103363862/189267164-1aa4a785-9eed-4d7c-b5a9-3886f38f4728.png)

# Diamond Class
The customers which have a RFM score greater than equal to 10 and till the end(in these scenario maximum RFM score is 12) those customers are belog to Diamond Category.

Those customers are the most important customers for the company with respect to sales.

Company should target those customers to sell expensive iteams and aware that customers when company launches new products.

Also company requires to develop marketing campeign add target these customer at first priority.

Those customers and more likely distributors who distribute there products in all the area in there limit so company require to offer these categories of customer a huge discounts when they buy items in huge quantity.

# Platinum class
The customers which have a RFM score greater than equal to 8 and less than equal to 10 those customers are belog to platinum Category.

Those customer are second most important customers to generate sales for the company.

Company should target those customers to expensive products and midium expensive products.

also company should maintain good relationship with these costomers category stay in contact with these customers regularly.

There is a possibility that these customers are retailers who boughts a items in huge amount sp these customer categories are important categories to generate sales for the company.

# Gold Class
The customers which have a RFM score less than 8 all these customer are belong to category gold class.

Most number of customer are belong to these class .

These are the regular customers of company but these customers are not bought items in huge frequency.

Company dont need to target these customer for expensive product.

Also when company launch a marketing campaign. No need to target these customer at the level of Diamond and Platinum class customers.


# Applying Clustering Algorithems to segment customers.

Applied Unsupervised learing Algorithems to segment customers.

# Data Preprocessing

Applied stadernd Scalor to Standerdzed all values to perform machine learning algorithem effectively.



Created  function to handle zero and negative values to avoid infinite numbers during log tranformation


# VISUALIZING RELATION BETWEEN RECENCY , FREQUENCY AND MONETORY IN 3D AXIS

![3dd](https://user-images.githubusercontent.com/103363862/189268711-0baaed8a-210a-4d18-9dda-f686951e7a6e.png)





# K-Means Clustering.

k-means clustering is a method of vector quantization, originally from signal processing, that aims to partition n observations into k clusters in which each observation belongs to the cluster with the nearest mean (cluster centers or cluster centroid), serving as a prototype of the cluster. 




This results in a partitioning of the data space into Voronoi cells. k-means clustering minimizes within-cluster variances (squared Euclidean distances), but not regular Euclidean distances, which would be the more difficult Weber problem: the mean optimizes squared errors, whereas only the geometric median minimizes Euclidean distances. For instance, better Euclidean solutions can be found using k-medians and k-medoids.

# Applying elbow method to identify number of clusters.

![elbow](https://user-images.githubusercontent.com/103363862/189269008-cb6c929e-7588-45ec-a25d-67da9aa6b97d.png)

From the above elbow curve we can see that if the number of clusters is 2 then we get lower within cluster sum of sqaured of error but also when the number of cluster is 3 then we can say that wcss value will flatten.

soo we are applying both number of cluster and see the results.

# K-means with 3 clusters
By applyint k-means and number of clusters 3 the cluster formation have done very well by kmeans.

Now we have to clarify is 3 clusters are perfects for these dataset for taht we are apllylying silhouette score.

# Silhouette Coefficient:

![sil](https://user-images.githubusercontent.com/103363862/189269707-c03ecf85-8ce4-41fe-a253-09db17af7935.png)


Silhouette score is 0.52 when we form 3 number of cluster it is better as compared to all number of cluster values.


# Dendogram

A dendrogram is a tree diagram that is used to represent and categorize hierarchical relationships among objects. 


The picture is an output from the illustration of hierarchical clustering. The name comprises clades (branches) that are further integrated into smaller branches. Individual elements are placed at the lower level, grouped according to the attributes, and placed at higher levels. The end of each chapter (also called leaf) is the data.

![den](https://user-images.githubusercontent.com/103363862/189269842-99b1d00e-6bad-4364-b217-76c303ce1d22.png)


By applying dendogram we can also visualize that 3 clustors and suitable for these dataset.


# Applying K_means clustering

By grouping RFM dataframe on the basis of clusters, and using K-mean to summarize the variables we understand that :-
Diamond Customers - Cluster 2
These are the most valuable customers for the company.These customers are very Recent also bought items very frequently and these customers bought items in a mass valume.

So company need to maitain good relationship with these customers they have to offer discounts and better deals to that customer so that company able to generate more sales from that customer.

This customers are more likely to be wholesellers or distributors.

Also when company develop any marketing campaign these customers should be the first priority of the company.

Platinum Customers - Cluster 1
These customers segment is more recent after diamond cluster also they bought more items in in bulk valume .

These customer are second most important customer for company after diamond customers.

Also company have to bilt strategy to convert these customers into Diamond Customers.

Gold Customers - Cluster 0
These customers are not reguar customers of company also these customers does not bought items very frequently and they do not bought items in bulk valume.

So company give less priority to this customers.

Also company built strategy to convert these customer in Platinum customers.

# Applying Principal Component Analysis to visualize Clustures.

Principal Component Analysis is an unsupervised learning algorithm that is used for the dimensionality reduction in machine learning. It is a statistical process that converts the observations of correlated features into a set of linearly uncorrelated features with the help of orthogonal transformation. 

These new transformed features are called the Principal Components. It is one of the popular tools that is used for exploratory data analysis and predictive modeling. It is a technique to draw strong patterns from the given dataset by reducing the variances.

PCA generally tries to find the lower-dimensional surface to project the high-dimensional data.

PCA works by considering the variance of each attribute because the high attribute shows the good split between the classes, and hence it reduces the dimensionality. Some real-world applications of PCA are image processing, movie recommendation system, optimizing the power allocation in various communication channels. 

It is a feature extraction technique, so it contains the important variables and drops the least important variable.

![pca](https://user-images.githubusercontent.com/103363862/189270648-3c411d7e-de2c-4f9c-8c84-f97090637474.png)


By visualizing K_means cluster we can clearly seen that it performs very well job.


the clustor centrods are at long distance and there are are some outlier but it is not affection to form cluster in that case.

# Conclusion
We appliend customer segmentation by using two technique firstly we group customers into three segment using RFM score by these we can get mmost valuable person and prioterise them accordind to there RFM score. This technique is very helpful for marketing cmpaign and also to traget customers for some of the specific products.

After that we have choosen k_means clastering divide clusteres into three segments K_means clusters works very well in these scenario it does noy affected by the outliers and also it forms clusters in very appropiate way . Also we use some techniques to estimate the perfect number of clusters by using elbow Method,dendogram and silhouit score.

Also we use Pricipal component analysis to reduce the dimention of the dataset in order to visualise how k_means buildt clusters by visualising these we can conclude that k_means algorithems form a clusters according to the recency , frequency and monetory attributes of the customer it futher divinde it into three group and we label these group as Diamond , Platinum and gold.

Diamond class customers are most valuble customers for the store to target and to offers deals in order to generate more sales from the customer. This type are customers are typically Wholeseller,distributors.

Platinum customers are less valuable that duamond customers . stores management should build srategies for how they convert platinum customers into diamond class customers.

Gold customers are least valuable customers for the store management than Diamond and Platinum class customers.












































