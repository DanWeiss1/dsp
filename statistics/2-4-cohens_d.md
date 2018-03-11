[Think Stats Chapter 2 Exercise 4](http://greenteapress.com/thinkstats2/html/thinkstats2003.html#toc24) (Cohen's d)

```{python}
# read in nsfg data and split into first and not first pregnancies
import nsfg
preg = nsfg.ReadFemPreg
firsts = preg[preg['pregordr'] ==1]
other = preg[preg['pregordr'] != 1]
# calculate mean for totalweight_lb of first babies and other babies
mean1, mean2 = firsts['totalwgt_lb'].mean(), other['totalwgt_lb'].mean()

# caluclate difference in means
meandif = mean1 - mean2
# calculate variance of weight of first and non first babies
var1, var2 =  firsts['totalwgt_lb'].var(), other['totalwgt_lb'].var()

# get numbers of first and non first babies in the data
n1, n2 = len(firsts['totalwgt_lb']), len(other['totalwgt_lb'])

# get pooled sd
pooledSD = (n1 * var1 + n2 * var2) / (n1 + n2)

# calculate and print Cohen's D
cohensD = meandif/pooledSD
print(cohensD)
```

First babies are slightly smaller than others with an effect size of ~0.5