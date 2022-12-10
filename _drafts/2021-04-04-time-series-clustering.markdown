---
title: "A way to cluster multiple time series"
date: 2021-04-04 16:15:00
categories: [time-series, clustering]
tags: [statistics, time-series, machine-learning, unsupervised-learning]
---

I like to keep track of things in my life. I mean, not just by eyeballing and organising where each item is placed on my closet, but also recording stuff like personal expense, weight, and step counts. These kind of data are tracked over time and are known as *time series* data. Given multiple time series, there are situations where we might be interested to explore if they share any similarities, e.g., does my exercise routine (i.e., step count) have a similar pattern to my spending? *If it is true, I should contemplate whether those steps were actually me exploring a shopping mall.*

## How to measure the similarity?

While analysing time series data, by default we usually check the autocorrelation and partial autocorrelation of the time series [[1]](https://machinelearningmastery.com/gentle-introduction-autocorrelation-partial-autocorrelation/). However, these approaches only measure the relationship between a data point with the other data points **within the same time series**. Hence, we can't use this when we want to compare different time series.

Another way that we frequently use is computing the **summary statistics** of each time series data, let's say, the mean and standard deviation, then execute any **clustering algorithm**. Despite the simplicity, we might lose important information of the time series data since we're only taking the summary statistics as the input. *Then, how can we do better?*

![The [Datasaurus Dozen](https://www.autodesk.com/research/publications/same-stats-different-graphs)](https://miro.medium.com/max/600/1*W--cGoA3_n2ZlU6Xs4o2iQ.gif)
<center>The <a href='https://www.autodesk.com/research/publications/same-stats-different-graphs'>Datasaurus Dozen</a>; how totally different datasets may share similar mean and standard deviations.</center>

There are several ways to measure the similarity between two time series, such as:

### Euclidean distance

- illustration
- formula
- drawback: one-to-one distance

...

### Dynamic Time Warping

- illustration
- formula
- allows one to many comparison between indices on different time series
- provides warping mechanism
- allow time series averaging via barycenter
- drawback: computational cost

...

## Time series clustering

After computing the similarity measures, we can cluster the time series.

**example image**, e.g., from [tslearn docs](https://tslearn.readthedocs.io/en/stable/auto_examples/clustering/plot_kmeans.html)

- k-means
- hierarchical
- density-based
- self-organising map

Give explanations on how each method works.

## Example Case

Based on k-means clustering with dynamic time warping, use `tslearn` Python package.


## Takeaways

...

Limitations:

- computational complexity
- can't handle multivariate time series. In this case, feature-based time series clustering is recommended (**TO DO: citation; figure out the proper way to extract the time series features**). Can try autoencoders. 

## References

[1] https://machinelearningmastery.com/gentle-introduction-autocorrelation-partial-autocorrelation/

[2] https://multithreaded.stitchfix.com/blog/2016/01/13/market-watch/

[3] ...