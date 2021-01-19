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
