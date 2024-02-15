# credit-risk-classification


## Credit Risk Analysis Report
-------------------------------
### Overview of the Analysis
-------------------------------
The purpose of this analysis was to use information about borrowers to train a model, so that loan risk could be effectively determined for future loans. The financial information that was taken into consideration to train the model was a borrower's loan size, interest rate, income, debt to income ratio, number of accounts, any derogatory marks, and total amount of debt. The data then told whether or not the loan was healthy or high-risk in each case. In the dataset that was used there were 75,036 instances of healthy loans and 2500 instances of high-risk loans. To start the analysis, the target (whether the loan was healthy or high-risk) was split from the rest of the data (the features). Then both the target and features were split into training and testing data. Then, two models were created and evaluated. The first model was a logistic regression model that was trained with the training data, both the features and the target, and then predicted results using the test data of features. The predictions were then compared with the actual target results and evaluated to see how accurate the model was. The second model was a logistic regression model as well, but the data used to train the model was oversampled to try to balance the amount of healthy loans and high-risk loans that were taken into consideration when training the model. This second model then predicted results from the testing data and was evaluated to see how well it could predict the loan status.

### Results
-------------------------------
* Machine Learning Model 1:
    * Accuracy: The balanced accuracy was 95.2%. This means that the model predicted 95.2% of healthy and high-risk loans correctly.
    * Precision: For healthy loans, the precision of the model was 100%. If a loan was predicted to be healthy, it was actually healthy 100% of the time. For high-risk loans, the precision of the model was 85%. If a loan was predicted to be high-risk, it was actually high-risk 85% of the time.
    * Recall: For healthy loans, the recall of the model was 99%. If a loan was actually healthy, it was predicted to be healthy 99% of the time. For high-risk loans, the recall of the model was 91%. If a loan was actually high-risk, it was predicted to be high risk 91% of the time.

* Machine Learning Model 2 (used the oversampled data):
    * Accuracy: The balanced accuracy was 99.4%. This means that the model predicted 99.4% of healthy and high-risk loans correctly.
    * Precision: For healthy loans, the precision of the model was 100%. If a loan was predicted to be healthy, it was actually healthy 100% of the time. For high-risk loans, the precision of the model was 84%. If a loan was predicted to be high-risk, it was actually high-risk 84% of the time.
    * Recall: For healthy loans and high-risk loans, the recall of the model was 99%. Whether the loan was actually healthy or high-risk, the model's prediction was correct 99% of the time.

### Summary
-------------------------------
Both models were effective at predicting correctly whether a loan would be healthy or high-risk. However, the second model, which used the oversampled training data, would be the recommended model. This model had a higher balanced accuracy (99.4%) than the first model (95.2%), so it was able to more accurately predict both types of loans. When considering which model was better at predicting healthy loans, they were identical in their precision and recall. Both models had 100% precision and 99% recall for healthy loans. When considering which model predicted high-risk loans better, the second model had a higher recall for high-risk loans (99%) than the first model (91%) and a similar precision (84%) to the first model (85%). The second model used more high-risk loan data when it was trained, which could explain the higher recall for high-risk loans.


### Sources
-------------------------------
* In line [14], used https://imbalanced-learn.org/stable/references/generated/imblearn.over_sampling.RandomOverSampler.html as a resource to fit and resample the training data with .fit_resample()
