# Segmentation model using K means clustering

## 1. Purpose 

The purpose of this model is to be able for a company to seperate their customers into segments based on historical data. These groups will connect demographic and online behaviour/activity with spending habits allowing a company to offer a customer a tailored value proposition/ product selection based on the demographic/ behavioural aspects observed ,increasing the expected conversion of leads. The selection of variables will be based on Recency, Frequency and Monetary values which have been proven to be powerful characteristics for segmenting based on [customer behaviour and value](https://www.researchgate.net/publication/392017535_Using_RFM_Analysis_to_Predict_High-_Value_Customers).   

## 2. Detailing the environment/ Loading the data

https://www.kaggle.com/datasets/vishakhdapat/customer-segmentation-clustering?resource=download

The data used is artificial customer data for a grocery store. It has both physical and online data. The initial data set contained 2240 data points. After cleaning and formating the data there were 2211 customer profile records, with customers who had intially used the service from 2012-07 to 2014-06.The customers average age group is 45 with an average income of $52,232.51.  

## 3. Data Columns and Explorations



![Column](./images/column_names.png)

![Column](./images/gen_metrics.png)

![Age Distribution](./images/Age_Distribution.png)

![Income Distribution](./images/dist_income.png)

![Education](./images/education.png)

# 4. Feature Engineering

Created total children variables

Created total spending for variable by summing up all product expenditure

Created total campaign responses from all campaigns

![Features](./images/feat_df.png)

# Correlation Matrix

![Correlation Matrix](./images/Corr_matrix.png)

# K means algorithm
Analysing the elbow diagram we can tell that 2 clusters will allow for the smallest sum of squares on average per cluster. Allowing for most well defined groupings for the dataset.

![K means elbow](./images/K_means.png)

# Clustering

![Segmentation](./images/seg_image.png)

# Summary of the Cluster Characteristics 

The clustering analysis reveals a clear segmentation within the customer base. Customers in Cluster 0 represent a high-value segment, with nearly double the average income and approximately 250% higher purchasing volume compared to the other cluster. This group tends to be slightly older and has fewer children, with roughly half the number of dependents.

From a behavioural perspective, these customers show a stronger preference for catalogue-based shopping, with around 25% engaging through this channel compared to only .1% in the other cluster. They are also significantly less deal-driven, with only .1% purchasing through promotions versus 34% in the lower-value segment. Additionally, they are three times more likely to respond to marketing campaigns, indicating higher engagement and brand responsiveness.

In contrast, the second cluster consists of more price-conscious shoppers with lower income and overall spending levels. These customers demonstrate higher online browsing activity, with nearly twice as many web visits as the high-value segment, yet they convert less efficiently, generating only around half the number of web purchases. This suggests greater comparison shopping behaviour and stronger price sensitivity.

![Summary of Clusters](./images/cluster_sum.png)

# Recommendations


1. Catalogue Optimisation

Adjust the catalogue mix to feature a higher proportion of premium and higher-margin products, supported by fewer discount-driven offers. This aligns with the preferences of Cluster 0 customers, who demonstrate higher purchasing power, lower price sensitivity, and a stronger preference for catalogue-based shopping.

2. Targeted Discount Strategy

Deploy targeted promotional campaigns toward Cluster 1 customers to stimulate purchase frequency and conversion. As this segment displays greater price sensitivity and higher deal engagement, personalised discounts and promotional offers are likely to drive incremental sales and improve overall conversion rates.

3. Segmented Marketing Messaging

Develop differentiated marketing messaging across clusters. For Cluster 1, emphasise value, affordability, and family-oriented product offerings to better align with their demographic and purchasing behaviour. In contrast, messaging for Cluster 0 should highlight product quality, exclusivity, and convenience to reinforce their premium purchasing tendencies.
