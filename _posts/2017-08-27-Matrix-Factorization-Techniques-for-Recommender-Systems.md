---
layout: post
title:  "Matrix Factorization Techniques for Recommender Systems"
categories: recommender system matrix-factorization netflix-prize
published: true
---

Latent factor methods came as an alternative to neighbourhood methods, where it stopped analyzing the relationship between item-user and used a number of latent factors to predict rating patterns, taking advantage of computer calculated dimensions of the data.

Matrix factorization is one of the most succesful realization of latent factor models, in its most basic form you have the factor vector for an item *i* and user *u*, the prediction *r* can be calculated with the dot product of these vectors:

$$r_{ui} = q_i^T p_u$$

In this paper it's well explained the basic idea of matrix factorization and shows the 2 ways of calculating these vectors, but they focus on the minimization problem of the regularized squared error on the set of known ratings, because with SVD there are complications with a high sparsity of the data.

Next, it's shown the 2 approaches to solve the problem, listing their pros and cons and how they're calculated (in simple terms), but I would prefered some tests using both approaches in different datasets to see better their use cases and why to use one instead of the other.

I really liked the cases where matrix factorization can be more flexible to different types of data, not only explicit feedback, and applying more interpretations to the data, like temporal dynamics and confidence levels. It's easy to see how these method bring collaborative filtering to a new level, taking advantage of implicit feedback to solve typical problems like *cold start* or the evolution of a person's preferences, that in the neighbourhood versions of collaborative filtering can't be achieved using only explicit feedback.
