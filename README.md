# Erin_Portfolio
Data Science Portfolio

# [Project 1: Mushroom Classifier]
I will be investigating the K Nearest Neighbors and PCA algorithms using sklearn's KNeighborsClassifier and PCA class. I will use a RandomForestClassifier and a Logistic Regression to predict whether or not a mushroom is edible based on the mushroom dataset. The KNN algorithm will be used to fill in missing values in our dataset and the PCA algorithm will be used to reduce the dimensionality of the data. The goal is to evaluate the effect of dimensionality reduction on two common models and to gain experience with the KNN algorithm with respect to imputation. This Notebook is broken down into 7 sections:
1). Import Data
- Simply importing .csv containing the mushroom dataset
2. Investigate and Fix Data
- Print out data and fill in any missing values using KNN algorithm
3. Train on Full Dataset
- Encode the full dataset, train the RandomForestClassifier and Logistic Regression, and comment on training time
4. Evaluate Performance on Full Dataset
- Calculate accuracy, precision, and recall scores for each model and comment on results
5. Reduce Dimensionality
- Apply PCA reduction to full dataset, display old and new dimensions and reduction percentage
6. Train on Reduced Dataset
- Retrain RandomForestClassifier and Logistic Regression on reduced dataset and comment on training times
7. Compare Performance
- Tabulate RandomForestClassifier and Logistic Regression performance data for both datasets and comment on results




Conclusions
Based on the table above, the models perform worse with the reduced dataset, however the drop in performance is greatly outweighed by the drop in dimensions. This means even with a logistic regression, which is a fairly simple model, we can expect decent results with much less training time. However, the RandomForestClassifier takes longer to train on the reduced dataset because there are fewer ways in which the data can be split. Even so, the RandomForestClassifier performs very well - greatly outperforming the logistic regression on the reduced dataset in both accuracy and precision, but losing slightly in recall. This means the RandomForestClassifier is more likely to get the correct prediction and less likely to have false positives (in this case falsely identifying a poisonous mushroom as edible). But, the RandomForestClassifier is less likely to get all edible mushrooms (falsely labels as poisonous). So, overall, the RandomForestClassifier performs better on the reduced data, especially because the logistic regression is much more likely to say a poisonous mushroom is edible. I would also conclude that using the logistic regression on the full dataset is the best option because it did not miss any mushroom labels and had a lower training time compared to the RandomForestClassifier.
