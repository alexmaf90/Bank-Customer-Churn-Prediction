# Bank Customer Churn Prediction

This project aims to predict customer churn in a bank using machine learning models. The dataset contains various features related to customers and their banking behavior.

## Dataset Information

The dataset used for this project contains the following columns:

- RowNumber: Corresponds to the record number.
- CustomerId: Randomly generated ID for each customer.
- Surname: Surname of the customer.
- CreditScore: Credit score of the customer.
- Geography: Customer's location.
- Gender: Customer's gender.
- Age: Customer's age.
- Tenure: Number of years the customer has been with the bank.
- Balance: Account balance of the customer.
- NumOfProducts: Number of products purchased by the customer.
- HasCrCard: Indicates whether the customer has a credit card.
- IsActiveMember: Indicates whether the customer is an active member.
- EstimatedSalary: Estimated salary of the customer.
- Exited: Whether the customer left the bank (target variable).
- Satisfaction Score: Score provided by the customer for their complaint resolution.
- Card Type: Type of card held by the customer.
- Point Earned: Points earned by the customer for using a credit card.

## Data Preprocessing

- Removed irrelevant columns: RowNumber, CustomerId, Surname.
- Split the dataset into training and testing sets.
- Applied one-hot encoding to categorical variables.

## Data Visualization

During the exploratory data analysis phase, the following insights were gained:

- There is a 100% correlation between the "Complain" variable and the target variable "Exited." Therefore, the "Complain" variable was removed from the dataset.

- The age of the customer, whether the customer is an active member, and the account balance are the most correlated variables with the target variable. These variables have a significant influence on customer churn.

- When examining the continuous variables, it was observed that most of them are well balanced. However, the "EstimatedSalary" variable shows a nearly equal distribution across different salary ranges.

- Analyzing the "Balance" variable, it was found that a large number of people in the dataset do not have any money in their account. For those who do have money, the balance is relatively evenly distributed.

- Box plots for "CreditScore" and "Age" revealed the presence of outliers. However, for the current analysis, these outliers were not removed.

- When considering the categorical variables in relation to the target variable, no significant differences or patterns emerged. The distribution of values appears to be relatively consistent between positive and negative outcomes.

- It is interesting to note that older customers are more likely to leave the bank, as indicated by the analysis of the age variable.

## Machine Learning Models

The following machine learning models were used for customer churn prediction:

1. Logistic Regression:
   - Accuracy: 0.814
   - Precision: 0.560
   - Recall: 0.207
   - F1-score: 0.3025

2. Decision Tree Classifier:
   - Accuracy: 0.7897
   - Precision: 0.4628
   - Recall: 0.5
   - F1-score: 0.4807

3. Support Vector Classifier:
   - Accuracy: 0.8633
   - Precision: 0.8222
   - Recall: 0.3801
   - F1-score: 0.5199

4. Random Forest Classifier:
   - Accuracy: 0.8697
   - Precision: 0.783
   - Recall: 0.4572
   - F1-score: 0.5773

5. XGBoost Classifier:
   - Accuracy: 0.868
   - Precision: 0.7561
   - Recall: 0.4606
   - F1-score: 0.5722

## Conclusion

Conclusions
After thorough analysis and experimentation, we have gained several insights from the customer churn prediction project. Here are the key findings:

Data Visualization: Through visual exploration of the dataset, we observed that the variable "Complain" had a 100% correlation with the target variable "Exited." Therefore, we decided to remove the "Complain" variable from our analysis. Additionally, we found that age, customer activity status, and balance were the most correlated variables with the target variable.

Model Evaluation: To predict customer churn, we trained and evaluated several machine learning models, including Logistic Regression, Decision Tree, Random Forest, and Gradient Boosting Classifier. The evaluation was based on multiple metrics, including accuracy, precision, recall, and F1-score.

Best Model Selection: After considering all the metrics, we selected the Random Forest Classifier as the best model for our customer churn prediction task. It achieved the highest accuracy of 0.8697 among all the models. However, it's important to note that the choice of the best model may depend on the specific requirements and priorities of your application. It is recommended to assess different metrics and choose the model that best aligns with your needs.

Interpreting Results: While analyzing the categorical variables in relation to the target variable, we found that the distribution of values appeared to be relatively consistent between positive and negative outcomes. However, it is possible that when considering multiple variables together, new patterns or associations could emerge that were not apparent in the bivariate analysis alone. Additionally, we discovered that older customers were more likely to leave the bank.

In conclusion, by leveraging machine learning techniques and thorough analysis of the dataset, we were able to build a predictive model for customer churn. The selected Random Forest Classifier offers high accuracy and performs well in identifying potential churned customers.
