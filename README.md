# Question # 1.

A publishing company has just published a new textbook. Before the company decides the price at which to sell this textbook, it want to know the average price of all such textbooks in the market. The research department at the company took a sample of 25 comparable textbooks and collected information on their prices. This information produced a mean price of $145 for this sample. It is known that the standard deviation of the prices of all such textbooks is $35 and the population of such prices is normal.

A. What is the point of estimate of the mean price all such textbooks?

The point estimate of the mean (xbar) is $145.

B. Construct a 90% confidence interval for the mean price of all such textbooks

A 90% confidence interval produces an alpha of .10, which means we must find the z-score for .05

```{r}
z = round(qnorm(.95),4)
```
Which comes out to be `r z`. 

Since we know the mean is 145 and the standard deviation is 35, we can calculate the margin of error.

```{r}
me = 35/sqrt(25)
me = round((z*me),4)

cipos = round((145 + me),4)
cineg = round((145 - me),4)
cineg
```

We can see that the margin of error is `r me`, which gives us a 90% confidence interval between (`r cineg` and `r cipos`).

#Question # 2

A. According to Mobes Services Inc. an individual checking his/her account at major U.S banks via cellphones cost the banks between $350 and $450. A recent random sample of 600 such checking accounts produced a mean annual cost of $500 to major U.S banks. Assume that the standard deviation of annual costs to major US banks of all such checking account is $40. Make a 99% confidence interval for the current mean annual cost to major banks all such checking account.

The mean (xbar) is 500, the alpha is .005, and the standard deviation is 40.

```{r}
z = round(qnorm(.99),4)

me = 35/sqrt(25)
me = round((z*me),4)

cipos = round((500 + me),4)
cineg = round((500 - me),4)
```

The z-score comes out to `r z`, and we can now find out the margin of error which is `r me`. Thus, the 99% confidence interval is between (`r cineg`, `r cipos`).
