<div align="center">
    <h1>Streaming Services</h1>
    <h2 style="margin-top: 0;">Uncovering the Drivers of Customer Churn</h2>
</div>

<div align="center">
    <img src="https://github.com/KoBlades/Customer-Churn-Project/blob/main/Visualizations/Title%20Photo.png" alt="Customer Churn" width="600"/>
</div>

<div align="center">
    <h3><b>Team Members:</b></h3>
    <h4>
      Jonathan Tran<br>
      Megan O'Connor<br>
      Long Le<br>
      Dhwani Shah
    </h4>
</div>

---

## Project Overview
This project focuses on predicting customer churn rates for a fictitious streaming subscription service using machine learning techniques. We utilized a dataset downloaded from Kaggle, which was clean and free of duplicates and missing values.

## Data Sources

**Kaggle**
[Predictive Analytics for Customer Churn: Dataset](https://www.kaggle.com/datasets/safrin03/predictive-analytics-for-customer-churn-dataset)


## Data Preparation
We began by thoroughly cleaning the dataset to ensure its integrity. This included checking for and removing any duplicate entries, as well as confirming the absence of missing values. The dataset was largely clear cut, which facilitated our analysis.

## Visualizations and Insights
To complement our predictive models, we created several visualizations that help illustrate key insights regarding churn rates. Our analysis revealed two main factors affecting churn:

### Customer Churn Distribution 
A clear overview of the churn rate within our dataset. The visualization reveals that the majority of customers remain subscribed, with only a small portion choosing to churn. This imbalance indicates that while most customers are retained, there is a significant enough churn segment to warrant targeted retention strategies. The churn segment represents valuable insights into behaviors and characteristics that lead to churn, guiding our predictive modeling and retention efforts.

<div align="center">
    <img src="https://github.com/KoBlades/Customer-Churn-Project/blob/main/Visualizations/Graphs/Customer%20Churn%20Distribution.png" alt="ChurnRateDistribution" width="1000"/>
</div>

### 1. Support Tickets
Our visualization indicated a correlation between the number of support tickets submitted and the churn rate. Specifically, we found that when users submitted **9 support tickets**, approximately **30%** of those users had churned at some point.

<div align="center">
    <img src="https://github.com/KoBlades/Customer-Churn-Project/blob/main/Visualizations/Graphs/SupportTickets%20vs%20Churn.png" alt="SupportVsChurnRate" width="1000"/>
</div>

### 2. Account Age
Another significant finding was related to the age of the accounts. The highest churn rates occurred within the **initial period** of account creation, with **30%** of churn attributed to customers in their early account years. This suggests that customers who experience a poor first impression are more likely to leave, while those who remain tend to stay longer.

<div align="center">
    <img src="https://github.com/KoBlades/Customer-Churn-Project/blob/main/Visualizations/Graphs/Account%20Age%20vs%20Churn.png" alt="AccountAgeVsChurnRate" width="900"/>
</div>

## Machine Learning Model
We created a supervised machine learning model since our training dataset included target information. We decided to use a Logistic Regression model because it can classify the data into the binary customer categories: churn or not churn. It predicts the probability of a customer discontinuing their services by classifying a customer as churned if the probability calculated from the model is greater than 0.5.

The model identified the following as key features in predicting churn:
- the monthly subscription rate
- support tickets per month
- user rating, watchlist size
- total charges over the account lifetime

The model indicates that higher monthly subscription fees and support tickets increases the probability that a customer will churn. It also indicates that customers who have been with the service longer are less likely to churn, as indicated through the total charges feature since it takes into consideration the account lifetime.

### Model Performance
This model has an accuracy score of 82%. It has a high precision score of 1 and a lower recall score of 0.82 which is good in the context of identifying customers that are more likely to churn because we want to be sure we are identifying those that will absolutely discontinue their services.

This could allow the company time to get ahead of this by developing a more strategic plan on working with these customers before they decide to discontinue their services.

### Testing the Model
After training the model, we tested it on data that does not have the churn classification included in the dataset. 

**Account Age**
The account age distribution between customers predicted to churn and not churn were quite similar across the different membership types. Customers predicted to discontinue their services have an average account age of 6.5 months while those not predicted to churn have an average account age of 5 years. This aligns with the total charges as a key feature since customers that have been on the service longer will have a higher total charges value.

From the customers predicted to churn, it seems like a relatively similar proportion of customer are predicted to churn from each membership tier. Although 73% of those customers predicted to churn will come from customers on standard and basic membership plans.

<div align="center">
    <img src="https://github.com/KoBlades/Customer-Churn-Project/blob/main/Visualizations/Graphs/AgeBySubBoxPlot.png" alt="BPofAgeBySubType" width="900"/>
</div>

**Support Tickets Per Month**
From the graph, we can see that the average number of tickets sent each month is higher for customer predicted to churn. The average number of tickets sent by customers predicted to discontinue their services is up at 8 tickets while those not predicted to churn are sending just over 4 tickets a month on average.

After performing a one-way ANOVA, we concluded that there is a statistically significant difference between the average number of support tickets sent per month between customers predicted to churn and not churn.

Regardless, it seems like a relatively high number tickets are being sent to support. Additional analysis on the tickets being sent should be conducted.

<div align="center">
    <img src="https://github.com/KoBlades/Customer-Churn-Project/blob/main/Visualizations/Graphs/MonthlySubChargeBP.png" alt="MonthlySubCharge" width="900"/>
</div>

**Monthly Subscription Fees**
Looking at the subscription fees, customers that are predicted to churn have a higher average monthly fee at $18.25, while those predicted not to churn have a lower average fee of $11.94. And after performing a one-way ANOVA, we concluded that there is a statistically significant difference between these average monthly subscription fees.

More information or exploration is needed on the price changes over time to understand why the gap between the average monthly fee is significantly different between the two groups.


## Recommendations
Based on our findings, we propose the following strategies to reduce churn rates:

- **Discounted Pricing for New Customers:** Implement discounted prices for customers during their first year or two of service. This strategy aims to improve first impressions and encourage retention.

- **Enhanced Customer Service:** Identify and prioritize top-performing customer service specialists for support tickets of **5 or higher**. While visualizing the impact of this approach on profit may be challenging, the theoretical benefits in customer satisfaction and retention could be substantial.

- **Contract Based Subscription:** Having subscriptions that include a one year contract to push users deeper into their account age. This will allow a longer retention of these accounts over the year.  

## Future Work
To visualize the total loss from churn versus overall profit would be beneficial, as it would provide a clearer picture of the financial implications of customer retention strategies.
