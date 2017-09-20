---
layout: post
title:  "Hybrid Recommender Systems: Survey and Experiments"
categories: hybrid recommender system
published: true
---

In [this paper](https://link.springer.com/article/10.1023%2FA%3A1021240730564) the author takes a complete tour in what is a hybrid recommender system, how you can combine 2 types of recommendation algorithms, the advantages and disadvantages of the most common recommender systems, and their experimentation with the Entree Chicago knowledge-based recommender system that they added collaborative-filtering with the cascade method shown in the paper.

It's well known that every recommendation algorithm has its flaws and good things that we can take advantage when combining different systems, and in Table II you can see the trade-off between the need to gather specific data and the problems with sparse data, because collaborative algorithms have cold start issues while others also need extra information about the users or the recommended items (Demographic, Utility-based and Knowledge-based).

According to the author, they're 7 ways to make a hybrid recommender system, where they can be divided in two groups, the ones that "mix" in certain ways the results of different recommeders (in the paper all the examples are with 2 systems, but it could be more) to improve the results, and other group where basically the results, features or model from one system becomes the input of another, or it refines the results from the first one.

### Group 1:
* __Weighted__: Basically, the results from different systems are combined with a score (or weight) into a single recommendation.
* __Switching__: Depending on the situation different algorithms are used.
* __Mixed__: Results from different systems are shown simultaneously.

### Group 2:
* __Feature combination__: The features of different recommendation data are used as input for a single algorithm.
* __Cascade__: The results from one system are refined by another.
* __Feature augmentation__: The output from one technique is used as the input of another one.
* __Meta-level__: The model learned from one system is the input of another system.

There's table IV with all the combinations between 2 recommender systems on one axis and on the other the type of hybridization, noting that they're combinations that can't be used with some hybridization models, because the information live in different spaces (CF with knowledge-based using Feature combination) or the models used can't be used as inputs into the other (Knowledge-based with Demographic using meta-level). Also they're redundant combinations in the table, and taking all this out, we get 53 possibilities where 14 have been explored (but from the year of the paper it's probable that they're already more combinations explored). This kind of analysis is very interesting to other researchers who can pick one of these combinations and study how it can improve recommendations, but also the definition of ways of implementing hybrid recommenders opens more doors to experiment with more than 2 algorithms, or using in different ways the data and results to resolve the current problems with non-hybrid systems.

To conclude, the making of a hybrid recommendation algorithm can be designed to address relevant problems of common systems, and also improve how the data is used and what new data can be extracted from it when combining different techniques, but also you have to be aware of the complications that this can bring when it's not thought the process of hybridization, from which way and data to combine, to what parameters are used in each algorithm, like in the case study of EntreeC and the different similarity algorithms used depending on how the data is going to be used, they analysed the use of Pearson, cosine and a metric made by them that uses the semantics of the ratings.