[Think Stats Chapter 5 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2006.html#toc50) (blue men)

```{python}

# import scipy.stats norm module

from scipy.stats import norm

# create function to convert heights to cm from feet and inches
def heightToCM(ft, inch):
    return (ft * 12 + inch) * 2.54

norm.cdf(heightToCM(ft = 6, inch = 1), loc = 178, scale = 7.7) - norm.cdf(heightToCM(ft =5 , inch = 10), loc = 178, scale = 7.7)
```

Approximately 34.3% of males are in the range of heights accepted by the blue man group
