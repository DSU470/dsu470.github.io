---
title       : shinyCarsApp
subtitle    : Exploring data has never been this easy
author      : DSU470
job         : Analyst
framework   : io2012        # {io2012, html5slides, shower, dzslides, ...}
highlighter : highlight.js  # {highlight.js, prettify, highlight}
hitheme     : tomorrow      # 
widgets     : []            # {mathjax, quiz, bootstrap}
mode        : selfcontained # {standalone, draft}
knit        : slidify::knit2slides
---

## shinyCarsApp: exploring data made easy

And now for something completely different: a shiny app that allows the user to explore data about various aspects of cars, shinyCarsApp!

With shinyCars, it is easy to show:

1. Plain data
2. Some summary statistics
3. Show plots!

Please allow us to introduce shinyCarsApp!

--- .class #id 

## Data set
- We could simply show the first 3 rows of the dataset

```r
head(mtcars, 3)
```

```
##                mpg cyl disp  hp drat    wt  qsec vs am gear carb
## Mazda RX4     21.0   6  160 110 3.90 2.620 16.46  0  1    4    4
## Mazda RX4 Wag 21.0   6  160 110 3.90 2.875 17.02  0  1    4    4
## Datsun 710    22.8   4  108  93 3.85 2.320 18.61  1  1    4    1
```

--- .class #id

## Showing plots

- Alternatively, we could show some descriptive summary of the data


```r
library(ggplot2)
qplot(hp,mpg,data=mtcars,xlab="Engine power (hp)",ylab="Miles per gallon",
      main="Regression of mpg (outcome) and engine power(input) by number of cylinders", 
      geom=c("point","smooth"),method="lm",facets=.~cyl)
```

![plot of chunk qplot](assets/fig/qplot.png) 

--- .class #id

## Conclusion

shinyCarsApp is:

- easy to use
- runs from a server, run anytime anywhere on any device
- free of charge
- always up to date

Thanks for your time!
