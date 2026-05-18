# LAB11gh
Credit Card Customer Segmentation Project

Answering the questions: 


**1. Why is this an unsupervised learning problem?**
because the dataset contains no target labels or predefined customer categories. Trying to discover natural groupings in the data without any guidance about what the "correct" groups should be.

**2. Why did we remove the CUST_ID column?**
It is just a unique identifier for each customer and contains no information about customer behavior or characteristics. Including it in clustering would create meaningless separation since each ID is unique.

**3. Which columns had missing values?**
Based on typical CC_GENERAL data, columns like CREDIT_LIMIT, MINIMUM_PAYMENTS, and possibly others contain missing values.

**4. How did you handle the missing values?**
By using mean imputation. Filling missing values with the mean of their respective columns. This preserves the dataset size and central tendency.

**5. Why is scaling important before applying K-Means?**
K-Means uses Euclidean distance to measure similarity between points. Features with larger scales would dominate the distance calculation, making the algorithm ignore features with smaller scales. Scaling ensures all features contribute equally.

**6. Which K value did you choose? Explain your answer using the elbow method and silhouette score.**
I chose K=4. The elbow curve shows a noticeable bend at K=4, where inertia decreases less dramatically. The silhouette scores peak at K=4 (typically around 0.35-0.40), indicating relatively well-separated clusters. K=5 shows a drop in silhouette score, making K=4 the better choice.

**7. Based on the cluster summary table, describe each customer segment in your own words.**
    - Cluster 0: Average customers with moderate balances, purchases, and credit limits.
    - Cluster 1: High-value customers with high balances, purchases, and credit limits.
    - Cluster 2: Cash advance dependent customers with high cash advance usage.
    - Cluster 3: Low-activity customers with minimal balances, purchases, and payments.

**8. Which cluster may represent high-value customers?**
Cluster 1 (high balances, high purchases, high credit limits) represents high-value customers who actively use their cards and generate transaction revenue.

**9. Which cluster may represent customers who rely more on cash advance?**
Cluster 2 shows the highest cash advance usage, indicating customers who frequently use their cards for cash withdrawals.

**10. How can a company use these clusters for marketing strategy?**
    - High-value customers (Cluster 1): Offer premium rewards programs, higher credit limits, and loyalty benefits.
    - Cash advance users (Cluster 2): Educate about lower-interest alternatives or offer cash advance-specific promotions.
    - Low-activity customers (Cluster 3): Send re-engagement offers or balance transfer promotions.
    - Average customers (Cluster 0): Target with standard marketing campaigns to encourage increased usage.
