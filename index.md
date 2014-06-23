---
title       : mtcars linear regressions
subtitle    : project for the Developing Data Products course
author      : f. Delgove
job         : 
framework   : io2012        # {io2012, html5slides, shower, dzslides, ...}
highlighter : highlight.js  # {highlight.js, prettify, highlight}
hitheme     : tomorrow      # 
widgets     : []            # {mathjax, quiz, bootstrap}
mode        : selfcontained # {standalone, draft}
knit        : slidify::knit2slides
---

## mtcars linear regressions

**mtcars linear regressions** is a shiny app  
designed to show the result of a linear  
model predicting the number of miles per gallon (mpg).

Selecting one or more predictors will produce  
the summary of the associated linear model.

--- .class #id 

## Exemple
With the variables **wt**, **qsec** and **am** selected   
using the boxes at the left part of the web page,  
the shiny app will produce the formula and present  
the summary of the model.  

---
## Exemple output

```r
summary(lm(mpg ~ wt + qsec + am, data = mtcars))
```

```
## 
## Call:
## lm(formula = mpg ~ wt + qsec + am, data = mtcars)
## 
## Residuals:
##    Min     1Q Median     3Q    Max 
## -3.481 -1.556 -0.726  1.411  4.661 
## 
## Coefficients:
##             Estimate Std. Error t value Pr(>|t|)    
## (Intercept)    9.618      6.960    1.38  0.17792    
## wt            -3.917      0.711   -5.51    7e-06 ***
## qsec           1.226      0.289    4.25  0.00022 ***
## am             2.936      1.411    2.08  0.04672 *  
## ---
## Signif. codes:  0 '***' 0.001 '**' 0.01 '*' 0.05 '.' 0.1 ' ' 1
## 
## Residual standard error: 2.46 on 28 degrees of freedom
## Multiple R-squared:  0.85,	Adjusted R-squared:  0.834 
## F-statistic: 52.7 on 3 and 28 DF,  p-value: 1.21e-11
```


---

## Where ? 
The app is hosted on the Rstudio shiny server  
and can be launched using this link  

https://frounch.shinyapps.io/dataProd

