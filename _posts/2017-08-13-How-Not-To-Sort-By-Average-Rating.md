---
layout: post
title:  "How Not To Sort By Average Rating"
categories: recommender system sorting algorithms ratings
published: true
---

In [this post by Evan Miller](http://www.evanmiller.org/how-not-to-sort-by-average-rating.html), he discusses how to sort user rated items to put the highest-rated first and lowest-rated in the bottom, based in the solutions implemented by different websites, and how they're wrong in comparison of using the lower bound of the Wilson score confidence interval for a Bernoulli parameter.

First of all, I think this is an excellent post because it proposes a problem and analyzes known solutions showing the aspects that can be improved or  why they give a bias solution, and ends with a mathematical explanation of his proposed solution. Second, despite the year of the post, it's still a relevant discussion today because some websites still make this kind of mistakes either by a lack of mathematical knowledge or not taking the time to investigate a better solution to an apparently easy problem.

The only thing I didn't liked is how the author shows the Amazon solution is wrong (using the average rating), which I also understand it's not the best suited solution to the problem, but he doesn't even propose how to correct it in this case, because a 5-star rating system can't be fixed using the Wilson score confidence interval, simply because this only works in Bernoulli parameters, that means, variables whose outcomes are binary. I also understand that this is a harder problem as we have more information to analyze, but I imagine there are solutions for this, maybe using Bayesian inference.

I liked the implementation examples and other applications for the Wilson score confidence interval, showing how to use it and also making the reader think of new ways to use this.

Finally, I think this is a nice solution which has been adopted by popular websites (e.g. [Reddit in their comment ranking system](https://possiblywrong.wordpress.com/2011/06/05/reddits-comment-ranking-algorithm/)), but they're other approaches to solve this taking in consideration variables like time to rank things, which it might be more important for different applications (e.g. news that are too old might be not relevant to show in the front of a website), [HackerNews](https://medium.com/hacking-and-gonzo/how-hacker-news-ranking-algorithm-works-1d9b0cf2c08d) and [Reddit](https://medium.com/hacking-and-gonzo/how-reddit-ranking-algorithms-work-ef111e33d0d9) use time as an important variable for ranking their stories, so that posts that are newer have better chances to appear first. Said that, this is not the only solution, and it heavily depends on one's needs.
