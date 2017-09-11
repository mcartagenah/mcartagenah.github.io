---
layout: post
title:  "Collaborative Filtering for Social Tagging Systems: An Experiment with CiteULike"
categories: collaborative-filtering social-tagging
published: true
---

In this paper they compare the classic user-based collaborative filtering algorithm, with 2 variations:
* The addition of a neighbor-weight parameter in the prediction stage of the algorithm.
* The change of the _Pearson_ correlation similarity for BM25-based similarity, mainly used in information retrieval.

I think it's well explained the dataset characteristics, how they obtained it, and what pre-process they made, specifically the use of stemmed tags.

Looking at the results, you can see how these 2 variations improve the precision and nDCG of the classical user-based CF algorithm, but I would've liked a comparison in the training time, because user-based CF has complexity $$O(MN)$$ and in the BM25 similarity it is needed to look over all of the central users neighbors and their tags, which can be pretty big in comparison with the number of users.

To conclude, I think this paper brings interesting results in how to approach different recommendation problems, because as they explain, this dataset in particular doesn't represent a binarizable rating, here it's more like an amount of likeness to the item rather than a good or bad rating, and therefore the introduction of tags to CF algorithms can be beneficial.