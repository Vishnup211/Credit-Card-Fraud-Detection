# Credit-Card-Fraud-Detection
Data Science Task 5: Credit Card Fraud Detection 
### Objective of This Project
Credit card fraud poses a serious financial risk, resulting in substantial financial losses to consumers and financial institutions. The objective of this project is to create a machine learning model that accurately identifies fraud transactions while producing fewer false positives 
###  Data Preprocessing & Feature Engineering
Removed duplicate entries to prevent data redundancy
Checked for missing values and ensured data integrity

### In the Feature Engineering part to imrove the perfomance of the model,
#### Transaction Hour
Extracted from timestamps to identify time-based fraud patterns.
#### Night Transaction
Flagged transactions occurring between 10 PM and 6 AM, as fraud tends to happen more during off-hours.
#### Log Amount 
Applied log transformation to normalize the distribution of transaction amounts.
#### Transaction Frequency
Counted the number of transactions per hour to detect unusual transaction bursts.
#### Amount Deviation
Calculated the difference between the transaction amount and the mean amount for that hour to identify anomalies.
### To handle Class Imbalance 
The legit tranaction are more frequent than the fradulent transactions so in order to reduce imalance issuse , The Over-sampling Technique use is SMOTE
### Model Selection & Training
The  model selected here is Random Forest Classifier
### Model Evaluation & Results
The model achieved exceptional performance:
Classification Report:
              precision    recall  f1-score   support

           0       1.00      1.00      1.00     56651
           1       1.00      1.00      1.00     28325
    accuracy                           1.00     84976
   macro avg       1.00      1.00      1.00     84976
weighted avg       1.00      1.00      1.00     84976

### Confusion Matrix:
[[56645     6]

 [    1 28324]]
### ROC-AUC Score
 0.9999889336519697

### Conclusion
The Random Forest model was able to successfully detect the fradulent transactions and it had an approx of 100 % accuracy and had very low false postive rate
 
