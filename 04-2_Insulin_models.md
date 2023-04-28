# Insulin Models



<!-- Environment -->


<!-- ## Custom functions -->


<!-- # Read data -->


<!-- Variable definitions -->


Number of samples per timepoint
<table class=" lightable-classic" style='font-size: 18px; font-family: "Arial Narrow", "Source Sans Pro", sans-serif; width: auto !important; '>
 <thead>
  <tr>
   <th style="text-align:left;">   </th>
   <th style="text-align:right;"> SCOPE </th>
   <th style="text-align:right;"> STOP </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td style="text-align:left;"> 12wks </td>
   <td style="text-align:right;"> 0 </td>
   <td style="text-align:right;"> 0 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> 15wks </td>
   <td style="text-align:right;"> 0 </td>
   <td style="text-align:right;"> 0 </td>
  </tr>
</tbody>
</table>

## Raw plots
<img src="04-2_Insulin_models_files/figure-html/raw_plot3-1.png" width="1152" /><img src="04-2_Insulin_models_files/figure-html/raw_plot3-2.png" width="1152" />

## SCOPE vs STOP
Fit GEE models for Insulin and HOMA-IR.<br />

- <b>Outcomes: </b> Insulin, HOMA-IR (all outcomes log-transformed) <br />
- <b>Independent variables:</b> Study, GA at sampling <br />
- <b>Model fitted:</b> LME model <br/>
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;log(insulin) ~ Study + GA at sampling + Study:GA at sampling")<br />
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Random intercepts for Study ID



### Global tests
Type III ANOVA on main and interaction effects, and model summaries.

<b> Insulin </b><br /><table class=" lightable-classic" style='font-size: 16px; font-family: "Arial Narrow", "Source Sans Pro", sans-serif; width: auto !important; '>
 <thead>
  <tr>
   <th style="text-align:left;">   </th>
   <th style="text-align:left;"> model term </th>
   <th style="text-align:right;"> df1 </th>
   <th style="text-align:right;"> df2 </th>
   <th style="text-align:right;"> F.ratio </th>
   <th style="text-align:right;"> Chisq </th>
   <th style="text-align:left;"> p.value </th>
   <th style="text-align:left;">  </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td style="text-align:left;"> 1 </td>
   <td style="text-align:left;"> Study </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> Inf </td>
   <td style="text-align:right;"> 2.836 </td>
   <td style="text-align:right;"> 2.836 </td>
   <td style="text-align:left;"> 0.09 </td>
   <td style="text-align:left;"> ns </td>
  </tr>
  <tr>
   <td style="text-align:left;"> 3 </td>
   <td style="text-align:left;"> GA_samp </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> Inf </td>
   <td style="text-align:right;"> 0.141 </td>
   <td style="text-align:right;"> 0.141 </td>
   <td style="text-align:left;"> 0.7 </td>
   <td style="text-align:left;"> ns </td>
  </tr>
  <tr>
   <td style="text-align:left;"> 2 </td>
   <td style="text-align:left;"> Study:GA_samp </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> Inf </td>
   <td style="text-align:right;"> 1.794 </td>
   <td style="text-align:right;"> 1.794 </td>
   <td style="text-align:left;"> 0.2 </td>
   <td style="text-align:left;"> ns </td>
  </tr>
</tbody>
</table>


<b> HOMA.IR </b><br /><table class=" lightable-classic" style='font-size: 16px; font-family: "Arial Narrow", "Source Sans Pro", sans-serif; width: auto !important; '>
 <thead>
  <tr>
   <th style="text-align:left;">   </th>
   <th style="text-align:left;"> model term </th>
   <th style="text-align:right;"> df1 </th>
   <th style="text-align:right;"> df2 </th>
   <th style="text-align:right;"> F.ratio </th>
   <th style="text-align:right;"> Chisq </th>
   <th style="text-align:left;"> p.value </th>
   <th style="text-align:left;">  </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td style="text-align:left;"> 1 </td>
   <td style="text-align:left;"> Study </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> Inf </td>
   <td style="text-align:right;"> 3.756 </td>
   <td style="text-align:right;"> 3.756 </td>
   <td style="text-align:left;"> 0.05 </td>
   <td style="text-align:left;"> ns </td>
  </tr>
  <tr>
   <td style="text-align:left;"> 3 </td>
   <td style="text-align:left;"> GA_samp </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> Inf </td>
   <td style="text-align:right;"> 0.338 </td>
   <td style="text-align:right;"> 0.338 </td>
   <td style="text-align:left;"> 0.6 </td>
   <td style="text-align:left;"> ns </td>
  </tr>
  <tr>
   <td style="text-align:left;"> 2 </td>
   <td style="text-align:left;"> Study:GA_samp </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> Inf </td>
   <td style="text-align:right;"> 1.926 </td>
   <td style="text-align:right;"> 1.926 </td>
   <td style="text-align:left;"> 0.2 </td>
   <td style="text-align:left;"> ns </td>
  </tr>
</tbody>
</table>

### Model summary
Ratio of Geometric means (95% CI)


<b> Insulin </b><br /><table class=" lightable-classic" style='font-size: 16px; font-family: "Arial Narrow", "Source Sans Pro", sans-serif; width: auto !important; '>
 <thead>
  <tr>
   <th style="text-align:left;"> Var </th>
   <th style="text-align:left;"> Effect </th>
   <th style="text-align:left;"> P </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td style="text-align:left;"> (Intercept) </td>
   <td style="text-align:left;"> 3.31 (2.07, 4.54) </td>
   <td style="text-align:left;"> &lt;0.0001 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> StudySTOP </td>
   <td style="text-align:left;"> -1.10 (-2.39, 0.18) </td>
   <td style="text-align:left;"> 0.09 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> GA_samp </td>
   <td style="text-align:left;"> -0.04 (-0.12, 0.04) </td>
   <td style="text-align:left;"> 0.36 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> StudySTOP:GA_samp </td>
   <td style="text-align:left;"> 0.06 (-0.03, 0.14) </td>
   <td style="text-align:left;"> 0.18 </td>
  </tr>
</tbody>
</table>


<b> HOMA.IR </b><br /><table class=" lightable-classic" style='font-size: 16px; font-family: "Arial Narrow", "Source Sans Pro", sans-serif; width: auto !important; '>
 <thead>
  <tr>
   <th style="text-align:left;"> Var </th>
   <th style="text-align:left;"> Effect </th>
   <th style="text-align:left;"> P </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td style="text-align:left;"> (Intercept) </td>
   <td style="text-align:left;"> 2.00 (0.71, 3.28) </td>
   <td style="text-align:left;"> 0.002 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> StudySTOP </td>
   <td style="text-align:left;"> -1.32 (-2.65, 0.01) </td>
   <td style="text-align:left;"> 0.05 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> GA_samp </td>
   <td style="text-align:left;"> -0.04 (-0.13, 0.04) </td>
   <td style="text-align:left;"> 0.29 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> StudySTOP:GA_samp </td>
   <td style="text-align:left;"> 0.06 (-0.03, 0.15) </td>
   <td style="text-align:left;"> 0.17 </td>
  </tr>
</tbody>
</table>


### Diagnostics
Model diagnositcs.


<p>Diagnositcs for  Insulin </b></p>
<img src="04-2_Insulin_models_files/figure-html/model_diag-1.png" width="672" />
<p>Diagnositcs for  HOMA.IR </b></p>
<img src="04-2_Insulin_models_files/figure-html/model_diag-2.png" width="672" />

### Estimated means
Estimated marginal means (or adjusted means) adjusted for GA at sampling.<br />

<b> Insulin </b><table class=" lightable-classic" style='font-size: 16px; font-family: "Arial Narrow", "Source Sans Pro", sans-serif; width: auto !important; '>
 <thead>
  <tr>
   <th style="text-align:left;"> Study </th>
   <th style="text-align:right;"> GA_samp </th>
   <th style="text-align:right;"> response </th>
   <th style="text-align:right;"> SE </th>
   <th style="text-align:right;"> df </th>
   <th style="text-align:right;"> asymp.LCL </th>
   <th style="text-align:right;"> asymp.UCL </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td style="text-align:left;"> SCOPE </td>
   <td style="text-align:right;"> 10 </td>
   <td style="text-align:right;"> 18.76364 </td>
   <td style="text-align:right;"> 4.2175619 </td>
   <td style="text-align:right;"> Inf </td>
   <td style="text-align:right;"> 12.07786 </td>
   <td style="text-align:right;"> 29.15039 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> STOP </td>
   <td style="text-align:right;"> 10 </td>
   <td style="text-align:right;"> 11.15307 </td>
   <td style="text-align:right;"> 0.3824004 </td>
   <td style="text-align:right;"> Inf </td>
   <td style="text-align:right;"> 10.42821 </td>
   <td style="text-align:right;"> 11.92832 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> SCOPE </td>
   <td style="text-align:right;"> 16 </td>
   <td style="text-align:right;"> 14.99829 </td>
   <td style="text-align:right;"> 0.6087778 </td>
   <td style="text-align:right;"> Inf </td>
   <td style="text-align:right;"> 13.85134 </td>
   <td style="text-align:right;"> 16.24022 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> STOP </td>
   <td style="text-align:right;"> 16 </td>
   <td style="text-align:right;"> 12.64918 </td>
   <td style="text-align:right;"> 0.9369103 </td>
   <td style="text-align:right;"> Inf </td>
   <td style="text-align:right;"> 10.93993 </td>
   <td style="text-align:right;"> 14.62547 </td>
  </tr>
</tbody>
</table>

<b> HOMA.IR </b><table class=" lightable-classic" style='font-size: 16px; font-family: "Arial Narrow", "Source Sans Pro", sans-serif; width: auto !important; '>
 <thead>
  <tr>
   <th style="text-align:left;"> Study </th>
   <th style="text-align:right;"> GA_samp </th>
   <th style="text-align:right;"> response </th>
   <th style="text-align:right;"> SE </th>
   <th style="text-align:right;"> df </th>
   <th style="text-align:right;"> asymp.LCL </th>
   <th style="text-align:right;"> asymp.UCL </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td style="text-align:left;"> SCOPE </td>
   <td style="text-align:right;"> 10 </td>
   <td style="text-align:right;"> 4.711398 </td>
   <td style="text-align:right;"> 1.0994442 </td>
   <td style="text-align:right;"> Inf </td>
   <td style="text-align:right;"> 2.982049 </td>
   <td style="text-align:right;"> 7.443630 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> STOP </td>
   <td style="text-align:right;"> 10 </td>
   <td style="text-align:right;"> 2.360383 </td>
   <td style="text-align:right;"> 0.0854038 </td>
   <td style="text-align:right;"> Inf </td>
   <td style="text-align:right;"> 2.198792 </td>
   <td style="text-align:right;"> 2.533849 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> SCOPE </td>
   <td style="text-align:right;"> 16 </td>
   <td style="text-align:right;"> 3.604846 </td>
   <td style="text-align:right;"> 0.1557167 </td>
   <td style="text-align:right;"> Inf </td>
   <td style="text-align:right;"> 3.312209 </td>
   <td style="text-align:right;"> 3.923337 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> STOP </td>
   <td style="text-align:right;"> 16 </td>
   <td style="text-align:right;"> 2.633698 </td>
   <td style="text-align:right;"> 0.2057485 </td>
   <td style="text-align:right;"> Inf </td>
   <td style="text-align:right;"> 2.259794 </td>
   <td style="text-align:right;"> 3.069469 </td>
  </tr>
</tbody>
</table>


### Comparisons
<table class=" lightable-classic" style='font-size: 16px; font-family: "Arial Narrow", "Source Sans Pro", sans-serif; width: auto !important; '>
 <thead>
  <tr>
   <th style="text-align:left;"> Hormone </th>
   <th style="text-align:left;"> Contrast </th>
   <th style="text-align:left;"> Ratio of Geometric means (95% CI) </th>
   <th style="text-align:left;"> P-value </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td style="text-align:left;"> Insulin </td>
   <td style="text-align:left;"> STOP / SCOPE </td>
   <td style="text-align:left;"> 0.59 (0.38, 0.93) </td>
   <td style="text-align:left;"> 0.02 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Insulin </td>
   <td style="text-align:left;"> STOP / SCOPE </td>
   <td style="text-align:left;"> 0.84 (0.71, 1.00) </td>
   <td style="text-align:left;"> 0.04 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> HOMA.IR </td>
   <td style="text-align:left;"> STOP / SCOPE </td>
   <td style="text-align:left;"> 0.50 (0.32, 0.80) </td>
   <td style="text-align:left;"> 0.003 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> HOMA.IR </td>
   <td style="text-align:left;"> STOP / SCOPE </td>
   <td style="text-align:left;"> 0.73 (0.61, 0.87) </td>
   <td style="text-align:left;"> 0.0004 </td>
  </tr>
</tbody>
</table>

<img src="04-2_Insulin_models_files/figure-html/em_plots-1.png" width="672" /><img src="04-2_Insulin_models_files/figure-html/em_plots-2.png" width="672" />

### Plots for GA
<img src="04-2_Insulin_models_files/figure-html/em_plots2-1.png" width="960" /><img src="04-2_Insulin_models_files/figure-html/em_plots2-2.png" width="960" />

# Session info
**Results generated on: 2023-04-28 13:36:20**
<details><summary>Click for more details</summary>

```r
sessionInfo()
```

```
## R version 4.2.3 (2023-03-15)
## Platform: x86_64-pc-linux-gnu (64-bit)
## Running under: Ubuntu 22.04.2 LTS
## 
## Matrix products: default
## BLAS:   /usr/lib/x86_64-linux-gnu/openblas-pthread/libblas.so.3
## LAPACK: /usr/lib/x86_64-linux-gnu/openblas-pthread/libopenblasp-r0.3.20.so
## 
## locale:
##  [1] LC_CTYPE=en_AU.UTF-8          LC_NUMERIC=C                 
##  [3] LC_TIME=en_AU.UTF-8           LC_COLLATE=en_AU.UTF-8       
##  [5] LC_MONETARY=en_AU.UTF-8       LC_MESSAGES=en_AU.UTF-8      
##  [7] LC_PAPER=en_AU.UTF-8          LC_NAME=en_AU.UTF-8          
##  [9] LC_ADDRESS=en_AU.UTF-8        LC_TELEPHONE=en_AU.UTF-8     
## [11] LC_MEASUREMENT=en_AU.UTF-8    LC_IDENTIFICATION=en_AU.UTF-8
## 
## attached base packages:
## [1] parallel  grid      stats     graphics  grDevices utils     datasets 
## [8] methods   base     
## 
## other attached packages:
##  [1] xlsx_0.6.5        doParallel_1.0.17 iterators_1.0.14  foreach_1.5.2    
##  [5] ggpubr_0.6.0      car_3.1-2         carData_3.0-5     emmeans_1.8.5    
##  [9] geepack_1.3.9     readxl_1.4.2      Hmisc_5.0-1       htmlwidgets_1.6.2
## [13] kableExtra_1.3.4  knitr_1.42        rmarkdown_2.21    ggplot2_3.4.2    
## [17] devtools_2.4.5    usethis_2.1.6     pander_0.6.5      magrittr_2.0.3   
## [21] gridExtra_2.3     nvimcom_0.9-75   
## 
## loaded via a namespace (and not attached):
##   [1] TH.data_1.1-2      colorspace_2.1-0   ggsignif_0.6.4    
##   [4] ellipsis_0.3.2     estimability_1.4.1 htmlTable_2.4.1   
##   [7] base64enc_0.1-3    fs_1.6.1           rstudioapi_0.14   
##  [10] farver_2.1.1       remotes_2.4.2      fansi_1.0.4       
##  [13] mvtnorm_1.1-3      xml2_1.3.3         codetools_0.2-19  
##  [16] splines_4.2.3      cachem_1.0.7       pkgload_1.3.2     
##  [19] Formula_1.2-5      jsonlite_1.8.4     rJava_1.0-6       
##  [22] broom_1.0.4        cluster_2.1.4      shiny_1.7.4       
##  [25] compiler_4.2.3     httr_1.4.5         backports_1.4.1   
##  [28] Matrix_1.5-4       fastmap_1.1.1      cli_3.6.1         
##  [31] later_1.3.0        htmltools_0.5.5    prettyunits_1.1.1 
##  [34] tools_4.2.3        coda_0.19-4        gtable_0.3.3      
##  [37] glue_1.6.2         dplyr_1.1.2        Rcpp_1.0.10       
##  [40] cellranger_1.1.0   jquerylib_0.1.4    vctrs_0.6.2       
##  [43] nlme_3.1-162       svglite_2.1.1      xfun_0.39         
##  [46] stringr_1.5.0      xlsxjars_0.6.1     ps_1.7.5          
##  [49] rvest_1.0.3        mime_0.12          miniUI_0.1.1.1    
##  [52] lifecycle_1.0.3    rstatix_0.7.2      MASS_7.3-58.3     
##  [55] zoo_1.8-12         scales_1.2.1       promises_1.2.0.1  
##  [58] sandwich_3.0-2     yaml_2.3.7         memoise_2.0.1     
##  [61] sass_0.4.5         rpart_4.1.19       stringi_1.7.12    
##  [64] highr_0.10         checkmate_2.1.0    pkgbuild_1.4.0    
##  [67] rlang_1.1.0        pkgconfig_2.0.3    systemfonts_1.0.4 
##  [70] evaluate_0.20      lattice_0.21-8     purrr_1.0.1       
##  [73] labeling_0.4.2     processx_3.8.1     tidyselect_1.2.0  
##  [76] bookdown_0.33      R6_2.5.1           generics_0.1.3    
##  [79] profvis_0.3.7      multcomp_1.4-23    mgcv_1.8-42       
##  [82] pillar_1.9.0       foreign_0.8-84     withr_2.5.0       
##  [85] survival_3.5-5     abind_1.4-5        nnet_7.3-18       
##  [88] tibble_3.2.1       crayon_1.5.2       utf8_1.2.3        
##  [91] urlchecker_1.0.1   data.table_1.14.8  callr_3.7.3       
##  [94] digest_0.6.31      webshot_0.5.4      xtable_1.8-4      
##  [97] tidyr_1.3.0        httpuv_1.6.9       munsell_0.5.0     
## [100] viridisLite_0.4.1  bslib_0.4.2        sessioninfo_1.2.2
```
</details>


