Chi-Square Test
================
Maria Nakhoul
16 March 2022

## Summary of the test

The chi-square test is a statistical test used to compare the
relationship between categorical variables. It is a nonparametric test,
which means that the normality assumptions can’t be met. There are 2
types of chi-square tests: 1. chi-square test for goodness of fit 2.
chi-square test for independence

Test for independence is used to determine the relationship among the
categorical variables. Goodness of fit test is used to determine if the
sample we have matches a hypothesized distribution. Inputs are what
distinguish the 2 tests. Goodness of fit takes in a vector of observed
frequencies and a vector of expected proportions (proportions must add
up to 1). Independence takes in 2 vectors of frequencies. The formula
for both the tests is the same.

![](Chi-Squared-Test_files/Chi-square%20test%20formula.png)<!-- -->

In hypothesis testing, the H0 for the chi-square test would be that the
categories are independent and the alternative hypothesis would be that
the categories are dependent.

To run the chi-suqare tests, use the following function.

``` r
table <- rbind(c(84, 46, 122),
             c(3, 6, 12))

rownames(table) <- c("Yes", "No")
colnames(table) <- c("High", "Medium", "Low")

chisq.test(table)
```

    ## 
    ##  Pearson's Chi-squared test
    ## 
    ## data:  table
    ## X-squared = 3.5912, df = 2, p-value = 0.166

If frequencies are less than 5 in any of the inputs, use a fisher’s
exact test

``` r
fisher.test(table)
```

    ## 
    ##  Fisher's Exact Test for Count Data
    ## 
    ## data:  table
    ## p-value = 0.1486
    ## alternative hypothesis: two.sided
