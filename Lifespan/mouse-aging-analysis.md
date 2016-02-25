# Aging Analysis of Mck-TSC1
Dave Bridges, Kaleigh Fisher and Binbin Lu  
February 9, 2015  



# Data Entry

These data are accumulated from the database.  The analysis includes all alive animals, animals which were sacrificed and animals which died of natural causes (denoted in the database as "Unknown").  Animals which died with an estimated death date are excluded from the analysis.  We are testing the effects of age on death by natural causes.  This script is located in /Users/davebridges/Documents/Source/DrosophilaMuscleFunction/Lifespan and was most recently run on Wed Feb 17 16:46:06 2016.


# Mck-TSC1 Mice

```
## [1] 292
```

## Analysis

The data is saved in /Users/davebridges/Documents/Source/DrosophilaMuscleFunction/Lifespan with the data saved as ../Data/Mouse Log.csv and analysed using R \cite{base}.
The data was analysed using the survival package \cite{survival1, survival2}.  Log rank tests were performed using the coin package \cite{coin1, coin2}.
This plot analyses all of the natural deaths (marked in the database as unknown).  The median age at death was 272.5 for knockout mice and 623 for control mice

![](mouse-aging-analysis_files/figure-html/data-analysis-all-1.png) 
This analysis contains a total of **625** animals, from which we have detected **49** natural deaths.  See Table below for a summary of natural deaths and see the figure below for the combined death curves with errors.

## Comparing all Four Genotypes
This analysis looks at all four genotypes for *Ckmm-Tsc1*.


```
## 
## 	Asymptotic K-Sample Logrank Test
## 
## data:  survobj.mck by
## 	 Genotype (fl/fl; Tg/+, +/+; +/+, +/+; Tg/+, fl/fl; +/+)
## chi-squared = 16, df = 3, p-value = 0.0011
```

The chi-squared test for comparing all four genotypes is significant, with a p-value of 0.00009.  The results of these tests are in the table below.  The effects of each genotype, relative to the knockout strains are in Table \ref{tab:mck-coef}. These data are visualised in the figure.  This means that the knockout mice are 3.66749 to 5.34657 times more likely to die at any given time, depending on the strain.


Table: Muscle TSC1 Knockout Tests

                         test   df     pvalue
----------------------  -----  ---  ---------
Likelihood ratio test      19    3   0.000322
Wald test                  18    3   0.000348
Score (logrank) test       21    3   0.000088



Table: Muscle TSC1 Knockout Coefficients, relative to Knockout

                        beta      se    2.5 %   97.5 %          p
-------------------  -------  ------  -------  -------  ---------
Genotype+/+; +/+      -1.676   0.187   -2.648   -0.705   0.000719
Genotype+/+; Tg/+     -1.459   0.232   -2.477   -0.440   0.004996
Genotypefl/fl; +/+    -1.300   0.273   -2.038   -0.561   0.000565

# Comparing Floxed to Knockout
This section only compares fl/fl;+/+ to fl/fl;Tg/+.


The chi-squared test for comparing the two genotypes is significant, with a p-value of 0.00152.  The results of these tests are in the table below.  The effects of each genotype, relative to the knockout strains are in the table below. These results are presented graphically in the figure below.  This means that the knockout mice are 3.27717 times more likely to die at any given time.


Table: Muscle TSC1 Knockout Tests (WT vs KO)

                         test   df   pvalue
----------------------  -----  ---  -------
Likelihood ratio test      10    1   0.0015
Wald test                   9    1   0.0026
Score (logrank) test       10    1   0.0015



Table: Muscle TSC1 Knockout Coefficients, relative to Knockout

                        beta      se    2.5 %   97.5 %        p
-------------------  -------  ------  -------  -------  -------
Genotypefl/fl; +/+    -1.187   0.305   -1.959   -0.415   0.0026

# Death Logs
This table shows the age, and at risk individuals for each natural death, along with the \% survival and the confidence intervals.

 time   n.risk   n.event   n.censor      surv   std.err     upper     lower  strata               
-----  -------  --------  ---------  --------  --------  --------  --------  ---------------------
   10      188         1          0   0.99468   0.00533   1.00000   0.98434  Genotype=fl/fl; Tg/+ 
   17      187         0          3   0.99468   0.00533   1.00000   0.98434  Genotype=fl/fl; Tg/+ 
   18      184         1          7   0.98927   0.00763   1.00000   0.97460  Genotype=fl/fl; Tg/+ 
   19      176         0          1   0.98927   0.00763   1.00000   0.97460  Genotype=fl/fl; Tg/+ 
   21      175         0          3   0.98927   0.00763   1.00000   0.97460  Genotype=fl/fl; Tg/+ 
   22      172         0          1   0.98927   0.00763   1.00000   0.97460  Genotype=fl/fl; Tg/+ 
   28      171         0          2   0.98927   0.00763   1.00000   0.97460  Genotype=fl/fl; Tg/+ 
   30      169         0          1   0.98927   0.00763   1.00000   0.97460  Genotype=fl/fl; Tg/+ 
   31      168         0          2   0.98927   0.00763   1.00000   0.97460  Genotype=fl/fl; Tg/+ 
   33      166         0          1   0.98927   0.00763   1.00000   0.97460  Genotype=fl/fl; Tg/+ 
   34      165         0          1   0.98927   0.00763   1.00000   0.97460  Genotype=fl/fl; Tg/+ 
   41      164         0          3   0.98927   0.00763   1.00000   0.97460  Genotype=fl/fl; Tg/+ 
   42      161         0          3   0.98927   0.00763   1.00000   0.97460  Genotype=fl/fl; Tg/+ 
   43      158         0          1   0.98927   0.00763   1.00000   0.97460  Genotype=fl/fl; Tg/+ 
   48      157         0          2   0.98927   0.00763   1.00000   0.97460  Genotype=fl/fl; Tg/+ 
   50      155         0          1   0.98927   0.00763   1.00000   0.97460  Genotype=fl/fl; Tg/+ 
   58      154         0          1   0.98927   0.00763   1.00000   0.97460  Genotype=fl/fl; Tg/+ 
   60      153         0          1   0.98927   0.00763   1.00000   0.97460  Genotype=fl/fl; Tg/+ 
   62      152         0          2   0.98927   0.00763   1.00000   0.97460  Genotype=fl/fl; Tg/+ 
   63      150         0          3   0.98927   0.00763   1.00000   0.97460  Genotype=fl/fl; Tg/+ 
   64      147         0          1   0.98927   0.00763   1.00000   0.97460  Genotype=fl/fl; Tg/+ 
   69      146         0          1   0.98927   0.00763   1.00000   0.97460  Genotype=fl/fl; Tg/+ 
   71      145         1          0   0.98245   0.01030   1.00000   0.96282  Genotype=fl/fl; Tg/+ 
   78      144         0          2   0.98245   0.01030   1.00000   0.96282  Genotype=fl/fl; Tg/+ 
   85      142         0          2   0.98245   0.01030   1.00000   0.96282  Genotype=fl/fl; Tg/+ 
   89      140         0          2   0.98245   0.01030   1.00000   0.96282  Genotype=fl/fl; Tg/+ 
  102      138         0          2   0.98245   0.01030   1.00000   0.96282  Genotype=fl/fl; Tg/+ 
  103      136         0          3   0.98245   0.01030   1.00000   0.96282  Genotype=fl/fl; Tg/+ 
  108      133         0          4   0.98245   0.01030   1.00000   0.96282  Genotype=fl/fl; Tg/+ 
  110      129         1          0   0.97484   0.01291   0.99981   0.95048  Genotype=fl/fl; Tg/+ 
  111      128         0          1   0.97484   0.01291   0.99981   0.95048  Genotype=fl/fl; Tg/+ 
  112      127         0          1   0.97484   0.01291   0.99981   0.95048  Genotype=fl/fl; Tg/+ 
  114      126         1          0   0.96710   0.01517   0.99628   0.93877  Genotype=fl/fl; Tg/+ 
  123      125         0          1   0.96710   0.01517   0.99628   0.93877  Genotype=fl/fl; Tg/+ 
  124      124         0          3   0.96710   0.01517   0.99628   0.93877  Genotype=fl/fl; Tg/+ 
  125      121         1          0   0.95911   0.01729   0.99217   0.92715  Genotype=fl/fl; Tg/+ 
  130      120         0          1   0.95911   0.01729   0.99217   0.92715  Genotype=fl/fl; Tg/+ 
  132      119         0          6   0.95911   0.01729   0.99217   0.92715  Genotype=fl/fl; Tg/+ 
  137      113         0          1   0.95911   0.01729   0.99217   0.92715  Genotype=fl/fl; Tg/+ 
  138      112         1          0   0.95054   0.01948   0.98753   0.91494  Genotype=fl/fl; Tg/+ 
  147      111         0          1   0.95054   0.01948   0.98753   0.91494  Genotype=fl/fl; Tg/+ 
  148      110         0          3   0.95054   0.01948   0.98753   0.91494  Genotype=fl/fl; Tg/+ 
  150      107         0          3   0.95054   0.01948   0.98753   0.91494  Genotype=fl/fl; Tg/+ 
  153      104         0          2   0.95054   0.01948   0.98753   0.91494  Genotype=fl/fl; Tg/+ 
  160      102         0          3   0.95054   0.01948   0.98753   0.91494  Genotype=fl/fl; Tg/+ 
  164       99         0          2   0.95054   0.01948   0.98753   0.91494  Genotype=fl/fl; Tg/+ 
  172       97         0          4   0.95054   0.01948   0.98753   0.91494  Genotype=fl/fl; Tg/+ 
  174       93         0          1   0.95054   0.01948   0.98753   0.91494  Genotype=fl/fl; Tg/+ 
  177       92         0          6   0.95054   0.01948   0.98753   0.91494  Genotype=fl/fl; Tg/+ 
  180       86         1          3   0.93949   0.02272   0.98227   0.89857  Genotype=fl/fl; Tg/+ 
  182       82         1          0   0.92803   0.02582   0.97621   0.88224  Genotype=fl/fl; Tg/+ 
  191       81         0          2   0.92803   0.02582   0.97621   0.88224  Genotype=fl/fl; Tg/+ 
  195       79         0          1   0.92803   0.02582   0.97621   0.88224  Genotype=fl/fl; Tg/+ 
  196       78         0          1   0.92803   0.02582   0.97621   0.88224  Genotype=fl/fl; Tg/+ 
  200       77         0          4   0.92803   0.02582   0.97621   0.88224  Genotype=fl/fl; Tg/+ 
  202       73         0          3   0.92803   0.02582   0.97621   0.88224  Genotype=fl/fl; Tg/+ 
  204       70         0          3   0.92803   0.02582   0.97621   0.88224  Genotype=fl/fl; Tg/+ 
  209       67         0          3   0.92803   0.02582   0.97621   0.88224  Genotype=fl/fl; Tg/+ 
  216       64         0          1   0.92803   0.02582   0.97621   0.88224  Genotype=fl/fl; Tg/+ 
  221       63         0          1   0.92803   0.02582   0.97621   0.88224  Genotype=fl/fl; Tg/+ 
  225       62         0          3   0.92803   0.02582   0.97621   0.88224  Genotype=fl/fl; Tg/+ 
  243       59         0          1   0.92803   0.02582   0.97621   0.88224  Genotype=fl/fl; Tg/+ 
  244       58         1          0   0.91203   0.03113   0.96942   0.85805  Genotype=fl/fl; Tg/+ 
  245       57         0          1   0.91203   0.03113   0.96942   0.85805  Genotype=fl/fl; Tg/+ 
  248       56         0          1   0.91203   0.03113   0.96942   0.85805  Genotype=fl/fl; Tg/+ 
  251       55         0          1   0.91203   0.03113   0.96942   0.85805  Genotype=fl/fl; Tg/+ 
  256       54         0          2   0.91203   0.03113   0.96942   0.85805  Genotype=fl/fl; Tg/+ 
  257       52         0          1   0.91203   0.03113   0.96942   0.85805  Genotype=fl/fl; Tg/+ 
  261       51         0          2   0.91203   0.03113   0.96942   0.85805  Genotype=fl/fl; Tg/+ 
  264       49         1          0   0.89342   0.03734   0.96126   0.83037  Genotype=fl/fl; Tg/+ 
  266       48         0          3   0.89342   0.03734   0.96126   0.83037  Genotype=fl/fl; Tg/+ 
  267       45         0          1   0.89342   0.03734   0.96126   0.83037  Genotype=fl/fl; Tg/+ 
  270       44         0          1   0.89342   0.03734   0.96126   0.83037  Genotype=fl/fl; Tg/+ 
  273       43         0          2   0.89342   0.03734   0.96126   0.83037  Genotype=fl/fl; Tg/+ 
  276       41         0          1   0.89342   0.03734   0.96126   0.83037  Genotype=fl/fl; Tg/+ 
  280       40         0          2   0.89342   0.03734   0.96126   0.83037  Genotype=fl/fl; Tg/+ 
  281       38         1          0   0.86991   0.04589   0.95177   0.79509  Genotype=fl/fl; Tg/+ 
  283       37         0          1   0.86991   0.04589   0.95177   0.79509  Genotype=fl/fl; Tg/+ 
  287       36         0          1   0.86991   0.04589   0.95177   0.79509  Genotype=fl/fl; Tg/+ 
  292       35         1          0   0.84505   0.05428   0.93991   0.75977  Genotype=fl/fl; Tg/+ 
  296       34         0          1   0.84505   0.05428   0.93991   0.75977  Genotype=fl/fl; Tg/+ 
  297       33         0          1   0.84505   0.05428   0.93991   0.75977  Genotype=fl/fl; Tg/+ 
  299       32         0          1   0.84505   0.05428   0.93991   0.75977  Genotype=fl/fl; Tg/+ 
  308       31         0          1   0.84505   0.05428   0.93991   0.75977  Genotype=fl/fl; Tg/+ 
  309       30         1          0   0.81689   0.06400   0.92605   0.72059  Genotype=fl/fl; Tg/+ 
  310       29         0          2   0.81689   0.06400   0.92605   0.72059  Genotype=fl/fl; Tg/+ 
  313       27         0          2   0.81689   0.06400   0.92605   0.72059  Genotype=fl/fl; Tg/+ 
  314       25         0          1   0.81689   0.06400   0.92605   0.72059  Genotype=fl/fl; Tg/+ 
  316       24         1          1   0.78285   0.07686   0.91012   0.67338  Genotype=fl/fl; Tg/+ 
  317       22         0          1   0.78285   0.07686   0.91012   0.67338  Genotype=fl/fl; Tg/+ 
  318       21         0          1   0.78285   0.07686   0.91012   0.67338  Genotype=fl/fl; Tg/+ 
  319       20         0          1   0.78285   0.07686   0.91012   0.67338  Genotype=fl/fl; Tg/+ 
  320       19         0          1   0.78285   0.07686   0.91012   0.67338  Genotype=fl/fl; Tg/+ 
  323       18         0          1   0.78285   0.07686   0.91012   0.67338  Genotype=fl/fl; Tg/+ 
  324       17         0          1   0.78285   0.07686   0.91012   0.67338  Genotype=fl/fl; Tg/+ 
  338       16         0          1   0.78285   0.07686   0.91012   0.67338  Genotype=fl/fl; Tg/+ 
  343       15         0          1   0.78285   0.07686   0.91012   0.67338  Genotype=fl/fl; Tg/+ 
  352       14         0          1   0.78285   0.07686   0.91012   0.67338  Genotype=fl/fl; Tg/+ 
  371       13         1          0   0.72263   0.11098   0.89822   0.58136  Genotype=fl/fl; Tg/+ 
  375       12         0          2   0.72263   0.11098   0.89822   0.58136  Genotype=fl/fl; Tg/+ 
  396       10         0          1   0.72263   0.11098   0.89822   0.58136  Genotype=fl/fl; Tg/+ 
  411        9         0          1   0.72263   0.11098   0.89822   0.58136  Genotype=fl/fl; Tg/+ 
  452        8         1          0   0.63230   0.17371   0.88876   0.44985  Genotype=fl/fl; Tg/+ 
  586        7         1          0   0.54197   0.23234   0.85457   0.34372  Genotype=fl/fl; Tg/+ 
  595        6         1          0   0.45164   0.29549   0.80598   0.25309  Genotype=fl/fl; Tg/+ 
  601        5         1          0   0.36131   0.37056   0.74698   0.17477  Genotype=fl/fl; Tg/+ 
  635        4         0          1   0.36131   0.37056   0.74698   0.17477  Genotype=fl/fl; Tg/+ 
  638        3         1          1   0.24088   0.55135   0.70975   0.08175  Genotype=fl/fl; Tg/+ 
  832        1         1          0   0.00000       Inf        NA        NA  Genotype=fl/fl; Tg/+ 
   15      125         0          5   1.00000   0.00000   1.00000   1.00000  Genotype=+/+; +/+    
   16      120         0          5   1.00000   0.00000   1.00000   1.00000  Genotype=+/+; +/+    
   17      115         0          2   1.00000   0.00000   1.00000   1.00000  Genotype=+/+; +/+    
   18      113         0         12   1.00000   0.00000   1.00000   1.00000  Genotype=+/+; +/+    
   19      101         0          3   1.00000   0.00000   1.00000   1.00000  Genotype=+/+; +/+    
   20       98         1          6   0.98980   0.01026   1.00000   0.97010  Genotype=+/+; +/+    
   21       91         0          3   0.98980   0.01026   1.00000   0.97010  Genotype=+/+; +/+    
   22       88         0          7   0.98980   0.01026   1.00000   0.97010  Genotype=+/+; +/+    
   24       81         0          1   0.98980   0.01026   1.00000   0.97010  Genotype=+/+; +/+    
   28       80         0          1   0.98980   0.01026   1.00000   0.97010  Genotype=+/+; +/+    
   30       79         0          1   0.98980   0.01026   1.00000   0.97010  Genotype=+/+; +/+    
   31       78         0          2   0.98980   0.01026   1.00000   0.97010  Genotype=+/+; +/+    
   32       76         0          2   0.98980   0.01026   1.00000   0.97010  Genotype=+/+; +/+    
   34       74         0          1   0.98980   0.01026   1.00000   0.97010  Genotype=+/+; +/+    
   38       73         0          2   0.98980   0.01026   1.00000   0.97010  Genotype=+/+; +/+    
   41       71         0          1   0.98980   0.01026   1.00000   0.97010  Genotype=+/+; +/+    
   43       70         0          1   0.98980   0.01026   1.00000   0.97010  Genotype=+/+; +/+    
   49       69         0          1   0.98980   0.01026   1.00000   0.97010  Genotype=+/+; +/+    
   50       68         0          2   0.98980   0.01026   1.00000   0.97010  Genotype=+/+; +/+    
   70       66         0          2   0.98980   0.01026   1.00000   0.97010  Genotype=+/+; +/+    
   86       64         0          1   0.98980   0.01026   1.00000   0.97010  Genotype=+/+; +/+    
  100       63         0          2   0.98980   0.01026   1.00000   0.97010  Genotype=+/+; +/+    
  103       61         0          1   0.98980   0.01026   1.00000   0.97010  Genotype=+/+; +/+    
  112       60         0          2   0.98980   0.01026   1.00000   0.97010  Genotype=+/+; +/+    
  138       58         0          1   0.98980   0.01026   1.00000   0.97010  Genotype=+/+; +/+    
  143       57         0          1   0.98980   0.01026   1.00000   0.97010  Genotype=+/+; +/+    
  156       56         0          1   0.98980   0.01026   1.00000   0.97010  Genotype=+/+; +/+    
  170       55         0          1   0.98980   0.01026   1.00000   0.97010  Genotype=+/+; +/+    
  193       54         0          1   0.98980   0.01026   1.00000   0.97010  Genotype=+/+; +/+    
  195       53         0          3   0.98980   0.01026   1.00000   0.97010  Genotype=+/+; +/+    
  198       50         0          1   0.98980   0.01026   1.00000   0.97010  Genotype=+/+; +/+    
  206       49         0          1   0.98980   0.01026   1.00000   0.97010  Genotype=+/+; +/+    
  216       48         0          1   0.98980   0.01026   1.00000   0.97010  Genotype=+/+; +/+    
  217       47         0          1   0.98980   0.01026   1.00000   0.97010  Genotype=+/+; +/+    
  225       46         0          1   0.98980   0.01026   1.00000   0.97010  Genotype=+/+; +/+    
  247       45         0          1   0.98980   0.01026   1.00000   0.97010  Genotype=+/+; +/+    
  251       44         0          1   0.98980   0.01026   1.00000   0.97010  Genotype=+/+; +/+    
  254       43         0          1   0.98980   0.01026   1.00000   0.97010  Genotype=+/+; +/+    
  259       42         0          2   0.98980   0.01026   1.00000   0.97010  Genotype=+/+; +/+    
  261       40         0          1   0.98980   0.01026   1.00000   0.97010  Genotype=+/+; +/+    
  262       39         0          2   0.98980   0.01026   1.00000   0.97010  Genotype=+/+; +/+    
  263       37         0          1   0.98980   0.01026   1.00000   0.97010  Genotype=+/+; +/+    
  266       36         0          2   0.98980   0.01026   1.00000   0.97010  Genotype=+/+; +/+    
  267       34         0          1   0.98980   0.01026   1.00000   0.97010  Genotype=+/+; +/+    
  268       33         0          2   0.98980   0.01026   1.00000   0.97010  Genotype=+/+; +/+    
  273       31         0          1   0.98980   0.01026   1.00000   0.97010  Genotype=+/+; +/+    
  276       30         0          2   0.98980   0.01026   1.00000   0.97010  Genotype=+/+; +/+    
  280       28         0          1   0.98980   0.01026   1.00000   0.97010  Genotype=+/+; +/+    
  283       27         0          1   0.98980   0.01026   1.00000   0.97010  Genotype=+/+; +/+    
  284       26         0          1   0.98980   0.01026   1.00000   0.97010  Genotype=+/+; +/+    
  286       25         0          2   0.98980   0.01026   1.00000   0.97010  Genotype=+/+; +/+    
  296       23         0          3   0.98980   0.01026   1.00000   0.97010  Genotype=+/+; +/+    
  306       20         0          1   0.98980   0.01026   1.00000   0.97010  Genotype=+/+; +/+    
  312       19         0          1   0.98980   0.01026   1.00000   0.97010  Genotype=+/+; +/+    
  313       18         0          1   0.98980   0.01026   1.00000   0.97010  Genotype=+/+; +/+    
  317       17         0          1   0.98980   0.01026   1.00000   0.97010  Genotype=+/+; +/+    
  320       16         0          1   0.98980   0.01026   1.00000   0.97010  Genotype=+/+; +/+    
  325       15         0          1   0.98980   0.01026   1.00000   0.97010  Genotype=+/+; +/+    
  343       14         0          1   0.98980   0.01026   1.00000   0.97010  Genotype=+/+; +/+    
  365       13         0          1   0.98980   0.01026   1.00000   0.97010  Genotype=+/+; +/+    
  368       12         0          1   0.98980   0.01026   1.00000   0.97010  Genotype=+/+; +/+    
  372       11         0          2   0.98980   0.01026   1.00000   0.97010  Genotype=+/+; +/+    
  396        9         0          3   0.98980   0.01026   1.00000   0.97010  Genotype=+/+; +/+    
  642        6         1          0   0.82483   0.18286   1.00000   0.57638  Genotype=+/+; +/+    
  665        5         1          0   0.65986   0.28886   1.00000   0.37461  Genotype=+/+; +/+    
  678        4         1          0   0.49490   0.40838   1.00000   0.22228  Genotype=+/+; +/+    
  857        3         1          0   0.32993   0.57744   1.00000   0.10639  Genotype=+/+; +/+    
  885        2         1          0   0.16497   0.91293   0.98737   0.02756  Genotype=+/+; +/+    
  938        1         1          0   0.00000       Inf        NA        NA  Genotype=+/+; +/+    
   14      104         0          1   1.00000   0.00000   1.00000   1.00000  Genotype=+/+; Tg/+   
   16      103         0          4   1.00000   0.00000   1.00000   1.00000  Genotype=+/+; Tg/+   
   17       99         0          3   1.00000   0.00000   1.00000   1.00000  Genotype=+/+; Tg/+   
   18       96         0          6   1.00000   0.00000   1.00000   1.00000  Genotype=+/+; Tg/+   
   19       90         0          2   1.00000   0.00000   1.00000   1.00000  Genotype=+/+; Tg/+   
   20       88         0          5   1.00000   0.00000   1.00000   1.00000  Genotype=+/+; Tg/+   
   21       83         0          6   1.00000   0.00000   1.00000   1.00000  Genotype=+/+; Tg/+   
   22       77         0          4   1.00000   0.00000   1.00000   1.00000  Genotype=+/+; Tg/+   
   24       73         0          2   1.00000   0.00000   1.00000   1.00000  Genotype=+/+; Tg/+   
   28       71         0          1   1.00000   0.00000   1.00000   1.00000  Genotype=+/+; Tg/+   
   29       70         0          2   1.00000   0.00000   1.00000   1.00000  Genotype=+/+; Tg/+   
   30       68         0          1   1.00000   0.00000   1.00000   1.00000  Genotype=+/+; Tg/+   
   31       67         0          4   1.00000   0.00000   1.00000   1.00000  Genotype=+/+; Tg/+   
   32       63         0          2   1.00000   0.00000   1.00000   1.00000  Genotype=+/+; Tg/+   
   33       61         0          1   1.00000   0.00000   1.00000   1.00000  Genotype=+/+; Tg/+   
   35       60         0          1   1.00000   0.00000   1.00000   1.00000  Genotype=+/+; Tg/+   
   38       59         0          1   1.00000   0.00000   1.00000   1.00000  Genotype=+/+; Tg/+   
   46       58         0          4   1.00000   0.00000   1.00000   1.00000  Genotype=+/+; Tg/+   
   47       54         0          1   1.00000   0.00000   1.00000   1.00000  Genotype=+/+; Tg/+   
  100       53         0          2   1.00000   0.00000   1.00000   1.00000  Genotype=+/+; Tg/+   
  112       51         0          1   1.00000   0.00000   1.00000   1.00000  Genotype=+/+; Tg/+   
  114       50         1          0   0.98000   0.02020   1.00000   0.94195  Genotype=+/+; Tg/+   
  170       49         0          1   0.98000   0.02020   1.00000   0.94195  Genotype=+/+; Tg/+   
  188       48         0          2   0.98000   0.02020   1.00000   0.94195  Genotype=+/+; Tg/+   
  245       46         0          1   0.98000   0.02020   1.00000   0.94195  Genotype=+/+; Tg/+   
  248       45         0          1   0.98000   0.02020   1.00000   0.94195  Genotype=+/+; Tg/+   
  259       44         0          2   0.98000   0.02020   1.00000   0.94195  Genotype=+/+; Tg/+   
  261       42         0          1   0.98000   0.02020   1.00000   0.94195  Genotype=+/+; Tg/+   
  262       41         0          2   0.98000   0.02020   1.00000   0.94195  Genotype=+/+; Tg/+   
  266       39         0          3   0.98000   0.02020   1.00000   0.94195  Genotype=+/+; Tg/+   
  267       36         0          1   0.98000   0.02020   1.00000   0.94195  Genotype=+/+; Tg/+   
  268       35         0          1   0.98000   0.02020   1.00000   0.94195  Genotype=+/+; Tg/+   
  273       34         0          1   0.98000   0.02020   1.00000   0.94195  Genotype=+/+; Tg/+   
  280       33         0          1   0.98000   0.02020   1.00000   0.94195  Genotype=+/+; Tg/+   
  295       32         0          2   0.98000   0.02020   1.00000   0.94195  Genotype=+/+; Tg/+   
  296       30         0          1   0.98000   0.02020   1.00000   0.94195  Genotype=+/+; Tg/+   
  298       29         0          2   0.98000   0.02020   1.00000   0.94195  Genotype=+/+; Tg/+   
  299       27         0          1   0.98000   0.02020   1.00000   0.94195  Genotype=+/+; Tg/+   
  306       26         0          2   0.98000   0.02020   1.00000   0.94195  Genotype=+/+; Tg/+   
  310       24         0          1   0.98000   0.02020   1.00000   0.94195  Genotype=+/+; Tg/+   
  312       23         0          3   0.98000   0.02020   1.00000   0.94195  Genotype=+/+; Tg/+   
  313       20         0          2   0.98000   0.02020   1.00000   0.94195  Genotype=+/+; Tg/+   
  319       18         0          2   0.98000   0.02020   1.00000   0.94195  Genotype=+/+; Tg/+   
  322       16         0          1   0.98000   0.02020   1.00000   0.94195  Genotype=+/+; Tg/+   
  325       15         0          1   0.98000   0.02020   1.00000   0.94195  Genotype=+/+; Tg/+   
  337       14         0          2   0.98000   0.02020   1.00000   0.94195  Genotype=+/+; Tg/+   
  343       12         0          1   0.98000   0.02020   1.00000   0.94195  Genotype=+/+; Tg/+   
  354       11         0          2   0.98000   0.02020   1.00000   0.94195  Genotype=+/+; Tg/+   
  360        9         0          1   0.98000   0.02020   1.00000   0.94195  Genotype=+/+; Tg/+   
  368        8         0          1   0.98000   0.02020   1.00000   0.94195  Genotype=+/+; Tg/+   
  372        7         0          1   0.98000   0.02020   1.00000   0.94195  Genotype=+/+; Tg/+   
  380        6         0          2   0.98000   0.02020   1.00000   0.94195  Genotype=+/+; Tg/+   
  452        4         1          0   0.73500   0.28938   1.00000   0.41684  Genotype=+/+; Tg/+   
  773        3         1          0   0.49000   0.50041   1.00000   0.18376  Genotype=+/+; Tg/+   
  805        2         1          0   0.24500   0.86626   1.00000   0.04485  Genotype=+/+; Tg/+   
  935        1         1          0   0.00000       Inf        NA        NA  Genotype=+/+; Tg/+   
   15      208         0          1   1.00000   0.00000   1.00000   1.00000  Genotype=fl/fl; +/+  
   17      207         0          3   1.00000   0.00000   1.00000   1.00000  Genotype=fl/fl; +/+  
   18      204         0          9   1.00000   0.00000   1.00000   1.00000  Genotype=fl/fl; +/+  
   19      195         0          1   1.00000   0.00000   1.00000   1.00000  Genotype=fl/fl; +/+  
   21      194         0          4   1.00000   0.00000   1.00000   1.00000  Genotype=fl/fl; +/+  
   22      190         0          3   1.00000   0.00000   1.00000   1.00000  Genotype=fl/fl; +/+  
   23      187         0          1   1.00000   0.00000   1.00000   1.00000  Genotype=fl/fl; +/+  
   24      186         0          1   1.00000   0.00000   1.00000   1.00000  Genotype=fl/fl; +/+  
   28      185         0          2   1.00000   0.00000   1.00000   1.00000  Genotype=fl/fl; +/+  
   31      183         0          8   1.00000   0.00000   1.00000   1.00000  Genotype=fl/fl; +/+  
   32      175         0          3   1.00000   0.00000   1.00000   1.00000  Genotype=fl/fl; +/+  
   36      172         0          1   1.00000   0.00000   1.00000   1.00000  Genotype=fl/fl; +/+  
   37      171         0          1   1.00000   0.00000   1.00000   1.00000  Genotype=fl/fl; +/+  
   38      170         0          1   1.00000   0.00000   1.00000   1.00000  Genotype=fl/fl; +/+  
   39      169         0          3   1.00000   0.00000   1.00000   1.00000  Genotype=fl/fl; +/+  
   41      166         0          6   1.00000   0.00000   1.00000   1.00000  Genotype=fl/fl; +/+  
   42      160         0          1   1.00000   0.00000   1.00000   1.00000  Genotype=fl/fl; +/+  
   43      159         0          1   1.00000   0.00000   1.00000   1.00000  Genotype=fl/fl; +/+  
   45      158         0          1   1.00000   0.00000   1.00000   1.00000  Genotype=fl/fl; +/+  
   48      157         0          1   1.00000   0.00000   1.00000   1.00000  Genotype=fl/fl; +/+  
   49      156         0          1   1.00000   0.00000   1.00000   1.00000  Genotype=fl/fl; +/+  
   50      155         1          1   0.99355   0.00647   1.00000   0.98102  Genotype=fl/fl; +/+  
   58      153         0          1   0.99355   0.00647   1.00000   0.98102  Genotype=fl/fl; +/+  
   59      152         0          1   0.99355   0.00647   1.00000   0.98102  Genotype=fl/fl; +/+  
   62      151         0          4   0.99355   0.00647   1.00000   0.98102  Genotype=fl/fl; +/+  
   69      147         0          1   0.99355   0.00647   1.00000   0.98102  Genotype=fl/fl; +/+  
   70      146         0          1   0.99355   0.00647   1.00000   0.98102  Genotype=fl/fl; +/+  
   78      145         0          2   0.99355   0.00647   1.00000   0.98102  Genotype=fl/fl; +/+  
   81      143         0          1   0.99355   0.00647   1.00000   0.98102  Genotype=fl/fl; +/+  
   85      142         0          1   0.99355   0.00647   1.00000   0.98102  Genotype=fl/fl; +/+  
   86      141         0          1   0.99355   0.00647   1.00000   0.98102  Genotype=fl/fl; +/+  
   89      140         0          1   0.99355   0.00647   1.00000   0.98102  Genotype=fl/fl; +/+  
   97      139         1          0   0.98640   0.00970   1.00000   0.96783  Genotype=fl/fl; +/+  
  103      138         0          2   0.98640   0.00970   1.00000   0.96783  Genotype=fl/fl; +/+  
  106      136         0          1   0.98640   0.00970   1.00000   0.96783  Genotype=fl/fl; +/+  
  111      135         0          1   0.98640   0.00970   1.00000   0.96783  Genotype=fl/fl; +/+  
  112      134         0          3   0.98640   0.00970   1.00000   0.96783  Genotype=fl/fl; +/+  
  124      131         0          1   0.98640   0.00970   1.00000   0.96783  Genotype=fl/fl; +/+  
  126      130         0          1   0.98640   0.00970   1.00000   0.96783  Genotype=fl/fl; +/+  
  131      129         0          2   0.98640   0.00970   1.00000   0.96783  Genotype=fl/fl; +/+  
  132      127         1          1   0.97863   0.01251   1.00000   0.95493  Genotype=fl/fl; +/+  
  134      125         0          1   0.97863   0.01251   1.00000   0.95493  Genotype=fl/fl; +/+  
  135      124         1          0   0.97074   0.01490   0.99951   0.94280  Genotype=fl/fl; +/+  
  141      123         0          1   0.97074   0.01490   0.99951   0.94280  Genotype=fl/fl; +/+  
  143      122         0          3   0.97074   0.01490   0.99951   0.94280  Genotype=fl/fl; +/+  
  150      119         0          1   0.97074   0.01490   0.99951   0.94280  Genotype=fl/fl; +/+  
  153      118         0          2   0.97074   0.01490   0.99951   0.94280  Genotype=fl/fl; +/+  
  154      116         0          1   0.97074   0.01490   0.99951   0.94280  Genotype=fl/fl; +/+  
  155      115         0          1   0.97074   0.01490   0.99951   0.94280  Genotype=fl/fl; +/+  
  160      114         0          2   0.97074   0.01490   0.99951   0.94280  Genotype=fl/fl; +/+  
  164      112         0          2   0.97074   0.01490   0.99951   0.94280  Genotype=fl/fl; +/+  
  170      110         0          1   0.97074   0.01490   0.99951   0.94280  Genotype=fl/fl; +/+  
  171      109         0          2   0.97074   0.01490   0.99951   0.94280  Genotype=fl/fl; +/+  
  172      107         0          4   0.97074   0.01490   0.99951   0.94280  Genotype=fl/fl; +/+  
  174      103         0          3   0.97074   0.01490   0.99951   0.94280  Genotype=fl/fl; +/+  
  177      100         0          2   0.97074   0.01490   0.99951   0.94280  Genotype=fl/fl; +/+  
  180       98         0          1   0.97074   0.01490   0.99951   0.94280  Genotype=fl/fl; +/+  
  181       97         0          1   0.97074   0.01490   0.99951   0.94280  Genotype=fl/fl; +/+  
  188       96         0          2   0.97074   0.01490   0.99951   0.94280  Genotype=fl/fl; +/+  
  193       94         0          1   0.97074   0.01490   0.99951   0.94280  Genotype=fl/fl; +/+  
  195       93         0          2   0.97074   0.01490   0.99951   0.94280  Genotype=fl/fl; +/+  
  196       91         0          2   0.97074   0.01490   0.99951   0.94280  Genotype=fl/fl; +/+  
  200       89         0          1   0.97074   0.01490   0.99951   0.94280  Genotype=fl/fl; +/+  
  202       88         0          2   0.97074   0.01490   0.99951   0.94280  Genotype=fl/fl; +/+  
  204       86         0          2   0.97074   0.01490   0.99951   0.94280  Genotype=fl/fl; +/+  
  207       84         0          3   0.97074   0.01490   0.99951   0.94280  Genotype=fl/fl; +/+  
  209       81         0          3   0.97074   0.01490   0.99951   0.94280  Genotype=fl/fl; +/+  
  210       78         0          1   0.97074   0.01490   0.99951   0.94280  Genotype=fl/fl; +/+  
  212       77         0          1   0.97074   0.01490   0.99951   0.94280  Genotype=fl/fl; +/+  
  218       76         1          0   0.95797   0.01994   0.99614   0.92126  Genotype=fl/fl; +/+  
  221       75         0          1   0.95797   0.01994   0.99614   0.92126  Genotype=fl/fl; +/+  
  223       74         0          2   0.95797   0.01994   0.99614   0.92126  Genotype=fl/fl; +/+  
  225       72         0          3   0.95797   0.01994   0.99614   0.92126  Genotype=fl/fl; +/+  
  240       69         0          1   0.95797   0.01994   0.99614   0.92126  Genotype=fl/fl; +/+  
  243       68         0          1   0.95797   0.01994   0.99614   0.92126  Genotype=fl/fl; +/+  
  247       67         0          1   0.95797   0.01994   0.99614   0.92126  Genotype=fl/fl; +/+  
  251       66         0          2   0.95797   0.01994   0.99614   0.92126  Genotype=fl/fl; +/+  
  256       64         0          2   0.95797   0.01994   0.99614   0.92126  Genotype=fl/fl; +/+  
  261       62         0          2   0.95797   0.01994   0.99614   0.92126  Genotype=fl/fl; +/+  
  263       60         0          1   0.95797   0.01994   0.99614   0.92126  Genotype=fl/fl; +/+  
  266       59         0          3   0.95797   0.01994   0.99614   0.92126  Genotype=fl/fl; +/+  
  270       56         0          1   0.95797   0.01994   0.99614   0.92126  Genotype=fl/fl; +/+  
  273       55         0          2   0.95797   0.01994   0.99614   0.92126  Genotype=fl/fl; +/+  
  276       53         0          1   0.95797   0.01994   0.99614   0.92126  Genotype=fl/fl; +/+  
  280       52         0          1   0.95797   0.01994   0.99614   0.92126  Genotype=fl/fl; +/+  
  284       51         1          0   0.93918   0.02810   0.99236   0.88886  Genotype=fl/fl; +/+  
  286       50         0          1   0.93918   0.02810   0.99236   0.88886  Genotype=fl/fl; +/+  
  287       49         0          1   0.93918   0.02810   0.99236   0.88886  Genotype=fl/fl; +/+  
  293       48         0          1   0.93918   0.02810   0.99236   0.88886  Genotype=fl/fl; +/+  
  294       47         0          1   0.93918   0.02810   0.99236   0.88886  Genotype=fl/fl; +/+  
  296       46         0          2   0.93918   0.02810   0.99236   0.88886  Genotype=fl/fl; +/+  
  297       44         0          3   0.93918   0.02810   0.99236   0.88886  Genotype=fl/fl; +/+  
  298       41         0          1   0.93918   0.02810   0.99236   0.88886  Genotype=fl/fl; +/+  
  305       40         0          1   0.93918   0.02810   0.99236   0.88886  Genotype=fl/fl; +/+  
  306       39         0          1   0.93918   0.02810   0.99236   0.88886  Genotype=fl/fl; +/+  
  310       38         0          1   0.93918   0.02810   0.99236   0.88886  Genotype=fl/fl; +/+  
  314       37         0          2   0.93918   0.02810   0.99236   0.88886  Genotype=fl/fl; +/+  
  316       35         0          4   0.93918   0.02810   0.99236   0.88886  Genotype=fl/fl; +/+  
  317       31         0          6   0.93918   0.02810   0.99236   0.88886  Genotype=fl/fl; +/+  
  318       25         0          2   0.93918   0.02810   0.99236   0.88886  Genotype=fl/fl; +/+  
  333       23         0          3   0.93918   0.02810   0.99236   0.88886  Genotype=fl/fl; +/+  
  343       20         0          1   0.93918   0.02810   0.99236   0.88886  Genotype=fl/fl; +/+  
  360       19         0          2   0.93918   0.02810   0.99236   0.88886  Genotype=fl/fl; +/+  
  368       17         0          2   0.93918   0.02810   0.99236   0.88886  Genotype=fl/fl; +/+  
  375       15         0          1   0.93918   0.02810   0.99236   0.88886  Genotype=fl/fl; +/+  
  376       14         0          1   0.93918   0.02810   0.99236   0.88886  Genotype=fl/fl; +/+  
  378       13         0          1   0.93918   0.02810   0.99236   0.88886  Genotype=fl/fl; +/+  
  402       12         0          1   0.93918   0.02810   0.99236   0.88886  Genotype=fl/fl; +/+  
  427       11         0          2   0.93918   0.02810   0.99236   0.88886  Genotype=fl/fl; +/+  
  596        9         1          0   0.83483   0.12116   1.00000   0.65837  Genotype=fl/fl; +/+  
  623        8         1          0   0.73048   0.18038   1.00000   0.51294  Genotype=fl/fl; +/+  
  718        7         1          0   0.62612   0.23737   0.99704   0.39320  Genotype=fl/fl; +/+  
  819        6         1          0   0.52177   0.29946   0.93839   0.29012  Genotype=fl/fl; +/+  
  869        5         1          0   0.41742   0.37374   0.86835   0.20065  Genotype=fl/fl; +/+  
  879        4         1          0   0.31306   0.47224   0.78996   0.12407  Genotype=fl/fl; +/+  
  886        3         1          0   0.20871   0.62424   0.70941   0.06140  Genotype=fl/fl; +/+  
  894        2         1          0   0.10435   0.94323   0.66280   0.01643  Genotype=fl/fl; +/+  
  936        1         1          0   0.00000       Inf        NA        NA  Genotype=fl/fl; +/+  

![](mouse-aging-analysis_files/figure-html/fitting-mck-1.png) 

![](mouse-aging-analysis_files/figure-html/fitting-mck-ko-1.png) 


Table: Muscle TSC1 Knockout Summary

                        Total Animals   Natural Deaths
---------------------  --------------  ---------------
Genotype=fl/fl; Tg/+              188               22
Genotype=+/+; +/+                 125                7
Genotype=+/+; Tg/+                104                5
Genotype=fl/fl; +/+               208               15



## Combining the Control Mice

![](mouse-aging-analysis_files/figure-html/fitting-mck-controls-combined-1.png) 


The chi-squared test for comparing the two genotypes is significant, with a p-value of 0.  The results of these tests are in the table below.  The effects of each genotype, relative to the knockout strains are in the table below. These results are presented graphically in the figure below.  This means that the knockout mice are 4.17138 times more likely to die at any given time.


Table: Muscle TSC1 Knockout Tests controls combined

                         test   df      pvalue
----------------------  -----  ---  ----------
Likelihood ratio test      18    1   0.0000219
Wald test                  18    1   0.0000202
Score (logrank) test       21    1   0.0000047



Table: Muscle TSC1 Knockout Coefficients, relative to Knockout, controls combined

                  beta     se    2.5 %   97.5 %            p
-------------  -------  -----  -------  -------  -----------
KnockoutTRUE    -1.428   0.24   -2.085   -0.771   0.00002023




\bibliography{references}
\bibliographystyle{unsrt}

# Session Information


```
## R version 3.2.2 (2015-08-14)
## Platform: x86_64-apple-darwin13.4.0 (64-bit)
## Running under: OS X 10.11.3 (El Capitan)
## 
## locale:
## [1] en_US.UTF-8/en_US.UTF-8/en_US.UTF-8/C/en_US.UTF-8/en_US.UTF-8
## 
## attached base packages:
## [1] stats     graphics  grDevices utils     datasets  methods   base     
## 
## other attached packages:
## [1] bibtex_0.4.0       RColorBrewer_1.1-2 ggfortify_0.1.0   
## [4] ggplot2_2.0.0      proto_0.3-10       xtable_1.8-0      
## [7] coin_1.1-2         survival_2.38-3    knitr_1.11        
## 
## loaded via a namespace (and not attached):
##  [1] Rcpp_0.12.2       formatR_1.2.1     highr_0.5.1      
##  [4] plyr_1.8.3        tools_3.2.2       digest_0.6.8     
##  [7] evaluate_0.8      gtable_0.1.2      lattice_0.20-33  
## [10] DBI_0.3.1         yaml_2.1.13       parallel_3.2.2   
## [13] mvtnorm_1.0-3     gridExtra_2.0.0   stringr_1.0.0    
## [16] dplyr_0.4.3       stats4_3.2.2      grid_3.2.2       
## [19] R6_2.1.1          rmarkdown_0.8.1   multcomp_1.4-1   
## [22] TH.data_1.0-6     tidyr_0.3.1       magrittr_1.5     
## [25] scales_0.3.0      codetools_0.2-14  htmltools_0.2.6  
## [28] modeltools_0.2-21 splines_3.2.2     assertthat_0.1   
## [31] colorspace_1.2-6  sandwich_2.3-4    stringi_1.0-1    
## [34] munsell_0.4.2     zoo_1.7-12
```
