[Think Stats Chapter 3 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2004.html#toc31) (actual vs. biased)

```{python}
# import nsfg module and read in respondent data

import thinkstats2
resp = nsfg.readFemResp()

# create a PMF of the observed number of kids in a household
pmf_actual = thinkstats2.Pmf(resp['numkdhh'], label = "Actual")

# create a copy of the PMF and weight responses based on what you would get if you sampled kids and asked how many children were in their household

bias_pmf = pmf_actual.Copy(label = "Observed")
for x, p in pmf_actual.Items():
    bias_pmf.Mult(x, x)
    bias_pmf.Normalize()   

# plot the distributions
thinkplot.PrePlot(2)
thinkplot.Pmfs([pmf_actual, bias_pmf])
thinkplot.Show(xlabel='number of kids', ylabel='PMF')

# compute the means

pmf_actual.Mean()
bias_pmf.Mean



```
The actual mean of number of kids in a household is ~1.02
The biased mean is ~ 2.4

