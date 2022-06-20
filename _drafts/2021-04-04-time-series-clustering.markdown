---
title: "A way to cluster multiple time series"
date: 2021-04-04 16:15:00
categories: [time-series, clustering]
tags: [statistics, time-series, machine-learning, unsupervised-learning]
---

I like to keep track of things on my daily life. I mean, not just by eyeballing and organising where each item is placed on my closet, but also recording stuff like personal expense, weight, and step counts (well, as long as I have a fully-functioned smart band). These data are tracked over time and are called *time series* data. Given multiple time series, we can check their similarities, for example, does my exercise routine (i.e., step count) have a similar pattern to my spending? *If it is true, I should reflect and check if I usually kill my time walking at a shopping mall.*

## How to measure the similarity?

While analysing time series data, by default we usually check the autocorrelation and partial autocorrelation of the time series [[1]](https://machinelearningmastery.com/gentle-introduction-autocorrelation-partial-autocorrelation/). However, these approaches only measure the relationship between a data point with the other data points **within the same time series**. Hence, we can't use this when we want to compare different time series.

Another way that we frequently use is computing the summary statistics of each time series data, let's say, the mean and standard deviation, then execute any clustering algorithm. While this approach is not wrong (there are many ways to Rome!), we might lose important characteristics of the time series data since we're only taking the summary statistics as the input. *Then, how can we do better?*

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

...

## Time series clustering

Given the similarity measures, we can do clustering based on them.

**example image**, e.g., from [tslearn docs](https://tslearn.readthedocs.io/en/stable/auto_examples/clustering/plot_kmeans.html)

- k-means
- hierarchical
- density-based
- self-organising map

Give explanations on how each method works.

## Example Case

Based on k-means clustering with dynamic time warping, use `tslearn` Python package.


## Takeaways

...s

## References

[1] https://machinelearningmastery.com/gentle-introduction-autocorrelation-partial-autocorrelation/

[2] https://multithreaded.stitchfix.com/blog/2016/01/13/market-watch/

[3] ...