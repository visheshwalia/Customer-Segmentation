# Customer-Segmentation

Cluster Analysis for Credit Card Customer Segmentation:

In this analysis, we aimed to segment credit card customers into distinct clusters based on their financial behavior. The following key steps were performed:

**Data Import and Preprocessing:**
- We imported the necessary libraries and read the credit card customer data from a CSV file.
- Basic data exploration was conducted to understand the dataset's structure.

**Feature Engineering:**
- Several new columns were created to derive meaningful insights:
    - `monthly_avg_purchases`: Average monthly purchases by customers.
    - `monthly_cash_advance`: Average monthly cash advances by customers.
    - `limit_usage`: Ratio of balance to credit limit.
    - `purchase_type`: A categorical column indicating the type of purchases made by customers (None, One-off, Installment, or Both).

**Outlier Treatment:**
- Outliers in numeric columns were capped at 5th and 95th percentiles to reduce the impact of extreme values.

**Data Encoding:**
- Label encoding was applied to the categorical column `purchase_type`.

**Feature Scaling:**
- Standard scaling was performed on the dataset to ensure that all features have the same scale for accurate clustering.

**Principal Component Analysis (PCA):**
- PCA was applied to reduce the dimensionality of the dataset while retaining important information.
- The variance explained by each principal component was visualized to choose an appropriate number of components.

**Determining the Number of Clusters:**
- The "Elbow Method" was employed to identify the optimal number of clusters. Based on the within-cluster sum of squares (WCSS), it was determined that 4 clusters would be used for segmentation.

**K-Means Clustering:**
- K-Means clustering with 4 clusters was applied to the preprocessed data.
- The cluster assignments were added to the dataset as the 'Cluster' column.

**Cluster Analysis:**
- Each cluster was analyzed to understand the characteristics of customers within it.
    - **Cluster 0:** High credit limit, high purchases, high balance, and high payments, indicating regular and active users.
    - **Cluster 1:** Moderate credit limit, moderate purchases, moderate balance, and moderate payments, indicating regular users.
    - **Cluster 2:** High credit limit, low purchases, low balance, and low payments, indicating low usage customers.
    - **Cluster 3:** High credit limit, low purchases, high balance, and high payments, indicating infrequent but high-value users.

**Strategy for Customer Segmentation:**
- **Cluster 0:** These customers are already active and have high credit limits. No specific intervention is needed.
- **Cluster 1:** These customers are frequent users but have a moderate credit limit. Consider increasing their credit limit to encourage more spending.
- **Cluster 2:** These customers have high credit limits but rarely use their cards. They may not be potential customers for additional services.
- **Cluster 3:** These customers have high credit limits but infrequently use their cards for high-value transactions. Consider offering incentives to increase their spending frequency.

In summary, the clustering analysis allows the credit card company to tailor marketing and service strategies for different customer segments, ensuring a more targeted and effective approach to customer engagement and retention.
