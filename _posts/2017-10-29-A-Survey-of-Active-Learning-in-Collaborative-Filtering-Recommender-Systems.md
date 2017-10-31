---
layout: post
title:  "A survey of active learning in collaborative filtering recommender systems"
categories: recommender system
published: true
---

Source: <http://www.sciencedirect.com/science/article/pii/S1574013715300150>

In this paper the authors make an excellent work in compiling the most used active learning strategies for collaborative filtering, dividing them in personalized and non-personalized, and the number of heuristics used.

Active learning aims to find the data points that could better help the system to perform the recommendation task, because obtaining a lot of training data is expensive for the system.

A brief explanation of these divisions are that non-personalized strategies don't differentiate wether the user has already rated some items and propose new items for them to evaluate in order to improve the recommender accuracy, but in personalized strategies the items proposed to the users depends in part to what they have already seen and rated.

The number of heuristics is clear in what is the approach, they divide the strategies in single-heuristic and combined-heuristic, the single ones only use one approach to learn the items to ask the user, and combined-heuristic use a mixture of heuristics resulting in a hybrid evaluation of the most important scores for the system to improve.

After an explanation of the collaborative filtering algorithms in existence and the description of each active learning strategy, the authors proceed to evaluate the performance of these strategies using different metrics and comparing the results with other strategies, also they take into account the if the evaluation was offline or online.

I liked how this paper analyzes all these strategies and how they could be benefitial for different kinds of environments, but also their drawbacks. Also the online and offline is an interesting approach in how these strategies should be evaluated, considering the natural acquisition of ratings and that in offline tests, the continuous asking to users for ratings are often not quite realistic, as they said, if a user is constantly asked for ratings they will ignore them or quit the system, generating a bias in the evaluation method of active learning.

Finally, the practical guideline makes some interesting points in how you can evaluate active learning strategies to ensure more realistic results that will help improve these systems and that can be put into production, helping to solve the common problems of collaborative filtering algorithms and the expensiveness of gathering new data for training these systems.
