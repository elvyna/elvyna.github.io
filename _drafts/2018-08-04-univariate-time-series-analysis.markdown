---
title:  "Univariate Time Series Analysis"
date:   2018-08-04 23:16:23
categories: [jekyll]
tags: [jekyll]
---

```{text}
Que será, será
Whatever will be, will be
The future's not ours to see
Que será, será
What will be, will be
```

This song reminds me of growing up - not necessarily because this song was featured in an Indonesian TV commercial. As human being, we sometimes wish that we knew what would happen in the future; so that we can take the right action on current time. At the time of this writing, there are already some researches that evaluate feasibility of time traveling, but the realization is yet to come. Although we might not be able to see the future, there are some statistical methods to *estimate* what will happen in the future. Aside of the conventional statistical methods, there are some implementation of machine learning algorithms to handle this problem.

On this post, we will use [Wikipedia] as sample case. Based on its historical page traffic, we'll try to forecast number of traffic on the future. It is useful for the company to plan and prepare their site infrastructure specification - so the site can be accessed although the traffic is huge.

Since the observation is single variable, it is categorized as univariate time series. We will use some methods on this analysis - you can view the code [here](https://github.com/elvyna/data-analysis/tree/master/jupyter-notebook). Prior to forecasting, we should understand characteristics of the data.


## Time Series Decomposition

Prior to deciding which forecasting method can be used, we should observe the characteristics of data. Basically, time series data can be decomposed into several components:

1. Trend
2. Seasonality
3. Residual



## Simple Moving Average

This is the simplest method: we will take the arithmetic mean of some values and use it as estimation of future data.

$$
MA_t = \frac{x_t + x_{t-1} + ... + x_{t-N+1}}{N}
$$

For example, we calculate moving average of two data points.

|    Date    | Page View | Moving Avg |
|:----------:|:---------:|:----------:|
| 2015-07-01 |  84712190 |            |
| 2015-07-02 |  84438545 | 84575367.5 |
| 2015-07-03 |  80167728 | 82303136.5 |
| 2015-07-04 |  83463204 |   81815466 |

*insert plot here*

Despite its simplicity, moving average has some disadvantages:
- it is only useful when there are no trends on the series
- all past observations have equal weight

## Exponential Smoothing

...

## Auto Regressive Integrated Moving Average

...

## Long-Short Term Memory (LSTM)

...


# Defaults

You’ll find this post in your `_posts` directory. Go ahead and edit it and re-build the site to see your changes. You can rebuild the site in many different ways, but the most common way is to run `jekyll serve --watch`, which launches a web server and auto-regenerates your site when a file is updated.

Jekyll also offers powerful support for code snippets:

``` ruby
def print_hi(name)
  puts "Hi, #{name}"
end
print_hi('Tom')
#=> prints 'Hi, Tom' to STDOUT.
```

Check out the [Jekyll docs][jekyll] for more info on how to get the most out of Jekyll. File all bugs/feature requests at [Jekyll’s GitHub repo][jekyll-gh]. If you have questions, you can ask them on [Jekyll’s dedicated Help repository][jekyll-help].

[jekyll]:      http://jekyllrb.com
[jekyll-gh]:   https://github.com/jekyll/jekyll
[jekyll-help]: https://github.com/jekyll/jekyll-help
[Wikipedia]: http://wikipedia.org