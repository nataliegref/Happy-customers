
# Happy customers

## Problem statement:

We are one of the fastest growing startups in the logistics and delivery domain. We work with several partners and make on-demand delivery to our customers. During the COVID-19 pandemic, we are facing several different challenges and everyday we are trying to address these challenges.

We thrive on making our customers happy. As a growing startup, with a global expansion strategy we know that we need to make our customers happy and the only way to do that is to measure how happy each customer is. If we can predict what makes our customers happy or unhappy, we can then take necessary actions.

Getting feedback from customers is not easy either, but we do our best to get constant feedback from our customers. This is a crucial function to improve our operations across all levels.

We recently did a survey to a select customer cohort. You are presented with a subset of this data. We will be using the remaining data as a private test set.

## Data Description:

Y = target attribute (Y) with values indicating 0 (unhappy) and 1 (happy) customers
X1 = my order was delivered on time
X2 = contents of my order was as I expected
X3 = I ordered everything I wanted to order
X4 = I paid a good price for my order
X5 = I am satisfied with my courier
X6 = the app makes ordering easy for me

Attributes X1 to X6 indicate the responses for each question and have values from 1 to 5 where the smaller number indicates less and the higher number indicates more towards the answer.

## Download Data:

https://drive.google.com/open?id=1KWE3J0uU_sFIJnZ74Id3FDBcejELI7FD

## Goal(s):

Predict if a customer is happy or not based on the answers they give to questions asked.

## Success Metrics:

Reach 73% accuracy score or above, or convince us why your solution is superior. We are definitely interested in every solution and insight you can provide us.

Try to submit your working solution as soon as possible. The sooner the better.

## Bonus(es):

We are very interested in finding which questions/features are more important when predicting a customer’s happiness. Using a feature selection approach show us understand what is the minimal set of attributes/features that would preserve the most information about the problem while increasing predictability of the data we have. Is there any question that we can remove in our next survey?


# Method and Results
## Exploratory data analysis
I first explored the data to gain insights. This included assessing the balance of the data (54% of the data is Y=1) and how many entries we have (126) and how many features (6).
This exploration showed there was no missing data.
I then looked at histograms of the distribution of each of the features to better understand the dataset, as well as analyzed the feature importance for each 6 features.

## Building models
I then built several models: Logistic regression, KNN, Decision tree, Random forest, Gradient boostibng, and XGboost.
I trained these models using using training data (randomly selected from the whole dataset) at both a 80% and 75% split.
I also trained these models using scaled and unscaled data.
Finally I tried dropping one or two feature(s) to see if it improved the results of the models.

## Conclusion
The results showed that removing features X2 and X4 (the lowest on the chi square importance ranking) helping bring the accuracy above the target of 73%, using the Logistic regression model.
These questions can therefore be removed from the questionaire.
