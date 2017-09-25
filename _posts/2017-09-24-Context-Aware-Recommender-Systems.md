---
layout: post
title:  "Context-Aware Recommender Systems"
categories: context-aware context recommender system
published: true
---

Source: <https://www.aaai.org/ojs/index.php/aimagazine/article/view/2364>

Context is a powerful tool to improve recommendations, and rather than spending a lot of time defining what it is "context", this paper presents all the different forms of categorising the knowledge of a system about the contextual factors of the information, and the paradigms in which context is used, in order to better understand how context is used in different implementations.

The main difference between traditional recommender systems and context-aware recommender systems, is that in the first we worked with partial knowledge of the users preferences, getting information like $$(user, item, rating)$$ to predict unknown ratings from a user to different items. With context, we also get an additional field which is the context where the user rated a certain item, these can be helpful to make a more accurate prediction, although in not all cases this is true, and therefore it has to be studied case to case.

Depending on how the contextual information is used in the recommendation process it can be separated in three categories:
* __Contextual prefiltering:__ the contextual information is used to pre-select the data to be used in the recommendation algorithm, specifically in the rating prediction.
* __Contextual postfiltering:__ the contextual information is used to refine the results from the recommender system.
* __Contextual modeling:__ the contextual information is directly used in the rating prediction.

One of the most interesting characteristic of these paradigms is that the first two can be applied to any recommendation system already implemented, because they're not altering the process of generating unknown ratings, for example if after being tested that context helps to better predict ratings in some cases, a hybrid recommender could be made that in those cases uses the context-aware version.

Although contextual filtering can be easy to implement, contextual modeling can be more interesting and be used to get more complex models of recommendation, specially if mixed with contextual prefiltering and postfiltering, because these paradigms aren't necesarilly meant to be used alone, including with other recommender systems, which can be an interesting area to study and research.

In conclusion, this paper is a good introduction to context-aware systems, how they're categorised depending on the level of knowledgement a system has, or how the context data is used, also giving examples of real implementations, and stating the challenges of these types of recommending systems.
