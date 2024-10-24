
# Customer Segmentation Using Machine Learning

## Project Overview
This project focuses on customer segmentation using a machine learning approach. The goal is to identify distinct customer groups based on various demographic, service usage, and behavioral variables. By segmenting customers, businesses can better target marketing efforts, personalize services, and optimize customer retention strategies.

## Dataset Description
The dataset contains information on 1000 customers with the following features:

### Features:
1. **region**: Customer’s geographic region (categorical)
2. **tenure**: Number of years the customer has been with the company
3. **age**: Customer’s age
4. **marital**: Marital status (binary, 1 = married)
5. **address**: Number of years at the current address
6. **income**: Annual income
7. **ed**: Level of education (categorical, represented by numbers)
8. **employ**: Number of years employed
9. **retire**: Retirement status (binary)
10. **gender**: Gender (binary)
11. **reside**: Number of residents in the household
12. **tollfree**: Subscription to toll-free services (binary)
13. **equip**: Equipment rental status (binary)
14. **callcard**: Subscription to calling card service (binary)
15. **wireless**: Wireless service subscription (binary)
16. **multline**: Multiple phone line subscription (binary)
17. **voice**: Subscription to voice mail (binary)
18. **pager**: Pager subscription (binary)
19. **internet**: Internet service subscription (binary)
20. **callid**: Caller ID service subscription (binary)
21. **longmon**: Average monthly long-distance charges
22. **tollmon**: Average monthly toll-free charges
23. **equipmon**: Average monthly equipment charges
24. **cardmon**: Average monthly calling card charges
25. **wiremon**: Average monthly wireless charges
26. **ebill**: E-billing subscription (binary)
27. **custcat**: Customer category (target variable)

The dataset includes 30 columns in total, including customer features and service-related data.

### Data Types:
- **int64**: Integer data types representing categorical and numerical variables.
- **float64**: Float data types for numerical variables such as monthly charges.

## Data Preprocessing
- **Missing Values**: There were no missing values in the dataset, so no imputation was required.
- **Normalization**: Continuous variables such as monthly charges and income were normalized to ensure all features were on the same scale.
- **Encoding**: Binary variables (e.g., marital status, gender, internet subscription) were already numerically encoded.

## Methodology
### Segmentation Model:
We applied the **K-Means Clustering** algorithm for segmentation. K-Means is an unsupervised learning technique that groups customers into different clusters based on their similarities in the given feature space.

### Steps:
1. **Feature Selection**: Relevant features such as tenure, age, income, service usage, and subscription data were used to cluster the customers.
2. **Scaling**: StandardScaler was used to normalize numerical features.
3. **Model Training**: The K-Means algorithm was used to create clusters, with the optimal number of clusters determined using the **Elbow Method**.

### Model Evaluation:
- The **Silhouette Score** was used to evaluate the quality of the clustering. Higher silhouette scores indicate well-defined clusters.
- Visualizations of the clusters were generated using PCA (Principal Component Analysis) to reduce dimensions.

## Results
The clustering model identified distinct customer segments, including:
- High-income, long-tenure customers with multiple service subscriptions.
- Younger, tech-savvy customers with a preference for internet services but fewer traditional phone services.
- Older customers with simpler service needs.

These segments provide insights into customer behavior, allowing for better-targeted marketing strategies and service offerings.

## Recommendations
1. **Targeted Marketing**: Different marketing strategies should be developed for each customer segment, focusing on their specific needs and preferences.
2. **Service Personalization**: Personalize offerings for high-value customers to improve retention and satisfaction.
3. **Product Bundling**: Promote product bundles to customers who are likely to subscribe to multiple services based on their current usage patterns.

## Conclusion
This project demonstrates the potential of machine learning in customer segmentation, providing actionable insights that can lead to better customer engagement and optimized marketing strategies.
