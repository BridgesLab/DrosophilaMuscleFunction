# Western Blot Quantification from Muscle Tsc1 Knockout Quadriceps
Dave Bridges  
December 14, 2015  




# Data Entry and Calculations




These data are found in /Users/davebrid/Documents/GitHub/DrosophilaMuscleFunction/Protein Analysis/Muscle-Tsc1 Blots and were most recently updated on Tue Oct 25 19:24:24 2016.  It reads from the input quantification file named Quantification.csv.


Table: Raw Quantification Data

------------  ----------  ----------  ----------  ----------  ----------  ---------  ---------  ---------  ---------  ---------
Genotype      Wild-Type   Wild-Type   Wild-Type   Wild-Type   Wild-Type   Knockout   Knockout   Knockout   Knockout   Knockout 
Sample        811         867         1251        1260        1550        869        1264       1265       1266       1552     
4F2hc         11400       15600       17700       -3770       10500       18800      24700      18600      33900      15400    
Actin         296000      201000      321000      405000      317000      451000     493000     617000     527000     625000   
CD36          501000      68100       465000      686000      397000      619000     833000     1160000    1420000    1390000  
CI-NDUF88     67800       72400       80900       74300       47600       60100      53500      68300      72400      110000   
CII-SDHB      174000      186000      269000      168000      118000      166000     157000     127000     174000     228000   
CIII-UQCRC2   400000      444000      465000      468000      325000      487000     440000     255000     242000     306000   
CIV-MTCO1     6180        77100       17800       2350        15900       45100      30900      25300      25300      1310     
CV-ATP5A      218000      223000      344000      283000      224000      469000     301000     198000     210000     218000   
------------  ----------  ----------  ----------  ----------  ----------  ---------  ---------  ---------  ---------  ---------



Table: Summarized Ratios

-----------------  ----------  ----------  ----------  ----------  ----------  ---------  ---------  ---------  ---------  ---------
Sample             811         867         1251        1260        1550        869        1264       1265       1266       1552     
Genotype           Wild-Type   Wild-Type   Wild-Type   Wild-Type   Wild-Type   Knockout   Knockout   Knockout   Knockout   Knockout 
pS6K.Ratio         0.0261      0.0228      0.0269      0.0219      0.0315      0.1212     0.1084     0.0801     0.1051     0.0757   
pS6.Ratio          1.40        1.13        11.04       1.12        17.75       21.41      32.75      28.34      20.36      20.13    
pJNK.Ratio         0.641       0.580       0.588       0.708       0.671       2.039      0.946      0.897      0.979      0.461    
LC3.Ratio          2.056       2.033       1.302       1.672       1.103       0.158      0.259      0.168      0.305      0.210    
CD36.Ratio         0.477       0.049       0.388       0.597       0.320       0.534      0.817      0.829      0.904      1.397    
NDUF88.Ratio       0.0646      0.0521      0.0674      0.0646      0.0384      0.0518     0.0525     0.0488     0.0461     0.1106   
SDHB.Ratio         0.1657      0.1338      0.2242      0.1461      0.0952      0.1431     0.1539     0.0907     0.1108     0.2291   
UQCRC2.Ratio       0.381       0.319       0.388       0.407       0.262       0.420      0.431      0.182      0.154      0.308    
MTCO1.Ratio        0.00589     0.05547     0.01483     0.00204     0.01282     0.03888    0.03029    0.01807    0.01611    0.00132  
ATP5A.Ratio        0.208       0.160       0.287       0.246       0.181       0.404      0.295      0.141      0.134      0.219    
LAT1.Ratio         0.00821     0.01453     0.01475     0.01339     0.00903     0.01164    0.01245    0.00921    0.01242    0.01528  
Sarcolipin.Ratio   0.1038      0.1345      0.1333      0.0254      0.1532      0.4284     0.4892     0.4921     0.3777     0.4714   
4F2hc.Ratio        0.01086     0.01122     0.01475     -0.00328    0.00847     0.01621    0.02422    0.01329    0.02159    0.01548  
-----------------  ----------  ----------  ----------  ----------  ----------  ---------  ---------  ---------  ---------  ---------



Table: Summarized Normalized Ratios

----------------  ----------  ----------  ----------  ----------  ----------  ---------  ---------  ---------  ---------  ---------
Sample            811         867         1251        1260        1550        869        1264       1265       1266       1552     
Genotype          Wild-Type   Wild-Type   Wild-Type   Wild-Type   Wild-Type   Knockout   Knockout   Knockout   Knockout   Knockout 
pS6K.norm         1.011       0.882       1.041       0.846       1.220       4.689      4.197      3.098      4.069      2.930    
pS6.norm          0.216       0.175       1.702       0.172       2.735       3.300      5.048      4.369      3.139      3.103    
pJNK.norm         1.005       0.910       0.922       1.110       1.053       3.197      1.484      1.407      1.535      0.723    
LC3.norm          2.056       2.033       1.302       1.672       1.103       0.158      0.259      0.168      0.305      0.210    
CD36.norm         1.303       0.134       1.059       1.630       0.875       1.458      2.231      2.263      2.471      3.816    
NDUF88.norm       1.125       0.907       1.174       1.125       0.669       0.902      0.914      0.850      0.803      1.926    
SDHB.norm         1.083       0.875       1.465       0.955       0.622       0.935      1.006      0.593      0.724      1.498    
UQCRC2.norm       1.084       0.909       1.103       1.158       0.746       1.195      1.228      0.518      0.439      0.875    
MTCO1.norm        0.3232      3.0459      0.8145      0.1122      0.7041      2.1350     1.6635     0.9924     0.8849     0.0723   
ATP5A.norm        0.960       0.742       1.325       1.138       0.835       1.869      1.364      0.654      0.618      1.013    
LAT1.norm         0.685       1.213       1.231       1.118       0.754       0.971      1.039      0.769      1.036      1.275    
4F2hc.norm        1.29        1.34        1.76        -0.39       1.01        1.93       2.88       1.58       2.57       1.84     
Sarcolipin.norm   0.943       1.222       1.211       0.231       1.392       3.893      4.445      4.472      3.432      4.283    
----------------  ----------  ----------  ----------  ----------  ----------  ---------  ---------  ---------  ---------  ---------



Table: Summarized Values

---------------------  ----------  ---------
Genotype               Wild-Type   Knockout 
pS6K.norm_mean         1.0         3.8      
pS6.norm_mean          1.00        3.79     
pJNK.norm_mean         1.00        1.67     
LC3.norm_mean          1.63        0.22     
CD36.norm_mean         1.00        2.45     
NDUF88.norm_mean       1.00        1.08     
SDHB.norm_mean         1.000       0.951    
UQCRC2.norm_mean       1.000       0.851    
MTCO1.norm_mean        1.00        1.15     
ATP5A.norm_mean        1.0         1.1      
LAT1.norm_mean         1.00        1.02     
4F2hc.norm_mean        1.00        2.16     
Sarcolipin.norm_mean   1.0         4.1      
pS6K.norm_se           0.0663      0.3368   
pS6.norm_se            0.524       0.391    
pJNK.norm_se           0.0381      0.4093   
LC3.norm_se            0.1912      0.0277   
CD36.norm_se           0.251       0.383    
NDUF88.norm_se         0.0949      0.2126   
SDHB.norm_se           0.139       0.155    
UQCRC2.norm_se         0.076       0.165    
MTCO1.norm_se          0.527       0.353    
ATP5A.norm_se          0.105       0.235    
LAT1.norm_se           0.1167      0.0809   
4F2hc.norm_se          0.367       0.243    
Sarcolipin.norm_se     0.205       0.197    
---------------------  ----------  ---------


![Normalized mTORC1 Activity in Quadriceps](figures/s6k-quantification-1.pdf)

![Normalized S6K Activity in Quadriceps](figures/s6-quantification-1.pdf)

![Normalized mTORC1 Activity in Quadriceps](figures/mTORC1-quantification-1.pdf)

![Normalized JNK Phosphorylation in Quadriceps](figures/jnk-quantification-1.pdf)

![Normalized LC3 Processing in Quadriceps](figures/lc3-quantification-1.pdf)


![Normalized Mitochondrial Protein Levels in Quadriceps](figures/mitoprofile-quantification-1.pdf)


![Normalized CD36 Levels in Quadriceps](figures/cd36-quantification-1.pdf)

![Normalized LAT1 Protein Levels in Quadriceps](figures/lat1-quantification-1.pdf)


![](figures/sarcolipin-quantification-1.pdf)<!-- -->

# Statistics


Table: Statistical Summary

              Shapiro-WT   Shapiro-KO   Wilcoxon   Levene   Welch   Student
-----------  -----------  -----------  ---------  -------  ------  --------
pS6K               0.648        0.446      0.008    0.076   0.001     0.000
pS6                0.058        0.133      0.008    0.772   0.003     0.003
pJNK               0.603        0.158      0.151    0.206   0.178     0.142
LC3                0.395        0.605      0.008    0.015   0.002     0.000
ATP5A              0.838        0.493      1.000    0.187   0.701     0.697
UQCRC2             0.361        0.281      0.841    0.118   0.444     0.435
MTCO1              0.045        0.911      0.548    0.815   0.820     0.819
SDHB               0.885        0.596      0.841    0.849   0.821     0.821
NDUF88             0.163        0.002      0.690    0.679   0.747     0.743
Sarcolipin         0.153        0.272      0.008    0.900   0.000     0.000
CD36               0.793        0.412      0.016    0.701   0.016     0.013

# Session Information
\begin{itemize}\raggedright
  \item R version 3.3.0 (2016-05-03), \verb|x86_64-apple-darwin13.4.0|
  \item Locale: \verb|en_US.UTF-8/en_US.UTF-8/en_US.UTF-8/C/en_US.UTF-8/en_US.UTF-8|
  \item Base packages: base, datasets, graphics, grDevices,
    methods, stats, utils
  \item Other packages: car~2.1-3, dplyr~0.5.0, knitr~1.14,
    tidyr~0.6.0
  \item Loaded via a namespace (and not attached): assertthat~0.1,
    DBI~0.5-1, digest~0.6.10, evaluate~0.9, formatR~1.4,
    grid~3.3.0, highr~0.6, htmltools~0.3.5, lattice~0.20-34,
    lazyeval~0.2.0, lme4~1.1-12, magrittr~1.5, MASS~7.3-45,
    Matrix~1.2-7.1, MatrixModels~0.4-1, mgcv~1.8-15, minqa~1.2.4,
    nlme~3.1-128, nloptr~1.0.4, nnet~7.3-12, parallel~3.3.0,
    pbkrtest~0.4-6, quantreg~5.29, R6~2.1.3, Rcpp~0.12.7,
    rmarkdown~1.1, SparseM~1.72, splines~3.3.0, stringi~1.1.1,
    stringr~1.1.0, tibble~1.2, tools~3.3.0, yaml~2.1.13
\end{itemize}
