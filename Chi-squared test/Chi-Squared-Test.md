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

\[\chi^2 = \sum \frac {(O - E)^2}{E}\]

Load Libaries

``` r
library(dplyr)
```

    ## Warning: package 'dplyr' was built under R version 3.6.2

    ## Registered S3 methods overwritten by 'tibble':
    ##   method     from  
    ##   format.tbl pillar
    ##   print.tbl  pillar

    ## 
    ## Attaching package: 'dplyr'

    ## The following objects are masked from 'package:stats':
    ## 
    ##     filter, lag

    ## The following objects are masked from 'package:base':
    ## 
    ##     intersect, setdiff, setequal, union

``` r
library(ggpubr)
```

    ## Loading required package: ggplot2

    ## Loading required package: magrittr

## R Markdown

This is an R Markdown document. Markdown is a simple formatting syntax
for authoring HTML, PDF, and MS Word documents. For more details on
using R Markdown see <http://rmarkdown.rstudio.com>.

When you click the **Knit** button a document will be generated that
includes both content as well as the output of any embedded R code
chunks within the document. You can embed an R code chunk like this:

``` r
summary(cars)
```

    ##      speed           dist       
    ##  Min.   : 4.0   Min.   :  2.00  
    ##  1st Qu.:12.0   1st Qu.: 26.00  
    ##  Median :15.0   Median : 36.00  
    ##  Mean   :15.4   Mean   : 42.98  
    ##  3rd Qu.:19.0   3rd Qu.: 56.00  
    ##  Max.   :25.0   Max.   :120.00

## Including Plots

You can also embed plots, for example:

![](Chi-Squared-Test_files/figure-gfm/pressure-1.png)<!-- -->

Note that the `echo = FALSE` parameter was added to the code chunk to
prevent printing of the R code that generated the plot.
