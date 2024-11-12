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

**Team Members:** Megan, Dhwani, Long, Jonathan

## Project Overview
This project focuses on predicting customer churn rates for a fictitious streaming subscription service using machine learning techniques. We utilized a dataset downloaded from Kaggle, which was clean and free of duplicates and missing values.

## Data Preparation
We began by thoroughly cleaning the dataset to ensure its integrity. This included checking for and removing any duplicate entries, as well as confirming the absence of missing values. The dataset was largely clear cut, which facilitated our analysis.

## Visualizations and Insights
To complement our predictive models, we created several visualizations that help illustrate key insights regarding churn rates. Our analysis revealed two main factors affecting churn:

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

## Predictive Modeling
Our predictive model achieved an accuracy rate of **82%**. This model can help identify potential churn customers based on the analyzed features.

We also created a test set to assess how well the predictive model performs against the variables most correlated with churn. If the model performs better on this refined dataset, we can confidently assert that we've pinpointed the leading indicators of churn.

## Recommendations
Based on our findings, we propose the following strategies to reduce churn rates:

- **Discounted Pricing for New Customers:** Implement discounted prices for customers during their first year or two of service. This strategy aims to improve first impressions and encourage retention.

- **Enhanced Customer Service:** Identify and prioritize top-performing customer service specialists for support tickets of **5 or higher**. While visualizing the impact of this approach on profit may be challenging, the theoretical benefits in customer satisfaction and retention could be substantial.

## Future Work
To visualize the total loss from churn versus overall profit would be beneficial, as it would provide a clearer picture of the financial implications of customer retention strategies.
