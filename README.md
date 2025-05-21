# Restaurant Success and Revenue Prediction
## Business Goal
There is always a demand for restaurants regardless of where you decide to live. Sometimes, restaurants will open with the plan of staying open for a long period of time, but it does not always work out. Restaurants can close just as quickly and have a new one take its place. The goal of this analysis is to develop a predictive model that can determine restaurant success based on various factors. This can help new restaurant owners in identifying what strategies to deploy and how to achieve success and longevity.

## Data
The Restaurant Success dataset from Kaggle includes 15 feature columns, 14 of which are useable for anaylsis. These features are both classified as categorical and numerical, and can be used to determine whether or not a restaurant would be a success. More info on this dataset can be found at [https://www.kaggle.com/datasets/liyangng/restaurant-success-prediction/data]

First I decided to look at a couple of the categorical features to determine whether something like location or cuisine type had any effect on restaurant success.

![Successful_Restaurant Comparison](Images/Successful_Restaurant_Comparison.png)
![Successful Restaurants per City](Images/Succ_Rest_perCity.png)
![Successful Restaurants per Cuisine](Images/Succ_Rest_perCuisine.png)

After having discovered no correlation between the categorical features, I took a closer look at what features exactly had a higher effect on restaurant success. From the heatmap and scatterplot shown below, I determined that Social Media Followers and Marketing Budget had the highest impact on a restuarant's success.

![Restaurant Success Correlation Heatmap](Images/Restaurant_Success_Corr_HM.png)
![Social Media Followers vs Marketing Budget Scatterplot](Images/SCTPLT_Social_Media_Followers_vs_Marketing_Budget.png)

After this preliminary inspection, the data was split into training and test data.

## Modeling and Performance

In this project we employed various modeling techniques to classify whether a restaurant was successful, and to predict annual revenue. The models that were used for classification included `Logistic Regression`, `KNN`, `Decision Trees`, and `Random Forest`. The metrics that were used for comparisons for the classification models include Accuracy (train and test), R2 score, MSE, Precision Score, and Recall Score.

![Inital Classification Model Performance Comparison](Images/Inital_Classification_Model_Performance_Comparison.png)

As shown in the figure above, the decision tree model and the random forest model performed significantly better than the dummy model, the logistic regression model, and the k-nearest neighbors model. When looking at the other metrics, we can clearly see that decision tree and random forest outperform both logistic regression and k-nearest neighbors by having a higher r2 score and lower MSE. This can be seen in the barplot below.

![Further Analysis Results](Images/Further_Analysis_Results.png)

After having done a first pass on these models, I used GridSearchCV to find the models best performance hyperparameters. The results can be seen in the following barplots.

![Enhanced_Model_Accuracy_Comparison](Images/Enhanced_Model_Accuracy_Comparison.png)
![Enhanced Models Further Analysis Results](Images/Enhanced_Models_Further_Analysis_Results.png) 

The models that were used for regression included  `SVM`, `Linear Regression`, `Lasso`, and `Random Forest`.  The metrics that were used for comparisons for the regression models include Accuracy (train and test), R2 score, MSE, and MAE.

## Conclusions

