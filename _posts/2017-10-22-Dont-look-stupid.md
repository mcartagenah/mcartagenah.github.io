---
layout: post
title:  "Don't look stupid: Avoiding pitfalls when recommending research papers"
categories: recommender system
published: true
---

Source: <https://www.researchgate.net/publication/220878703_Don%27t_look_stupid_Avoiding_pitfalls_when_recommending_research_papers>

In this paper, the authors state that recommender systems should support a wide variety of tasks to fulfill, putting the example of a research paper recommender for a digital library, and how a recommender system could use different algorithms for different tasks.

But recommender system accuracy is not the only aspect to analyze if you want a good recommender, according to the paper it needs to be useful, and that's where the term usefulness is used to describe a good recommender that avoid the common pitfalls:
* Not building user confidence $$\longrightarrow$$ trust failure
* Not generating any recommendations $$\longrightarrow$$ knowledge failure
* Generating incorrect recommendations $$\longrightarrow$$ personalization failure
* Generating recommendations to meet the wrong need $$\longrightarrow$$ context failure

With this, it's stated that a system needs to avoid these common pitfalls for it to grow, but it can be difficult.

When the HRI model is explained, it's easy to understand the main idea, but seeing the aspects table some terms could be developed a little more to really understand HRI and what are they trying to accomplish abstracting this problem to the user interaction with the recommender system. For example when they mention all the models of information seeking behaviour, it doesn't explain how they used them to modelate the problem.

The experiments done were interesting and it made sense in how they will test if the HRI model would get better results using different algorithms for a set of different tasks in a digital library setting, and the fact that they obtained atypical results with what they were expecting makes an interesting case study, and I liked their conclusion, that recommender systems that generate bad items or nonsensical for the context really harms the user view and predisposition towards the recommender, falling into the pitfall of trust failure.