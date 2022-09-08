# Retail Customer Segmentation

![cs](https://user-images.githubusercontent.com/103363862/189126809-56f2433d-4eb9-4a51-a9c6-4d988b7b9e59.png)

ABSTRACT:	
Customer segmentation is the process by which you divide your customers into segments up based on common characteristics – such as demographics or behaviors, so you can market to those customers more effectively. These customer segmentation groups can also be used to begin discussions of building a marketing persona. we have to divide customers in appropriate segments in this project.


![problem](https://user-images.githubusercontent.com/103363862/189127153-eec195d7-1c32-4bfd-ba9c-1af4eb58a092.png)

PROBLEM STATEMENT:

Target Customers for various marketing campaign, provide information about new lunch products by estimating the buying capacity of customers.

The main goal of the project is to:

Creating group of customers having similar properties and targeting various segmentes of customers for various product.

To build a string relationship with customers which are most valuable for the store.

To convert irregular customers into regular by offering good deals.



Introduction :
Businesses all over the world are growing every day. With the help of technology, they have access to a wider market and hence, a large customer base. 
Customer segmentation refers to categorizing customers into different groups with similar characteristics.
Customer segmentation can help businesses focus on each customer group in a different way, in order to maximize benefits for customers as well as the business
This project mainly deals in segmenting customers of an online business store in the UK.



Factors Affecting :
Following are the factors affecting to segment customers:

Invoice No : Number uniquely assigned to each transaction. If this code starts with letter 'c', it indat-es a cancellation
StockCode: Product (item) code 5digit integral number uniquely assigned to each distinct product.
Description: Product (item) name. Nominal.
Quantity: The quantities of each product (item) per transaction. Numeric.
Invoice Date: Invoice Date and time. Numeric, the day and time when each transaction was generated.
Unit Price: Unit price. Numeric, Product price per unit in sterling.
CustomerID: Customer number. Nominal, a 5-digit integral number uniquely assigned to each customer.
Country: Country name. Nominal, the name of the country where each customer resides.
Data-set description

0   Invoice No                 object 
 1  Stock Code                object 
 2  Description               object 
 3   Quantity                   int64  
 4   Invoice Date            object 
 5   Unit Price                 float64
 6   Customer ID            float64
 7   Country                    object
Steps involved :

![rfm](https://user-images.githubusercontent.com/103363862/189128901-1ad57cd4-29ad-4afd-9b29-0342c4400e81.jpg)

Handling null values – Data contains lots of null values we have to drop all those null values because we don’t have any strategical intuition to handling those values all canceled order values are also dropped in order to perform segmentation appropriately.

Removing Outliers – We removed outliers which are present in quantity and Unit price in order to group customers appropriately.

Feature Extraction – We Extract features from Invoice Date that is day , days name , week , quarter and years which will be very helpful for exploratory data analysis.

Exploratory Data Analysis – We Explore data and built some meaningful insights such as top 10 most selling items .top 10 most potential customers , Sales generated per year , per month , per quarter ,per day name.

RFM Modeling – We extract feature like Recency , Frequency and Monetory and delvelop RFM score with respect to each customer and cluster customer by using these RFM score we group customers in three segments Diamond, Platinum and  Gold . From these we can conclude that Diamond customers are most valuable customers for store after that platinum customers are more important and gold customers are least important as compare two those two.

Implimention K-Means Clustering- We  have chosen K_means clustering algorithm to cluster all these customers into 3 segments  also we use elbow method , Silhouette score and Dedogram to estimate appropriate value of number of customers.
Dimensionality’s Reduction – We have reduce dimensions and convert it into two dimensions in order to visualize clusters properly.

![steps involved](https://user-images.githubusercontent.com/103363862/189127558-96967164-20af-4a7e-802c-e5ac31861328.jpg)

ALGORITHMS: 
KMeans -
k-means clustering is a method of vector quantization, originally from signal processing, that aims to partition n observations into k clusters in which each observation belongs to the cluster with the nearest mean (cluster centers or cluster centroid), serving as a prototype of the cluster. This results in a partitioning of the data space into Voronoi cells. k-means clustering minimizes within-cluster variances (squared Euclidean distances), but not regular Euclidean distances, which would be the more difficult Weber problem: the mean optimizes squared errors, whereas only the geometric median minimizes Euclidean distances. For instance, better Euclidean solutions can be found using k-medians and k-medoids.

![k means](https://user-images.githubusercontent.com/103363862/189127784-74b4971c-fe88-4308-a117-e0f87b2c12bd.png)




Dendogram - A dendrogram is a tree diagram that is used to represent and categorize hierarchical relationships among objects. 


The picture is an output from the illustration of hierarchical clustering. The name comprises clades (branches) that are further integrated into smaller branches. Individual elements are placed at the lower level, grouped according to the attributes, and placed at higher levels. The end of each chapter (also called leaf) is the data.

![dendogram](https://user-images.githubusercontent.com/103363862/189128096-8e8ae8c1-afce-4b2d-84ec-0053128b999b.png)



Silhouette Coefficient:
Silhouette Coefficient or silhouette score is a metric used to calculate the goodness of a clustering technique. Its value ranges from -1 to 1.
1: Means clusters are well apart from each other and clearly distinguished.
0: Means clusters are indifferent, or we can say that the distance between clusters is not significant.
-1: Means clusters are assigned in the wrong way.

![silhout score](https://user-images.githubusercontent.com/103363862/189128366-da05e9d6-cf91-48e5-b885-f342bef83593.png)


Principal Component Analysis –
Principal Component Analysis is an unsupervised learning algorithm that is used for the dimensionality reduction in machine learning. It is a statistical process that converts the observations of correlated features into a set of linearly uncorrelated features with the help of orthogonal transformation. These new transformed features are called the Principal Components. It is one of the popular tools that is used for exploratory data analysis and predictive modeling. It is a technique to draw strong patterns from the given dataset by reducing the variances.
PCA generally tries to find the lower-dimensional surface to project the high-dimensional data.
PCA works by considering the variance of each attribute because the high attribute shows the good split between the classes, and hence it reduces the dimensionality. Some real-world applications of PCA are image processing, movie recommendation system, optimizing the power allocation in various communication channels. It is a feature extraction technique, so it contains the important variables and drops the least important variable.
The PCA algorithm is based on some mathematical concepts such as:


Variance and Covariance
Eigenvalues and Eigen factors
Some common terms used in PCA algorithm:
Dimensionality: It is the number of features or variables present in the given dataset. More easily, it is the number of columns present in the dataset.
Correlation: It signifies that how strongly two variables are related to each other. Such as if one changes, the other variable also gets changed. The correlation value ranges from -1 to +1. Here, -1 occurs if variables are inversely proportional to each other, and +1 indicates that variables are directly proportional to each other.
Orthogonal: It defines that variables are not correlated to each other, and hence the correlation between the pair of variables is zero.
Eigenvectors: If there is a square matrix M, and a non-zero vector v is given. Then v will be eigenvector if Av is the scalar multiple of v.
Covariance Matrix: A matrix containing the covariance between the pair of variables is called the Covariance Matrix.


