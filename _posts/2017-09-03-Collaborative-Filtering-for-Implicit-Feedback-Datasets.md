---
layout: post
title:  "Collaborative Filtering for Implicit Feedback Datasets"
categories: collaborative-filtering implicit-feedback
published: true
---

Working with implicit feedback databases is a whole different problem than with information obtained directly from the users (explicit feedback) because we don't have a direct way of telling if the user doesn't like an item if he/she didn't interacted with it, and therefore it's needed a way to interpret these new kind of data so we can make better recommendations in environments where it's hard to obtain first-hand data.

In this method instead of using only the elements watched by a user *u*, they use the complete database using two variables: $$ p_{ui} $$ which binarizes the variable $$ r_{ui} $$ to represent if a item *i* was watched by user *u* (preference), and $$ c_{ui} = 1 + \alpha r_{ui} $$ that represents the level of confidence in that item *i* will be liked by user *u*.

It's noted that this rate of increase in confidence ($$ \alpha $$), worked best for them with $$ \alpha = 40 $$, but I think an explanation on how they got to that number and the implications of using bigger or smaller numbers in the tests would be nice to better understand how this variable represents confidence, also when they address they're more ways to transform $$r_{ui}$$ into confidence level and show the alternative method $$ c_{ui} = 1 + \alpha \ log(1 + \frac{r_{ui}}{\epsilon}) $$ would be interesting to see the effects on recommendations.

It's very interesting how this approach can even explain the recommendations made, which other latent factor methods couldn't, making a breakthrough in this kind of algorithms, also the interpretation given by the authors in terms of how the time watching a show is related with the confidence in that show is easily understandable, including when they discarded recurring tv shows.

To summarize, this paper explains well this algorithm and how to handle a implicit-feedback database, what are the common problems and things to consider before designing a recommendation algorithm, even though this particular one has scalability problems, it has a lot of value for further research.