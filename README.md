# NLP-project-1
Part 1 of the NLP with Hotel Reviews Deliverable

# NLP With Hotel Review Part 1
Due: Nov 15, 2020 by 11:59pm

In this deliverable, you will develop several machine learning models to correctly label the sentiment behind hotel reviews.

You will begin with some Exploratory Data Analysis (EDA), and then move into data augmentation, modelling, and iteration over model improvements.

Exploratory Data Analysis
First let's look at the data set, which you can download here.

The target column of interest is Reviewer_Score.

What is the shape of the dataset?
The reviews provided are all given as decimal values. Convert them into integers from 1 to 10
The reviews are scored from 1 to 10. What do you expect the distribution of scores to look like? What is the actual distribution of reviews?
Given this will be a classification problem, what is a potential problem with this distribution?
This dataset has a good mix of numeric and non-numeric columns. Which columns are numeric? Which are non-numeric? Can you turn some of the non-numeric columns to numeric?

Data Wrangling
Build the proper dataset separation (Optional but recommended: The dataset is actually too big to run quickly on most laptops. Feel free to sample ~10% of the data as your dataset from this point on. Make sure all classes are included in your subsample.)
Convert the Reviewer_Score column into a binary column in the following way. Reviews that are below 9 should be encoded as 0 ('not good') and reviews with scores 9 and 10 as 1 ('good').
Convert the columns you identified in question 2 into numeric columns, and drop all non-numeric columns except Positive_Review and Negative_Review.
Split the data into train and test sets.
Use a count vectorizer to combine Positive_Review and Negative_Review with the numeric data (notice that this is done AFTER the train/test split). You should vectorize each column separately, ending up with two sparse matrixes, and then combine the three matrixes (numeric data, positive matrix, negative matrix). You may have to adjust the min_df parameter.
What does the min_df parameter do?

# NLP With Hotel Review Part 2
Due: Nov 22, 2020 by 11:59pm

Your education team will provide you with "clean" data files for this deliverable.

Your target column is the "rating" column which is a binary column denoting good ratings as 1 and bad ones as 0.

Modeling
Employ a linear classifier on this dataset:

Fit a logisitic regression model to this data with the solver set to lbfgs. What is the accuracy score on the test set?
What are the 20 words most predictive of a good review (from the positive review column)? What are the 20 words most predictive with a bad review (from the negative review column)? Use the regression coefficients to answer this question
Reduce the dimensionality of the dataset using PCA, what is the relationship between the number of dimensions and run-time for a logistic regression?
List one advantage and one disadvantage of dimensionality reduction
Employ a K-Nearest Neighbour classifier on this dataset:

Fit a KNN model to this data. What is the accuracy score on the test set?
KNN is a computationally expensive model. Reduce the number of observations (data points) in the dataset. What is the relationship between the number of observations and run-time for KNN?
List one advantage and one disadvantage of reducing the number of observations.
Use the dataset to find an optimal value for K in the KNN algorithm. You will need to split your dataset into train and validation sets.
What is the issue with splitting the data into train and validation sets after performing vectorization?
Employ a Decision Tree classifier on this dataset:

Fit a decision tree model to this data. What is the accuracy score on the test set?
Use the data set (or a subsample) to find an optimal value for the maximum depth of the decision tree. You will need to split your data set into train and validation.
Provide two advantages of decision trees over KNN. Provide two weaknesses of decision trees (classification or regression trees)
What is the purpose of the validation set, i.e., how is it different than the test set?

Re-run a decision tree or logistic regression on the data again:

Perform a 5-fold cross validation to optimize the hyperparameters of your model.
What does your confusion matrix look like for your best model on the test set?
Create one new feature of your choice:

Explain your new feature and why you consider it will improve accuracy.
Run the model from question 5 again. You will have to re-optimize your hyperparameters. Has the accuracy score of your best model improved on the test set after adding the new feature you created?
