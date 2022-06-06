# Credit_Risk_Analysis

## Overview of the Analysis
Credit risk is an inherently unbalanced classification problem. Therefore, using the credit card dataset given from the LendingCLub, we will be oversampling, undersampling and sampling a combination of both using RandomOverSampler, SMOTE, ClusterCentroids
and SMOTEENN. We will then use BalancedRandomForestClassifier and EasyEnsembleClassifier to reduce bias and then evaluate the performance of these models in order to see if they should be used to predict credit risk. 


## Results
### OverSampling
**RandomOverSampler:**
* There was a balanced accuracy score of 66.1%
![Screen Shot 2022-06-05 at 3 55 02 PM](https://user-images.githubusercontent.com/98780937/172073991-9f90c4b7-c0d1-4e1f-b0f2-63fc79a5c5f9.png)
* The High Risk had a precision score of 1% with a recall score of 72%.
* THe Low Risk had a precision score of 100% with a recall score of 60%.
![Screen Shot 2022-06-05 at 3 55 15 PM](https://user-images.githubusercontent.com/98780937/172073993-e3acc56e-0464-403b-917b-4a95e67106e0.png)
 
**SMOTE:**
* There was a balanced accuracy score of 66.3%
![Screen Shot 2022-06-05 at 4 08 13 PM](https://user-images.githubusercontent.com/98780937/172074348-0a9b16da-4483-4287-b96b-7173fb07932e.png)
* The High Risk had a precision score of 1% with a recall score of 63%.
* THe Low Risk had a precision score of 100% with a recall score of 69%.
![Screen Shot 2022-06-05 at 4 08 23 PM](https://user-images.githubusercontent.com/98780937/172074355-72722927-cdfe-4a69-b8f5-98dd23fe2288.png)

### UnderSampling
**ClusterCentroids:** 
* There was a balanced accuracy score of 54.4%
![Screen Shot 2022-06-05 at 4 12 07 PM](https://user-images.githubusercontent.com/98780937/172074527-c8c26804-1d26-4193-9ad2-de71d8628270.png)
* The High Risk had a precision score of 1% with a recall score of 69%.
* THe Low Risk had a precision score of 100% with a recall score of 40%.
![Screen Shot 2022-06-05 at 4 12 15 PM](https://user-images.githubusercontent.com/98780937/172074533-5331b98d-440d-400f-b7df-399d7078da75.png)

### Combination (Over and Under) Sampling
**SMOTEENN:** 
* There was a balanced accuracy score of 64.5%
![Screen Shot 2022-06-05 at 4 17 00 PM](https://user-images.githubusercontent.com/98780937/172074664-75fd28ac-c51c-43ca-a9fb-82a8ca65f1f2.png)
* The High Risk had a precision score of 1% with a recall score of 72%.
* THe Low Risk had a precision score of 100% with a recall score of 57%.
![Screen Shot 2022-06-05 at 4 17 08 PM](https://user-images.githubusercontent.com/98780937/172074667-d11c3576-a809-4f2e-92a1-df6cbefb3065.png)

### Ensemble Classifiers
**BalancedRandomForestClassifier:**
* There was a balanced accuracy score of 78.9%
![Screen Shot 2022-06-05 at 4 25 57 PM](https://user-images.githubusercontent.com/98780937/172074923-34ef4693-eba8-40c2-8ecb-872175f8d25b.png)
* The High Risk had a precision score of 3% with a recall score of 70%.
* THe Low Risk had a precision score of 100% with a recall score of 87%.
![Screen Shot 2022-06-05 at 4 26 04 PM](https://user-images.githubusercontent.com/98780937/172074928-8be6f1cc-3b76-400b-8bfa-e597f804cb4f.png)
* The feature importance with the highest percentage was "total_rec_prncp" at 7.9%
![Screen Shot 2022-06-05 at 4 31 55 PM](https://user-images.githubusercontent.com/98780937/172075129-e59bcadc-9871-4ebd-9c96-5c514f4f4b98.png)

**EasyEnsembleClassifier:**
* There was a balanced accuracy score of 93.2%
![Screen Shot 2022-06-05 at 4 27 26 PM](https://user-images.githubusercontent.com/98780937/172074966-f69af1c6-3eb1-4d35-a69c-4ae0d4794a9f.png)
* The High Risk had a precision score of 9% with a recall score of 92%.
* THe Low Risk had a precision score of 100% with a recall score of 94%.
![Screen Shot 2022-06-05 at 4 27 35 PM](https://user-images.githubusercontent.com/98780937/172074969-d9178a04-1daa-4a86-9149-6d8149fc40e3.png)

## Summary
Given the results of our six machine learning models, we can see that the EasyEnsembleClassifier had the highest overall score, with the balanced accuracy score of 93%, high risk precision and recall score of 95 and 92 percent, respectively, and low risk precision and recall score of 100 and 94 percent, respectively. Following the EasyEnsembleClassifier, was the BalancedRandomForestClassifier, SMOTE, RandomOverSampler, SMOTEENN, and lastly ClusterCentroids with a balanced accuracy score of 54%, high risk precision and recall score of 1 and 69 percent, and low risk precision and recall score of 100 and 40 percent. Therefore, I would recommend using the EasyEnsembleClassifier model as we would be most succesful at predicting credit risk given the highest overall score. 
