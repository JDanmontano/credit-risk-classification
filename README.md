# credit-risk-classification
Overview of the Analysis
This analysis aimed to build and evaluate a machine learning model to assess loan risk based on historical data from a peer-to-peer lending platform. The goal was to predict the likelihood of a loan default by analyzing financial data from borrowers. The model used the loan_status column in the dataset as the target variable, which indicates whether a loan is healthy (0) or at high risk of default (1). The dataset contained 75,036 healthy loans (value 0) and 2,500 high-risk loans (value 1), showing a significant imbalance between the two classes.

Machine Learning Process
The steps taken in the machine learning process are outlined below:

Data Import: The dataset was loaded into a Pandas DataFrame for easier manipulation and analysis.
Feature and Label Creation: The target variable (loan_status) was separated as the label set (y), and the remaining features such as loan size, interest rate, borrower income, and debt-to-income ratio were used as the input features (X).
Data Splitting: The data was divided into training and testing datasets using the train_test_split() function to ensure a fair evaluation of the model.
Model Creation: A Logistic Regression model was chosen and trained on the dataset.
Model Prediction: Predictions were generated using the model's predict() method to classify loans as either healthy or high-risk.
Model Evaluation: The model's performance was assessed using a confusion matrix and a classification report, which provided insights into its accuracy, precision, and recall scores.
Results
Here are the results of the Logistic Regression model trained on the original dataset:

Accuracy: The model achieved an impressive accuracy score of 99.0%, meaning it correctly classified 99 out of 100 loans. However, this high accuracy is somewhat misleading because the dataset is imbalanced, with a large majority of healthy loans (96.77%).
Precision:
Healthy Loans (Class 0): The model achieved 100% precision, meaning every loan predicted as healthy was actually healthy.
High-Risk Loans (Class 1): The model achieved 85% precision, indicating that some loans predicted as high-risk were not actually high-risk, although this number is still relatively strong.
Recall:
Healthy Loans (Class 0): The recall for healthy loans was 99.0%, meaning the model correctly identified 99% of all healthy loans.
High-Risk Loans (Class 1): The recall for high-risk loans was 94.0%, meaning the model identified 94% of the high-risk loans but missed a few.
Summary
The Logistic Regression model performed very well in identifying healthy loans (class 0), achieving high precision and recall. However, the model struggled with high-risk loans (class 1) due to the imbalance in the dataset. While the model did achieve a solid recall of 94% for high-risk loans, the lower precision (85%) means that it made some false positive predictions, classifying healthy loans as high-risk. Given the importance of accurately identifying high-risk loans in the lending process, this could lead to issues if the goal is to minimize loan defaults. Therefore, further model adjustments or techniques, such as balancing the dataset or using a different model, might be necessary to improve predictions for high-risk loans.
