---
layout: post
title:  "Collaborative Filtering Recommender Systems"
categories: recommender system collaborative-filtering
published: false
---

This paper takes a complete tour on collaborative filtering, what is the core idea behind them, non-probabilistic and probabilistic algorithms, uses and challenges of their use, methods of evaluation among other things relevant for their understandment. This is a very educational paper, because it's explained step-by-step how these algorithms were conceived.

I think this paper does a good job introducing most of the useful concepts of collaborative filtering, and also showing the most used algorithms and how do they work, but one part that had my interest is the comparison of Collaborative Filtering with Content-Based Filtering because since it can predict relevance for items without ratings it could be used as a solution for the *New item* cold-start problem in collaborative filtering, making a hybrid solution that when a new item is added, it can be recommended to the users by similarity in content with other items rated good by the user. Even though this doesn't mean if two items have similar content (e.g. same terms, tags, description used, etc) they'll be similarly rated by a user, because the quality of the content can't be measured by the features used in content-based filtering, but it's a good approach to give new items chance to be rated.

The evaluation methods described in the paper, apart from accuracy seem to be useful in designing recommender systems, not only in collaborative filtering, because they're some criterias that aren't objective and depending on the types of recomendations it could be more meaningful to determine if it's a good recommender system, from the list mentioned, *novelty* and the concept of *serendipity* are the most interesting and in my opinion the hardest to achieve.

Finally, despite this paper being wrote in 2007, mentions ongoing challenges for collaborative filtering and although they're newer algorithms with better complexity, the challenges are still relevant I think, for the whole area, and not only CF algorithms. The privacy and security problem are always important to keep in mind, because for this kind of algorithms to work we need a huge amount of personal data to provide better recomendations, and normally security is the last concern when implementing these things. I think the trust problem is a recurring one even today in modern recommender systems, because it's hard to determine a shilling attack, or it's model-specific.
