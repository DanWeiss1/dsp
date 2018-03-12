[Think Stats Chapter 4 Exercise 2](http://greenteapress.com/thinkstats2/html/thinkstats2005.html#sec46) (random_dist)

```{python}
# import numpy and thinkstats2 modules

import numpy as np
import thinkstats2 as ts2

# generate random uniform array of 1000

a = np.random.random(1000,)

# plot the pmf

pmf = ts2.Pmf(a)
thinkplot.Pmf(pmf)

# plot the cdf

cdf = ts2.Cdf(a)
thinkplot.Cdf(cdf)

```

The array appears to be randomly distributed between 0 and 1