# **E-COMMERCE CUSTOMER CHURN PREDICTION AND ANALYSIS**

# **BUSINESS PROBLEM**

## *1.1 Context*

In simple terms, customer churn occurs when customers stop using a company's products or services. Losing or transitioning customers is one of the most critical issues for any business directly selling or serving customers, such as an e-commerce business.

In this case, an e-commerce company is grappling with a churn issue where 16.8% of its customers churned in the last period. With this challenge in mind, the e-commerce company has engaged us in a project to build an accurate predictive model.

As data scientists, our task is to identify the problem, analyse data for insights, create a machine learning model with an algorithm that can predict churn and non-churn customers as accurately as possible, and provide recommendations based on our overall findings.

Here are the definitions for each label in this e-commerce context:
 
    0 = Non-churning customers (loyal customers)
    These are customers marked by relatively high numbers on their last transaction day, order quantity, and subscription duration.

    1 = Churning customers (stopped/moved)
    These customers, on the other hand, are marked by relatively low numbers on their last transaction day, order quantity, and the type of items purchased (electronic items tend to indicate churn).

## *1.2 Problem Understanding*

In fact, the percentage of lost customers significantly impacts the company's growth rate, making customer churn rate crucial, especially in e-commerce. 

Furthermore, a survey proves that:
- Acquiring new customers can cost around 5 times more than maintaining relationships with existing ones.
- The success rate in selling to existing customers is 60-70%, while the success rate in selling to new customers is 5-20%.
- Increasing customer retention by 5% boosts profits by 25-95%.

For these reasons, compared to customer acquisition, paying attention to and enhancing relationships with existing customers provides long-term benefits to the company, such as increased customer lifetime value and its impact on company profits. However, the challenge is, that if we don't know which customers will churn, we might target all customers, potentially wasting retention costs.

Sources:
[ProfitWell](https://www.profitwell.com/recur/all/customer-acquisition-vs-retention), [Huify](https://www.huify.com/blog/acquisition-vs-retention-customer-lifetime-value)


## *1.3 Problem Statement*

After understanding the background of the issue, we can summarise the problem statement for this project. There are two essential points that form our foundation: Goals and Values. Our goals align with the context explained earlier, aiming to predict customer churn as accurately as possible. The primary objective is to minimise retention costs and enhance customer lifetime value.

In this context, we will make predictions using machine learning, specifically through Supervised Learning (Binary Classification). Besides predicting customer churn, the management also hopes to identify the factors/variables influencing whether a customer churns or not. This information enables them to formulate effective strategies to reduce high churn rates.

## *1.4 Metric analysis*

Type 1 error: False Positive (predicting churn, but in reality, it's incorrect)   
Consequence: Unnecessarily incurred costs for customers who, in fact, do not churn.

Type 2 error: False Negative (predicting no churn, but in reality, it's incorrect)    
Consequence: Losing potentially loyal customers will impact CLV and business growth.

Referring to the metric evaluation above, we need to minimise the False Negative Rate (increase CLV). If the model fails to minimise the False Negative Rate (Type 2 error), it means the model predicts customers who should churn as non-churning. If this happens, the company will lose customers, affecting Customer Life Value and the company's revenue.

However, we must also pay attention to the False Positive (Type 1 error) in prediction results. If it's high, it means the model incorrectly predicts non-churning customers. This will result in wasted costs by pursuing customers predicted to churn but won't actually churn.

So, the model we are looking for is one that provides accurate predictions for the positive class with the highest possible recall value to avoid losing potentially loyal customers, followed by a Precision value that is also equally high to avoid wasting allocated costs. Thus, we must balance precision and recall for the positive class. Therefore, the main metric we will use is the **f1-score**, while still ensuring that the **recall** value is higher than **precision**. Additionally, the goal of using the f1-score is one method to address data imbalance in the positive (churn) and negative (not churn) classes.

## *1.4 Overview result*

Based on the performance of the machine learning model that has been developed, it is found that the performance of the CatBoost model is excellent, producing an F1 score of around 0.82 and a Recall of 0.97. We can conclude that if our model is used to filter the list of customers who will be our marketing target, then our model can detect 97% of customers who will churn, and our model captures 92% of customers who choose to retain/stay (all based on its recall).

Our model has a precision of 71% in predicting customers who will not churn. So, whenever our model predicts that a candidate will not churn, the likelihood of that prediction being correct is around 71%. Thus, there will still be customers who actually will not churn but are predicted as customers who will churn, around 26% of all customers who will not churn (based on recall).
