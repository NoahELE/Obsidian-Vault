---
date created: Wednesday, May 11th 2022, 12:38:56 pm
date modified: Wednesday, May 25th 2022, 3:57:24 pm
---

# Week 10

## Recommender System

- An online system where many users interact with many items
- Each user has a profile
- User rate items:
    - Explicitly: give a score
    - implicitly: web usage mining; time spent on viewing the item; etc.
- System recommends items

## Item-based Collaborative Filtering

- Measure item similarity:
    - Imputation with their means
    - $sim(i, j) = \frac{1}{1 + d(j, j)}$ where $d(i, j) = \sqrt{\sum (r_{ki} - r_{kj})^2}$
    - Calculate the predicted score by weighted average
        - e.g. $predicted\ a_1\ score = \frac{sim(a_1, a_2) * a_2\ score + sim(a_1, a_3) * a_3\ score}{sim(a_1, a_2) + sim(a_1, a_3)}$

> Pros and Cons:
>
> - items similarities is computed offline, so efficient at runtime
> - suited for situations where number of users is far greater than number of items
> - cold start problem: how to deal with new items

## User-based Collaborative Filtering

mathematically similar with item-based approach

- Item-based performs better in practical cases: movies, books, etc.
- User preference is more dynamic; relatively static for item-based
- Sparsity problem with user based method

## Content-based Recommendation

Feature vector of item:

- Create feature vector from an item's attributes

Feature vector of user

- weighted average of feature vectors of rated items

Recommend item by:

- Similarity based on the feature vectors
- Cosine similarity of item's and user's feature vectors

> - relies on the properties of items, need solid profiles
> - transparency
> - independent from other's ratings
>     - no new-item problem
>     - can recommend unpopular items to user
> - over specification
>     - tends to recommend items similar to those already seen by the users
> - still has new-user problem

> A simple way to measure recommender system is RMSE
