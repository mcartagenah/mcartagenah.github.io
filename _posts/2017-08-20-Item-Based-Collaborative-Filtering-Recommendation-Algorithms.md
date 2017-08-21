---
layout: post
title:  "Item-Based Collaborative Filtering Recommendation Algorithms"
categories: recommender system collaborative-filtering item-based algorithm
published: true
---

In this paper we're presented with an alternative to user-based collaborative filtering which is using the similarity between items to predict ratings. This method improves the time required to produce a recommendation because it doesn't need to calculate the neighbourhood of the user, this calculation changes constantly because new user arrive more often than items into the system, allowing to pre-compute this neighbourhood, improving the speed of the model.

Here they show three methods to calculate the item similarity: *cosine-based similarity*, *correlation-based similarity* and *adjusted cosine similarity*.

In the experimental results, I liked that they tried first the sensitivity of the parameters in the model to find the best ones and later sticked to these values for the whole procedure, and also that they experimented with the ratio between training and testing sets. The comparison with other typically used algorithms for recommendations shows the real performance of this algorithm and what are their advantages and disadvantages with the other models. Here you can see that item-based CF gets better quality of predictions in general compared to user-based CF, but they're not significantly large. The area where item-based excels is in the time it requires to produce recommendations and the relationship between the model size and quality of output makes this algorithm achieve the goals proposed at the beginning of the publication.

With these conclusions we can clearly see that we need better recommendation algorithms to process the level of data available today, and that user-based CF isn't viable to use in these days that we require faster and better results to compete in the business world.