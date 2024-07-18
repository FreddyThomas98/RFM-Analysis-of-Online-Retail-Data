# RFM-Analysis-of-Online-Retail-Data
This project involves segmenting customers based on their purchasing behavior using RFM (Recency, Frequency, Monetary) analysis, aiming to optimize marketing strategies for an online retail business. The steps are:

Data Loading and Cleaning:

Loaded data from the "Online Retail.xlsx" file.
Removed cancelled orders (indicated by 'C' in InvoiceNo).
Dropped rows with missing CustomerID.
Filtered out transactions with zero or negative quantities or unit prices.
Calculated the TotalPrice for each transaction.
Feature Engineering:

Recency: Calculated the number of days since the customer's last purchase.
Frequency: Counted the number of unique purchases (invoices) for each customer.
Monetary: Summed the total spend of each customer.
Combined these metrics into a single DataFrame.
Removed outliers using the Interquartile Range (IQR) method to ensure robust analysis.
Data Scaling:

Standardized the RFM metrics using StandardScaler to prepare for clustering.
Clustering:

Used the Elbow Method to determine the optimal number of clusters based on the Sum of Squared Errors (SSE).
Applied K-Means clustering with the chosen number of clusters (3) to segment customers.
Visualization:

Created a 3D scatter plot to visualize customer segments across the RFM dimensions.
Cluster Interpretation:

Cluster 0 (At-Risk Customers): Customers who haven't purchased recently, purchase infrequently, and have low spending. These customers may need targeted re-engagement strategies.
Cluster 1 (Potential Loyalists): Customers with moderate recency, frequency, and monetary values. They purchase more frequently than at-risk customers and could be targeted for upsell and cross-sell opportunities.
Cluster 2 (Loyal Champions): Customers who have purchased very recently, purchase frequently, and spend the most. These high-value customers should be targeted for loyalty programs and personalized offers to retain and reward them.
This analysis helps in understanding customer segments and devising targeted marketing strategies to enhance customer retention and maximize revenue.







