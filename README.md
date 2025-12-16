# Mall Customer Segmentation 🛍️

![Python version](https://img.shields.io/badge/Python%20version-3.10%2B-lightgrey)
![Type of ML](https://img.shields.io/badge/Type%20of%20ML-Clustering%20-blue)

Badge [source](https://shields.io/)
<img src="https://www.cleartouch.in/wp-content/uploads/2023/02/Customer-Segmentation.png" width="1100">

The objective of this study is to utilize Machine Learning methods to perform customer segmentation. Customer segmentation involves dividing a market into distinct groups of customers who exhibit similar characteristics. By leveraging customer segmentation, companies can effectively identify and address unmet customer needs, gaining a competitive edge through the development of highly appealing products and services.

## Repository structure

Thank you for confirming. This is the most common indicator that the images are still being fetched directly from the original author's repository, even though you have corrected the links in your local README.md file.

The full URL used to load an image on a GitHub README often contains the username and the time the image was last updated on that source repository, which is why you see Taweilo and "2 years ago."

The previous fix (replacing absolute URLs with relative paths like Image/filename.jpg) should resolve this, but you may have missed one, or the changes weren't properly committed/pushed.

Here is the final, definitive fix and the exact steps you need to take.

Final Solution: The README.md File
You must make sure your README.md file looks exactly like this. Open your local README.md and use this copy-paste block to replace the entire content. This version has all external GitHub URLs removed.

Markdown

# Mall Customer Segmentation 🛍️

![Python version](https://img.shields.io/badge/Python%20version-3.10%2B-lightgrey)
![Type of ML](https://img.shields.io/badge/Type%20of%20ML-Clustering%20-blue)

Badge [source](https://shields.io/)
<img src="https://www.cleartouch.in/wp-content/uploads/2023/02/Customer-Segmentation.png" width="1100">

The objective of this study is to utilize Machine Learning methods to perform customer segmentation. Customer segmentation involves dividing a market into distinct groups of customers who exhibit similar characteristics. By leveraging customer segmentation, companies can effectively identify and address unmet customer needs, gaining a competitive edge through the development of highly appealing products and services.

## Repository structure 
.
├── Data_Mall_Customers.csv                <- Original dataset used for clustering.
├── Code_Mall_Customer_Segmenation.ipynb   <- Jupyter Notebook containing the Python code for data analysis and clustering.
└── Image/                                 <- Directory holding all visualizations used in the README.md and notebook.
    ├── 2.1 Original dataset.jpg           <- Snapshot of the initial dataset structure.
    ├── 2.2 Statistics.jpg                 <- Descriptive statistics of the dataset features.
    ├── 2.3 Income segmentation.jpg        <- Visualization of income distribution and segments.
    ├── 3.1 Visual inspection.jpg          <- Chart used for visual estimation of the optimal K (number of clusters).
    ├── 3.2 Elbow Method.jpg               <- Plot for the Elbow Method to determine optimal K.
    ├── 3.3 Silhouette Score.jpg           <- Plot for the Silhouette Score method to determine optimal K.
    ├── 4.1 K-means.jpg                    <- Visualization of the K-Means Clustering results.
    ├── 4.2 Hierarchical Clustering.jpg    <- Visualization of the Hierarchical Clustering results (Dendrogram).
    └── 5.1 Features of clusters.jpg       <- Analysis and visualization of the key features for the final clusters.
    
## 1. Business Understanding
Clustering, an unsupervised machine learning technique, is employed for customer segmentation. Clustering aims to discover inherent groups or clusters within data, without prior knowledge of their existence. The following highlights the advantages and disadvantages of utilizing clustering for customer segmentation.

**Advantages of clustering**:<br>

- Facilitates the identification of unexpected or unknown customer groups.
- Provides flexibility and can be applied to diverse datasets.
- Reduces the necessity for extensive expertise in understanding the relationship between customer demographics and behaviors.
- Offers quick and scalable analysis, even with large datasets.

**Disadvantages of clustering**:<br>
- Generated customer groups may lack interpretability and clarity.
- If the data does not incorporate customer behavior information, such as purchase history or service usage, the practical utilization of identified clusters might be challenging.

By considering these factors, businesses can make informed decisions when leveraging clustering techniques for customer segmentation, ensuring meaningful and actionable insights that drive strategic success.

## 2. Data Understanding 
This project is a part of the Mall Customer Segmentation Data competition held on Kaggle. Exploratory data analysis (EDA) is used to analyze and investigate data sets and summarize their main characteristics, often employing data visualization methods. The purpose is to understand data and encourage the following analytics.

* Original Dataset
<img src="Image/2.1 Original%20dataset.jpg" width="400">

| Name | Modeling Role | Measurement Level| Description|
| ---- | ------------- | ---------------- | ---------- |
| **CustomerID** | feature | int64 | Unique ID assigned to the customer |
| **Gender** | feature | Object | Gender of the customer |
| **Age** | feature| int64 | Age of the customer |
| **Annual Income (k$)** | feature | int64 | Annual Income of the customer |
| **Spending Score** | feature | int64 | Score assigned by the mall based on customer behavior and spending nature |

* Statistics
<img src="Image/2.2 Statistics.jpg" width="400">

* Income Segmentation
<img src="Image/Income%20segmentation.jpg" width="400">

## 3. Data Preparation 
### 3.1. Standardize the data: To calculate their z-score.
This is done in two steps, for each column:
1. First, subtract the mean of the data from each data point. This centers the data around 0, to make the data easier to look at and interpret, although this is not strictly required for clustering.
2. The second step is to divide the parameters by their standard deviation.

### 3.2 Different Approaches to Decide K (How many clusters)
1. Simple Visual Inspection to Choose the Optimal K
<img src="Image/3.1 Visual%20inspection.jpg" width="500"> 
2. The Elbow Method with the Sum of Squared Errors
<img src="Image/3.2 Elbow%20Method.jpg" width="500"> 
3. The Silhouette Score to Pick Optimal Number of Clusters
<img src="Image/3.3 Silhouette%20Score.jpg" width="500"> 

## 4. Modeling  
* K-means
<img src="Image/4.1 K-means.jpg" width="500"> 

* Hierarchical Clustering
<img src="Image/4.2 Hierarchical%20Clustering.jpg" width="500"> 

## 5. Evaluation
### K-means
<img src="Image/5.1 Features%20of%20clusters.jpg" width="500">
Describe each segmentation: Based on the income and Spending score, 5 clusters can be categorized as:

Cluster 0: Medium income, Midum Spending Score
Cluster 1: High Income, Low Spending Score
Cluster 2: Low Income, Low Spending Score
Cluster 3: Low Income, High Spending Score
Cluster 4: High Income, High Spending Score

## 6. Recommendation
The advantage of machine learning-based clustering is its ability to expedite the segmentation process and discover patterns without requiring extensive domain knowledge. There are various methods available for ML clustering, such as K-means, K-medians, and hierarchical clustering, each with its own strengths and limitations. In our specific case, K-means necessitates predefining the number of clusters (K), whereas hierarchical clustering can generate cluster groups based on different K values. It is crucial to compare the results of these techniques objectively.

Moreover, the choice of the number of segments (K) should align with business requirements. Fewer segments can provide a simplified and interpretable understanding of customers, while more segments allow for finer-grained customer segmentation. However, the clusters, regardless of their quality, hold no significance if they are not actionable for the business. Non-actionability can arise in two ways:

1. The clusters lack business rationale.
2. The number of clusters is excessively large.

In essence, machine learning techniques must consider business value and strategy to ensure that the insights derived are meaningful and actionable. By doing so, these insights become invaluable and can drive impactful business decisions.

## 7. Reference
- Baig, M. R., Govindan, G., & Shrimali, V. R. (2021). Data Science for Marketing Analytics: A practical guide to forming a killer marketing strategy through data analysis with Python (2nd ed.), Chapter 3: Unsupervised Learning and Customer Segmentation (pp. 113-159). Packt Publishing. 
- Sagar, A. (2019, August 24). Customer Segmentation Using K Means Clustering. https://towardsdatascience.com/customer-segmentation-using-k-means-clustering-d33964f238c3.


