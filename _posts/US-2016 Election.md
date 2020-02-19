---
title: "US 2016 Election Analysis"
date: 2018-06-12
tags: [data wrangling, data visualization, prediction, R]
header:
  image: "/images/perceptron/percept.jpg"
excerpt: "data wrangling, data visualization, prediction, R"
mathjax: "true"
---

# Background

## What makes predicting voter behavior (and thus election forecasting) a hard problem?

Many reasons may lead to the difficulty of predicting the voter behavior and election forecasting. The first one may be the number of voters for the
2016’s polls. While we were expecting that the equal number of Democrats and Republicians, it turned out that the Republican voters were much
higher than the Democratic voters.The second reason may be the decision changing for the voters. It depended on whether or not the voter is a
minority, and the income earned, and the gender. We should analysis all the factor that may influence an individual’s vote. Also,it turned out that
many voters changed their vote in the week that leads up to voting. And the last reason may be the unpredictable future events that will happen.
The society may change their attitude due to the news they’ve found on the TV or website, which is not predcitable.

# Visualization

```r
states = map_data("state")

ggplot(data = states) + 
  geom_polygon(aes(x = long, y = lat, fill = region, group = group), color = "white") + 
  coord_fixed(1.3) +
  guides(fill=FALSE)  # color legend is unnecessary and takes too long
```

```r
counties = map_data("county")

ggplot(data = counties)+
  geom_polygon(aes(x = long, y = lat, fill = region, group = group), color = "white") + 
  coord_fixed(1.3) +
  guides(fill=FALSE)  # color legend is unnecessary and takes too long
```