---
layout: post
title:  "Slope One Predictors for Online Rating-Based Collaborative Filtering"
categories: recommender system collaborative-filtering slope-one
published: true
---

The slope one algorithm tries to resolve a bunch of problems found in user-based and item-based collaborative filtering, specially that they're relatively hard to update when the database expands, they're not very efficient (scalability problem) and they have the cold-start problem.

In this paper they make a good job explaining the difference between the similarity measure used by user-based and item-based CF, and the "popularity differential" used in slope one, but the nomenclature can be a little bit tricky to understand.

Basically in slope one we're looking for the best predictor of the form *f(x) = x + b* which translates in *b* being the average difference between the evaluation arrays of two items.

In the experimental results part, they use MAE to measure the effectiveness of the predictions which is a commonly used evaluation metric.
I think is confusing how they separated the training and test sets, because first it says "In computing MAE, we successively hide ratings one at a time from all evaluations in the test set while predicting the hidden rating, computing the average error we make in the prediction." which implies they're using a leave-one-out cross validation, but later they say "we used enough evaluations to have a total of 50,000 ratings as a training set (χ) and an additional set of evaluations with a total of at least 100,000 ratings as the test set (χ')." which I think doesn't help to fully understand how they calculated the error metric.