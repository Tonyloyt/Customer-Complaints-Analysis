# Customer Complaints Analysis

This project aims to predict customer complaints based on transaction history data. The goal is to identify customers who are more likely to complain and proactively address their concerns, ultimately reducing the number of complaints and improving overall customer satisfaction.

## Problem Statement

Customers of our store have been complaining regularly on social media posts. To address this issue, we have decided to start a campaign to call customers who are more likely to complain. The objective is to collect their opinions and feedback on how we can serve them better. Using the transaction history data from the last 30 days, we need to develop a machine learning model to predict whether a customer will complain by the end of the month or not.

## Dataset

The dataset used for this project contains transaction history data with the following columns:

- `customer_registration_number`: Registration number of the customer
- `merchandize_category`: Category of the merchandise
- `amount_deposited_via_counter`: Amount deposited via counter
- `amount_deposited_via_card`: Amount deposited via card
- `balance_on_complaint_date`: Balance on the complaint date
- `transaction_date`: Date of the transaction
- `complaint_date`: Date of the complaint
- `restaurant_points`: Points earned from restaurant transactions
- `fuel_points`: Points earned from fuel transactions
- `groceries_points`: Points earned from groceries transactions
- `toys_points`: Points earned from toys transactions
- `cash_back_points`: Points earned from cash back
- `electronics`: Points earned from electronics purchases
- `complained`: Binary variable indicating if the customer has complained (1) or not (0)
- `Order_tyPe`: Type of the order
- `amount`: Amount of the transaction
- `quantity`: Quantity of the product
- `card_vendor`: Vendor of the card used for the transaction
- `used_coupon`: Indicator if a coupon was used for the transaction
- `product_discounted`: Indicator if the product was discounted
- `cust_age`: Age of the customer
- `cust_gender`: Gender of the customer

## Approach

The project follows the following approach:

1. **Exploratory Data Analysis (EDA)**: Perform exploratory data analysis to understand the data, identify patterns, and gain insights into customer behavior and complaint trends.

2. **Data Preprocessing**: Handle missing values, perform feature engineering, and encode categorical variables to prepare the data for model training.

3. **Feature Selection**: Select relevant features based on their significance in predicting customer complaints. Use statistical tests or domain knowledge to identify the most important features.

4. **Model Training**: Train a machine learning model using the labeled data to predict the likelihood of customer complaints. Evaluate multiple models such as Logistic Regression, Random Forest, LightGBM, and CatBoost to identify the best-performing model.

5. **Model Evaluation**: Evaluate the trained model using performance metrics such as accuracy, F1-score, area under the ROC curve (AUC), and confusion matrix. Assess the model's ability to predict customer complaints accurately.

6. **Feature Importances**: Analyze the feature importances from the trained CatBoost model to understand which features contribute the most to identifying customers with complaints. Use this information to gain insights into customer behavior and make data-driven decisions.

7. **Campaign Implementation**: Utilize the trained model to prioritize customers for the call campaign. Create a call script or outline based on the model's predictions to collect feedback and improve customer satisfaction.

8. **Monitoring and Iteration**: Continuously monitor the performance of the call campaign and customer satisfaction metrics. Iterate on the model and campaign strategies based on feedback and results to enhance the effectiveness of complaint management.

## Results

The CatBoost model outperformed other models with an

 accuracy of XX%, F1-score of XX%, and AUC of XX%. The confusion matrix for the model is as follows:

```
[[1831  738]
 [ 379 3437]]
```

The AUC score of 0.876 indicates that the model has good discriminatory power in distinguishing between customers who will complain and those who will not.

## Conclusion

Based on the analysis and model results, we can draw the following conclusions:

- The CatBoost model trained on transaction history data can accurately predict whether a customer is likely to complain.
- Features such as balance on the complaint date, transaction amount, customer age, and product discounts have a significant impact on identifying customers with complaints.
- The call campaign can be targeted towards customers with a higher likelihood of complaining, as determined by the model predictions.
- Regular monitoring and evaluation of the campaign, along with continuous model updates, will help in improving customer satisfaction and reducing the number of complaints.

## Recommendations

Based on the findings of this project, the following recommendations are suggested:

1. Improve data collection: Collect more detailed data related to customer interactions, preferences, and feedback to enhance the model's predictive power.

2. Explore additional features: Experiment with generating new features based on the existing data to capture more information about customer behavior and preferences.

3. Incorporate external data sources: Consider integrating external data sources such as demographic data or social media sentiment analysis to augment the existing transaction history data.

4. Regular model retraining: Retrain the model periodically using the latest transaction data to ensure its accuracy and effectiveness in predicting customer complaints.

5. Collaborate with customer service: Establish a feedback loop with the customer service team to gather insights from direct customer interactions and incorporate them into the complaint management strategy.

6. Continuously monitor and evaluate: Track the performance of the call campaign and customer satisfaction metrics over time. Make necessary adjustments to optimize the campaign's effectiveness.

7. Foster a customer-centric culture: Promote a customer-centric mindset throughout the organization, emphasizing the importance of customer satisfaction and complaint resolution.

By implementing these recommendations, the organization can improve its customer complaint management process, enhance customer satisfaction, and build long-term customer loyalty.
