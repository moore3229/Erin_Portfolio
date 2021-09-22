# Erin_Portfolio
Data Science Portfolio

# [Project 1: Mushroom Classifier: Project Overview](https://github.com/moore3229/Mushroom-Classifier)
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




Conclusion:
Based on the table above, the models perform worse with the reduced dataset, however the drop in performance is greatly outweighed by the drop in dimensions. This means even with a logistic regression, which is a fairly simple model, we can expect decent results with much less training time. However, the RandomForestClassifier takes longer to train on the reduced dataset because there are fewer ways in which the data can be split. Even so, the RandomForestClassifier performs very well - greatly outperforming the logistic regression on the reduced dataset in both accuracy and precision, but losing slightly in recall. This means the RandomForestClassifier is more likely to get the correct prediction and less likely to have false positives (in this case falsely identifying a poisonous mushroom as edible). But, the RandomForestClassifier is less likely to get all edible mushrooms (falsely labels as poisonous). So, overall, the RandomForestClassifier performs better on the reduced data, especially because the logistic regression is much more likely to say a poisonous mushroom is edible. I would also conclude that using the logistic regression on the full dataset is the best option because it did not miss any mushroom labels and had a lower training time compared to the RandomForestClassifier.




# [Project 2: Covid-19 Database: Project Overview](https://github.com/moore3229/Covid-19-Database)

Our goal is to investigate Covid-19 data obtained from AWS in order to better understand the virus's economic and socioeconomic effects. The data given by AWS' "Covid-19 Harmonized Dataset" is quite detailed, and it comes from "The Covid Tracking Project." As of March 7th, 2021, “The Covid Tracking Research” will stop collecting new data, which will have no effect on our project. Researchers, doctors, non-profits, educational institutions, students, and government organizations will all benefit from this database. These are the people that are involved in our project. We plan to build the database specifically to address queries about population density and covid-19 instances.

This project will help with research efforts among, public entities, private entities, and startups. The python app we will develop will be simple. We will use our python app to connect to the database, read and display select data, update specific data, and get state, population, and average daily hospitalization by state in descending order of hospitalization rate.
The intent of our efforts is to attempt to answer the question:

How does state population density relate to spread of the disease (a measure of the effectiveness of social distancing). Texas has nearly 20 million more residents than Michigan – and yet – Texas has a lower rate of positive cases than Michigan. Why? Is it due to Michigan have a higher number of elderly residents or due to increase property?

Conclusion:
We were able to gain insights, but due to the quality of the data we were not able to answer the specific questions we had as it pertained to the correlation of positive cases, death(s), age, employment, and poverty.
However – we were able to determine that there is a weak correlation between population density and positive covid cases. We used the following:

SELECT (AVG(POSITIVE * POP_DENSITY) - AVG(POSITIVE) * AVG(POP_DENSITY)) /
(SQRT(AVG(POSITIVE * POSITIVE) - AVG(POSITIVE) * AVG(POSITIVE)) * SQRT(AVG(POP_DENSITY * POP_DENSITY) - AVG(POP_DENSITY) * AVG(POP_DENSITY)))
AS CORRELATION_COEFFICIENT_POPULATION FROM C19_TRK_US_STATES_DAILY D
INNER JOIN C19_TRK_US_POPULATION_STATES P ON D.STATE = P.STATE WHERE DATE = '2020-03-15 00:00:00';

Due to relatively low correlation coefficient – the increase in positive cases may have more to do with low engagement in preventative measures – such as masks, social distancing, and hand washing – than population density.

# [Project 3: Polynomial Regression: Project Overview](https://github.com/moore3229/Polynomial-Regression)

Polynomial Regression Problem

- Created the following figure using matplotlib, which plots the data from the file called PolynomialRegressionData_II.csv
- Performed a PolynomialFeatures transformation, then perform linear regression to calculate theoptimal ordinary least squares regression model parameters.
- Recreated the first figure by adding the best fit curve to all subplots.
- Infered the true model parameters.


# [Project 4: ]



# [Project 5: Data Visualization - Tableau: Project Overview]




# [Project 6: Data Visualization - Qlik: Project Overview]




