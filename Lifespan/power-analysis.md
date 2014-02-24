Power Analysis for Drosophila Lifespan Experiments
====================================================

This analysis was performed by Dave Bridges on ``Tue Apr  2 21:44:34 2013``

The statistical power is the chance that an observation will be detected at a given false positive rate (for these calculations the false positive rate is 0.05).  The power is the same as one minus the false negative rate.  

The relative risk is the probability of an event, in this case death, relative to another group.  See http://en.wikipedia.org/wiki/Relative_risk for more details.


```
## Loading required package: powerSurvEpi
```

The number of samples can be determined either empirically by examining a series of sample sizes compared to the relative risk and statistical power:

![plot of chunk plots](figure/plots.png) 


The sample size can also be calculated for a given deisired relative risk and statistical power:


```r
ssizeCT.default(power = 0.8, k = 1, pE = 1, pC = 1, RR = 1.5, alpha = 0.05)
```

```
## nE nC 
## 99 99
```


References
-----------

```r
citation("powerSurvEpi")
```

```
## 
## To cite package 'powerSurvEpi' in publications use:
## 
##   Weiliang Qiu, Jorge Chavarro, Ross Lazarus, Bernard Rosner and
##   Jing Ma. (2012). powerSurvEpi: Power and sample size calculation
##   for survival analysis of epidemiological studies. R package
##   version 0.0.6. http://CRAN.R-project.org/package=powerSurvEpi
## 
## A BibTeX entry for LaTeX users is
## 
##   @Manual{,
##     title = {powerSurvEpi: Power and sample size calculation for survival analysis of
## epidemiological studies},
##     author = {Weiliang Qiu and Jorge Chavarro and Ross Lazarus and Bernard Rosner and Jing Ma.},
##     year = {2012},
##     note = {R package version 0.0.6},
##     url = {http://CRAN.R-project.org/package=powerSurvEpi},
##   }
## 
## ATTENTION: This citation information has been auto-generated from
## the package DESCRIPTION file and may need manual editing, see
## 'help("citation")' .
```

```r
citation()
```

```
## 
## To cite R in publications use:
## 
##   R Core Team (2013). R: A language and environment for
##   statistical computing. R Foundation for Statistical Computing,
##   Vienna, Austria. ISBN 3-900051-07-0, URL
##   http://www.R-project.org/.
## 
## A BibTeX entry for LaTeX users is
## 
##   @Manual{,
##     title = {R: A Language and Environment for Statistical Computing},
##     author = {{R Core Team}},
##     organization = {R Foundation for Statistical Computing},
##     address = {Vienna, Austria},
##     year = {2013},
##     note = {{ISBN} 3-900051-07-0},
##     url = {http://www.R-project.org/},
##   }
## 
## We have invested a lot of time and effort in creating R, please
## cite it when using it for data analysis. See also
## 'citation("pkgname")' for citing R packages.
```


Session Information
---------------------

```r
sessionInfo()
```

```
## R version 2.15.3 (2013-03-01)
## Platform: x86_64-apple-darwin9.8.0/x86_64 (64-bit)
## 
## locale:
## [1] C/en_US.UTF-8/C/C/C/C
## 
## attached base packages:
## [1] stats     graphics  grDevices utils     datasets  methods   base     
## 
## other attached packages:
## [1] RColorBrewer_1.0-5 powerSurvEpi_0.0.6 knitr_1.1         
## 
## loaded via a namespace (and not attached):
## [1] digest_0.6.3    evaluate_0.4.3  formatR_0.7     splines_2.15.3 
## [5] stringr_0.6.2   survival_2.37-2 tools_2.15.3
```

