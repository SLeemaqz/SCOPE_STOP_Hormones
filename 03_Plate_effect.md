<!-- Environment -->


# Plate Effect

This section explores the Plate effect on hormone levels.

- <b>Outcomes: </b> Prolactin, hPL, GH2 (all outcomes log-transformed) <br />
- <b>Independent variables:</b> Plate + Study, BMI, GA at sampling <br />
- <b>Model fitted:</b> LME model <br/>
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;log(hormones) ~ Plate + Study + BMI + GA at sampling<br />
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Random intercepts for Study ID<br />

`<svg aria-hidden="true" role="img" viewBox="0 0 512 512" style="height:1em;width:1em;vertical-align:-0.125em;margin-left:auto;margin-right:auto;font-size:inherit;fill:red;overflow:visible;position:relative;"><path d="M256 512A256 256 0 1 0 256 0a256 256 0 1 0 0 512zm0-384c13.3 0 24 10.7 24 24V264c0 13.3-10.7 24-24 24s-24-10.7-24-24V152c0-13.3 10.7-24 24-24zM224 352a32 32 0 1 1 64 0 32 32 0 1 1 -64 0z"/></svg>`{=html} <span style="color:red;"><b>There is evidence of a Plate effect and it will be adjusted for (as a random effect) in the analyses.</b></span><br />






<!-- Read data -->




<!-- Plate models -->



## Prolactin


<img src="03_Plate_effect_files/figure-html/barplot-1.png" width="1440" />


<b>Type III Sum of Squares</b>
<table class=" lightable-classic" style='font-size: 18px; font-family: "Arial Narrow", "Source Sans Pro", sans-serif; width: auto !important; '>
 <thead>
  <tr>
   <th style="text-align:left;">   </th>
   <th style="text-align:right;"> Chisq </th>
   <th style="text-align:right;"> Df </th>
   <th style="text-align:left;"> Pr(&gt;Chisq) </th>
   <th style="text-align:left;">  </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td style="text-align:left;"> (Intercept) </td>
   <td style="text-align:right;"> 199.66141 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:left;"> &lt;0.0001 </td>
   <td style="text-align:left;"> *** </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.Prolactin </td>
   <td style="text-align:right;"> 3242.32129 </td>
   <td style="text-align:right;"> 56 </td>
   <td style="text-align:left;"> &lt;0.0001 </td>
   <td style="text-align:left;"> *** </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Study </td>
   <td style="text-align:right;"> 0.39792 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:left;"> 0.5 </td>
   <td style="text-align:left;"> ns </td>
  </tr>
  <tr>
   <td style="text-align:left;"> BMI </td>
   <td style="text-align:right;"> 20.34960 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:left;"> &lt;0.0001 </td>
   <td style="text-align:left;"> *** </td>
  </tr>
  <tr>
   <td style="text-align:left;"> GA_samp </td>
   <td style="text-align:right;"> 243.34574 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:left;"> &lt;0.0001 </td>
   <td style="text-align:left;"> *** </td>
  </tr>
</tbody>
</table>


### Model summary
<div style="border: 1px solid #ddd; padding: 0px; overflow-y: scroll; height:500px; overflow-x: scroll; width:100%; "><table class=" lightable-classic" style='font-size: 14px; font-family: "Arial Narrow", "Source Sans Pro", sans-serif; width: auto !important; '>
 <thead>
  <tr>
   <th style="text-align:left;position: sticky; top:0; background-color: #FFFFFF;">   </th>
   <th style="text-align:right;position: sticky; top:0; background-color: #FFFFFF;"> Estimate </th>
   <th style="text-align:right;position: sticky; top:0; background-color: #FFFFFF;"> Std. Error </th>
   <th style="text-align:right;position: sticky; top:0; background-color: #FFFFFF;"> df </th>
   <th style="text-align:right;position: sticky; top:0; background-color: #FFFFFF;"> t value </th>
   <th style="text-align:left;position: sticky; top:0; background-color: #FFFFFF;"> Pr(&gt;|t|) </th>
   <th style="text-align:left;position: sticky; top:0; background-color: #FFFFFF;">  </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td style="text-align:left;"> (Intercept) </td>
   <td style="text-align:right;"> 2.7029744 </td>
   <td style="text-align:right;"> 0.1912911 </td>
   <td style="text-align:right;"> 2699.476 </td>
   <td style="text-align:right;"> 14.1301595 </td>
   <td style="text-align:left;"> &lt;0.0001 </td>
   <td style="text-align:left;"> *** </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.Prolactin1 </td>
   <td style="text-align:right;"> 0.1212429 </td>
   <td style="text-align:right;"> 0.1059894 </td>
   <td style="text-align:right;"> 2432.003 </td>
   <td style="text-align:right;"> 1.1439154 </td>
   <td style="text-align:left;"> 0.3 </td>
   <td style="text-align:left;"> ns </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.Prolactin2 </td>
   <td style="text-align:right;"> -0.1778566 </td>
   <td style="text-align:right;"> 0.1164062 </td>
   <td style="text-align:right;"> 2644.382 </td>
   <td style="text-align:right;"> -1.5278971 </td>
   <td style="text-align:left;"> 0.1 </td>
   <td style="text-align:left;"> ns </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.Prolactin3 </td>
   <td style="text-align:right;"> 0.0276810 </td>
   <td style="text-align:right;"> 0.1298168 </td>
   <td style="text-align:right;"> 2712.887 </td>
   <td style="text-align:right;"> 0.2132314 </td>
   <td style="text-align:left;"> 0.8 </td>
   <td style="text-align:left;"> ns </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.Prolactin4 </td>
   <td style="text-align:right;"> 0.6684824 </td>
   <td style="text-align:right;"> 0.1336746 </td>
   <td style="text-align:right;"> 2711.326 </td>
   <td style="text-align:right;"> 5.0008192 </td>
   <td style="text-align:left;"> &lt;0.0001 </td>
   <td style="text-align:left;"> *** </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.Prolactin5 </td>
   <td style="text-align:right;"> -2.7409455 </td>
   <td style="text-align:right;"> 0.1179895 </td>
   <td style="text-align:right;"> 2243.227 </td>
   <td style="text-align:right;"> -23.2304142 </td>
   <td style="text-align:left;"> &lt;0.0001 </td>
   <td style="text-align:left;"> *** </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.Prolactin6 </td>
   <td style="text-align:right;"> 0.6409714 </td>
   <td style="text-align:right;"> 0.1270956 </td>
   <td style="text-align:right;"> 2623.257 </td>
   <td style="text-align:right;"> 5.0432216 </td>
   <td style="text-align:left;"> &lt;0.0001 </td>
   <td style="text-align:left;"> *** </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.Prolactin7 </td>
   <td style="text-align:right;"> -0.1247035 </td>
   <td style="text-align:right;"> 0.1242381 </td>
   <td style="text-align:right;"> 2559.986 </td>
   <td style="text-align:right;"> -1.0037455 </td>
   <td style="text-align:left;"> 0.3 </td>
   <td style="text-align:left;"> ns </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.Prolactin8 </td>
   <td style="text-align:right;"> -0.0314571 </td>
   <td style="text-align:right;"> 0.1266782 </td>
   <td style="text-align:right;"> 2528.487 </td>
   <td style="text-align:right;"> -0.2483227 </td>
   <td style="text-align:left;"> 0.8 </td>
   <td style="text-align:left;"> ns </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.Prolactin9 </td>
   <td style="text-align:right;"> -0.0105195 </td>
   <td style="text-align:right;"> 0.1232303 </td>
   <td style="text-align:right;"> 2503.349 </td>
   <td style="text-align:right;"> -0.0853644 </td>
   <td style="text-align:left;"> 0.9 </td>
   <td style="text-align:left;"> ns </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.Prolactin10 </td>
   <td style="text-align:right;"> 0.1684885 </td>
   <td style="text-align:right;"> 0.1273688 </td>
   <td style="text-align:right;"> 2629.966 </td>
   <td style="text-align:right;"> 1.3228396 </td>
   <td style="text-align:left;"> 0.2 </td>
   <td style="text-align:left;"> ns </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.Prolactin11 </td>
   <td style="text-align:right;"> -0.1515120 </td>
   <td style="text-align:right;"> 0.1276569 </td>
   <td style="text-align:right;"> 2639.532 </td>
   <td style="text-align:right;"> -1.1868684 </td>
   <td style="text-align:left;"> 0.2 </td>
   <td style="text-align:left;"> ns </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.Prolactin12 </td>
   <td style="text-align:right;"> 0.0851213 </td>
   <td style="text-align:right;"> 0.1324984 </td>
   <td style="text-align:right;"> 2702.232 </td>
   <td style="text-align:right;"> 0.6424328 </td>
   <td style="text-align:left;"> 0.5 </td>
   <td style="text-align:left;"> ns </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.Prolactin13 </td>
   <td style="text-align:right;"> 0.1201180 </td>
   <td style="text-align:right;"> 0.1242124 </td>
   <td style="text-align:right;"> 2510.966 </td>
   <td style="text-align:right;"> 0.9670369 </td>
   <td style="text-align:left;"> 0.3 </td>
   <td style="text-align:left;"> ns </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.Prolactin14 </td>
   <td style="text-align:right;"> 0.3695932 </td>
   <td style="text-align:right;"> 0.1201204 </td>
   <td style="text-align:right;"> 2438.010 </td>
   <td style="text-align:right;"> 3.0768571 </td>
   <td style="text-align:left;"> 0.002 </td>
   <td style="text-align:left;"> ** </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.Prolactin15 </td>
   <td style="text-align:right;"> 0.0363681 </td>
   <td style="text-align:right;"> 0.1199989 </td>
   <td style="text-align:right;"> 2386.639 </td>
   <td style="text-align:right;"> 0.3030705 </td>
   <td style="text-align:left;"> 0.8 </td>
   <td style="text-align:left;"> ns </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.Prolactin16 </td>
   <td style="text-align:right;"> -0.1975497 </td>
   <td style="text-align:right;"> 0.1205968 </td>
   <td style="text-align:right;"> 2441.830 </td>
   <td style="text-align:right;"> -1.6381006 </td>
   <td style="text-align:left;"> 0.1 </td>
   <td style="text-align:left;"> ns </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.Prolactin17 </td>
   <td style="text-align:right;"> 0.2384564 </td>
   <td style="text-align:right;"> 0.1186976 </td>
   <td style="text-align:right;"> 2352.060 </td>
   <td style="text-align:right;"> 2.0089403 </td>
   <td style="text-align:left;"> 0.04 </td>
   <td style="text-align:left;"> \* </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.Prolactin18 </td>
   <td style="text-align:right;"> -0.0096860 </td>
   <td style="text-align:right;"> 0.1191918 </td>
   <td style="text-align:right;"> 2397.717 </td>
   <td style="text-align:right;"> -0.0812641 </td>
   <td style="text-align:left;"> 0.9 </td>
   <td style="text-align:left;"> ns </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.Prolactin19 </td>
   <td style="text-align:right;"> -0.2778632 </td>
   <td style="text-align:right;"> 0.1327844 </td>
   <td style="text-align:right;"> 1795.499 </td>
   <td style="text-align:right;"> -2.0925896 </td>
   <td style="text-align:left;"> 0.04 </td>
   <td style="text-align:left;"> \* </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.Prolactin20 </td>
   <td style="text-align:right;"> 1.3669180 </td>
   <td style="text-align:right;"> 0.1168697 </td>
   <td style="text-align:right;"> 2375.834 </td>
   <td style="text-align:right;"> 11.6960823 </td>
   <td style="text-align:left;"> &lt;0.0001 </td>
   <td style="text-align:left;"> *** </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.Prolactin21 </td>
   <td style="text-align:right;"> 0.2718832 </td>
   <td style="text-align:right;"> 0.1032018 </td>
   <td style="text-align:right;"> 2404.313 </td>
   <td style="text-align:right;"> 2.6344795 </td>
   <td style="text-align:left;"> 0.008 </td>
   <td style="text-align:left;"> ** </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.Prolactin22 </td>
   <td style="text-align:right;"> -0.0736811 </td>
   <td style="text-align:right;"> 0.1147746 </td>
   <td style="text-align:right;"> 2665.747 </td>
   <td style="text-align:right;"> -0.6419630 </td>
   <td style="text-align:left;"> 0.5 </td>
   <td style="text-align:left;"> ns </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.Prolactin23 </td>
   <td style="text-align:right;"> 0.6455957 </td>
   <td style="text-align:right;"> 0.1278116 </td>
   <td style="text-align:right;"> 2602.500 </td>
   <td style="text-align:right;"> 5.0511524 </td>
   <td style="text-align:left;"> &lt;0.0001 </td>
   <td style="text-align:left;"> *** </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.Prolactin24 </td>
   <td style="text-align:right;"> 0.4746078 </td>
   <td style="text-align:right;"> 0.1293510 </td>
   <td style="text-align:right;"> 2658.915 </td>
   <td style="text-align:right;"> 3.6691463 </td>
   <td style="text-align:left;"> 0.0002 </td>
   <td style="text-align:left;"> *** </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.Prolactin25 </td>
   <td style="text-align:right;"> 0.2473075 </td>
   <td style="text-align:right;"> 0.1337241 </td>
   <td style="text-align:right;"> 2702.103 </td>
   <td style="text-align:right;"> 1.8493859 </td>
   <td style="text-align:left;"> 0.06 </td>
   <td style="text-align:left;"> ns </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.Prolactin26 </td>
   <td style="text-align:right;"> -0.4426617 </td>
   <td style="text-align:right;"> 0.1308254 </td>
   <td style="text-align:right;"> 2707.453 </td>
   <td style="text-align:right;"> -3.3836078 </td>
   <td style="text-align:left;"> 0.0007 </td>
   <td style="text-align:left;"> *** </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.Prolactin27 </td>
   <td style="text-align:right;"> 0.0793262 </td>
   <td style="text-align:right;"> 0.1311297 </td>
   <td style="text-align:right;"> 2706.948 </td>
   <td style="text-align:right;"> 0.6049448 </td>
   <td style="text-align:left;"> 0.5 </td>
   <td style="text-align:left;"> ns </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.Prolactin28 </td>
   <td style="text-align:right;"> -0.0203714 </td>
   <td style="text-align:right;"> 0.1311472 </td>
   <td style="text-align:right;"> 2707.661 </td>
   <td style="text-align:right;"> -0.1553320 </td>
   <td style="text-align:left;"> 0.9 </td>
   <td style="text-align:left;"> ns </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.Prolactin29 </td>
   <td style="text-align:right;"> 0.5754633 </td>
   <td style="text-align:right;"> 0.1308084 </td>
   <td style="text-align:right;"> 2698.094 </td>
   <td style="text-align:right;"> 4.3992841 </td>
   <td style="text-align:left;"> &lt;0.0001 </td>
   <td style="text-align:left;"> *** </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.Prolactin30 </td>
   <td style="text-align:right;"> 0.1374354 </td>
   <td style="text-align:right;"> 0.1336598 </td>
   <td style="text-align:right;"> 2708.164 </td>
   <td style="text-align:right;"> 1.0282479 </td>
   <td style="text-align:left;"> 0.3 </td>
   <td style="text-align:left;"> ns </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.Prolactin31 </td>
   <td style="text-align:right;"> 0.7510783 </td>
   <td style="text-align:right;"> 0.1292684 </td>
   <td style="text-align:right;"> 2677.630 </td>
   <td style="text-align:right;"> 5.8102225 </td>
   <td style="text-align:left;"> &lt;0.0001 </td>
   <td style="text-align:left;"> *** </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.Prolactin32 </td>
   <td style="text-align:right;"> 0.2829795 </td>
   <td style="text-align:right;"> 0.1298106 </td>
   <td style="text-align:right;"> 2693.328 </td>
   <td style="text-align:right;"> 2.1799418 </td>
   <td style="text-align:left;"> 0.03 </td>
   <td style="text-align:left;"> \* </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.Prolactin33 </td>
   <td style="text-align:right;"> 0.2428402 </td>
   <td style="text-align:right;"> 0.1314159 </td>
   <td style="text-align:right;"> 2709.509 </td>
   <td style="text-align:right;"> 1.8478750 </td>
   <td style="text-align:left;"> 0.06 </td>
   <td style="text-align:left;"> ns </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.Prolactin34 </td>
   <td style="text-align:right;"> -0.0032740 </td>
   <td style="text-align:right;"> 0.1281654 </td>
   <td style="text-align:right;"> 2623.648 </td>
   <td style="text-align:right;"> -0.0255454 </td>
   <td style="text-align:left;"> 1.0 </td>
   <td style="text-align:left;"> ns </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.Prolactin35 </td>
   <td style="text-align:right;"> 0.0472200 </td>
   <td style="text-align:right;"> 0.1252984 </td>
   <td style="text-align:right;"> 2583.389 </td>
   <td style="text-align:right;"> 0.3768603 </td>
   <td style="text-align:left;"> 0.7 </td>
   <td style="text-align:left;"> ns </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.Prolactin36 </td>
   <td style="text-align:right;"> -0.0709905 </td>
   <td style="text-align:right;"> 0.1336269 </td>
   <td style="text-align:right;"> 2702.845 </td>
   <td style="text-align:right;"> -0.5312586 </td>
   <td style="text-align:left;"> 0.6 </td>
   <td style="text-align:left;"> ns </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.Prolactin37 </td>
   <td style="text-align:right;"> -0.0405481 </td>
   <td style="text-align:right;"> 0.1316884 </td>
   <td style="text-align:right;"> 2710.312 </td>
   <td style="text-align:right;"> -0.3079096 </td>
   <td style="text-align:left;"> 0.8 </td>
   <td style="text-align:left;"> ns </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.Prolactin38 </td>
   <td style="text-align:right;"> 0.2676561 </td>
   <td style="text-align:right;"> 0.1297542 </td>
   <td style="text-align:right;"> 2680.044 </td>
   <td style="text-align:right;"> 2.0627940 </td>
   <td style="text-align:left;"> 0.04 </td>
   <td style="text-align:left;"> \* </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.Prolactin39 </td>
   <td style="text-align:right;"> -0.1316890 </td>
   <td style="text-align:right;"> 0.1319063 </td>
   <td style="text-align:right;"> 2703.547 </td>
   <td style="text-align:right;"> -0.9983530 </td>
   <td style="text-align:left;"> 0.3 </td>
   <td style="text-align:left;"> ns </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.Prolactin40 </td>
   <td style="text-align:right;"> 0.0215482 </td>
   <td style="text-align:right;"> 0.1290479 </td>
   <td style="text-align:right;"> 2701.244 </td>
   <td style="text-align:right;"> 0.1669785 </td>
   <td style="text-align:left;"> 0.9 </td>
   <td style="text-align:left;"> ns </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.Prolactin41 </td>
   <td style="text-align:right;"> 0.1862089 </td>
   <td style="text-align:right;"> 0.1337114 </td>
   <td style="text-align:right;"> 2703.047 </td>
   <td style="text-align:right;"> 1.3926175 </td>
   <td style="text-align:left;"> 0.2 </td>
   <td style="text-align:left;"> ns </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.Prolactin42 </td>
   <td style="text-align:right;"> 0.2115212 </td>
   <td style="text-align:right;"> 0.1270103 </td>
   <td style="text-align:right;"> 2640.916 </td>
   <td style="text-align:right;"> 1.6653859 </td>
   <td style="text-align:left;"> 0.10 </td>
   <td style="text-align:left;"> ns </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.Prolactin43 </td>
   <td style="text-align:right;"> 0.3240612 </td>
   <td style="text-align:right;"> 0.1332052 </td>
   <td style="text-align:right;"> 2712.017 </td>
   <td style="text-align:right;"> 2.4327970 </td>
   <td style="text-align:left;"> 0.02 </td>
   <td style="text-align:left;"> \* </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.Prolactin44 </td>
   <td style="text-align:right;"> 0.0393886 </td>
   <td style="text-align:right;"> 0.1289286 </td>
   <td style="text-align:right;"> 2653.485 </td>
   <td style="text-align:right;"> 0.3055073 </td>
   <td style="text-align:left;"> 0.8 </td>
   <td style="text-align:left;"> ns </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.Prolactin45 </td>
   <td style="text-align:right;"> 0.1143590 </td>
   <td style="text-align:right;"> 0.1313129 </td>
   <td style="text-align:right;"> 2704.973 </td>
   <td style="text-align:right;"> 0.8708894 </td>
   <td style="text-align:left;"> 0.4 </td>
   <td style="text-align:left;"> ns </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.Prolactin46 </td>
   <td style="text-align:right;"> 0.0123467 </td>
   <td style="text-align:right;"> 0.1283756 </td>
   <td style="text-align:right;"> 2631.277 </td>
   <td style="text-align:right;"> 0.0961764 </td>
   <td style="text-align:left;"> 0.9 </td>
   <td style="text-align:left;"> ns </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.Prolactin47 </td>
   <td style="text-align:right;"> -0.2727913 </td>
   <td style="text-align:right;"> 0.1324885 </td>
   <td style="text-align:right;"> 2711.041 </td>
   <td style="text-align:right;"> -2.0589807 </td>
   <td style="text-align:left;"> 0.04 </td>
   <td style="text-align:left;"> \* </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.Prolactin48 </td>
   <td style="text-align:right;"> 0.0159011 </td>
   <td style="text-align:right;"> 0.1312939 </td>
   <td style="text-align:right;"> 2699.744 </td>
   <td style="text-align:right;"> 0.1211109 </td>
   <td style="text-align:left;"> 0.9 </td>
   <td style="text-align:left;"> ns </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.Prolactin49 </td>
   <td style="text-align:right;"> 0.2076152 </td>
   <td style="text-align:right;"> 0.1333566 </td>
   <td style="text-align:right;"> 2710.643 </td>
   <td style="text-align:right;"> 1.5568428 </td>
   <td style="text-align:left;"> 0.1 </td>
   <td style="text-align:left;"> ns </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.Prolactin50 </td>
   <td style="text-align:right;"> 0.1781638 </td>
   <td style="text-align:right;"> 0.1281007 </td>
   <td style="text-align:right;"> 2644.721 </td>
   <td style="text-align:right;"> 1.3908105 </td>
   <td style="text-align:left;"> 0.2 </td>
   <td style="text-align:left;"> ns </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.Prolactin51 </td>
   <td style="text-align:right;"> 0.2760667 </td>
   <td style="text-align:right;"> 0.1314998 </td>
   <td style="text-align:right;"> 2708.357 </td>
   <td style="text-align:right;"> 2.0993701 </td>
   <td style="text-align:left;"> 0.04 </td>
   <td style="text-align:left;"> \* </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.Prolactin52 </td>
   <td style="text-align:right;"> -0.0623079 </td>
   <td style="text-align:right;"> 0.1305366 </td>
   <td style="text-align:right;"> 2691.379 </td>
   <td style="text-align:right;"> -0.4773213 </td>
   <td style="text-align:left;"> 0.6 </td>
   <td style="text-align:left;"> ns </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.Prolactin54 </td>
   <td style="text-align:right;"> 0.2941893 </td>
   <td style="text-align:right;"> 0.1280834 </td>
   <td style="text-align:right;"> 2674.690 </td>
   <td style="text-align:right;"> 2.2968568 </td>
   <td style="text-align:left;"> 0.02 </td>
   <td style="text-align:left;"> \* </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.Prolactin55 </td>
   <td style="text-align:right;"> 0.2087797 </td>
   <td style="text-align:right;"> 0.1280497 </td>
   <td style="text-align:right;"> 2674.447 </td>
   <td style="text-align:right;"> 1.6304584 </td>
   <td style="text-align:left;"> 0.1 </td>
   <td style="text-align:left;"> ns </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.Prolactin56 </td>
   <td style="text-align:right;"> 0.2677806 </td>
   <td style="text-align:right;"> 0.1346602 </td>
   <td style="text-align:right;"> 2684.107 </td>
   <td style="text-align:right;"> 1.9885660 </td>
   <td style="text-align:left;"> 0.05 </td>
   <td style="text-align:left;"> ns </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.Prolactin57 </td>
   <td style="text-align:right;"> 1.2168334 </td>
   <td style="text-align:right;"> 0.1401107 </td>
   <td style="text-align:right;"> 2695.656 </td>
   <td style="text-align:right;"> 8.6848013 </td>
   <td style="text-align:left;"> &lt;0.0001 </td>
   <td style="text-align:left;"> *** </td>
  </tr>
  <tr>
   <td style="text-align:left;"> StudySTOP </td>
   <td style="text-align:right;"> 0.0301960 </td>
   <td style="text-align:right;"> 0.0478687 </td>
   <td style="text-align:right;"> 2710.543 </td>
   <td style="text-align:right;"> 0.6308090 </td>
   <td style="text-align:left;"> 0.5 </td>
   <td style="text-align:left;"> ns </td>
  </tr>
  <tr>
   <td style="text-align:left;"> BMI </td>
   <td style="text-align:right;"> -0.0089192 </td>
   <td style="text-align:right;"> 0.0019772 </td>
   <td style="text-align:right;"> 2628.076 </td>
   <td style="text-align:right;"> -4.5110530 </td>
   <td style="text-align:left;"> &lt;0.0001 </td>
   <td style="text-align:left;"> *** </td>
  </tr>
  <tr>
   <td style="text-align:left;"> GA_samp </td>
   <td style="text-align:right;"> 0.1511183 </td>
   <td style="text-align:right;"> 0.0096874 </td>
   <td style="text-align:right;"> 2707.712 </td>
   <td style="text-align:right;"> 15.5995430 </td>
   <td style="text-align:left;"> &lt;0.0001 </td>
   <td style="text-align:left;"> *** </td>
  </tr>
</tbody>
</table></div>



### Sample descriptives
<div style="border: 1px solid #ddd; padding: 0px; overflow-y: scroll; height:600px; overflow-x: scroll; width:100%; "><table class=" lightable-classic" style='font-size: 14px; font-family: "Arial Narrow", "Source Sans Pro", sans-serif; '>
 <thead>
<tr>
<th style="empty-cells: hide;position: sticky; top:0; background-color: #FFFFFF;" colspan="1"></th>
<th style="padding-bottom:0; padding-left:3px;padding-right:3px;text-align: center; position: sticky; top:0; background-color: #FFFFFF;" colspan="3"><div style="border-bottom: 1px solid #111111; margin-bottom: -1px; ">Study</div></th>
<th style="padding-bottom:0; padding-left:3px;padding-right:3px;text-align: center; position: sticky; top:0; background-color: #FFFFFF;" colspan="3"><div style="border-bottom: 1px solid #111111; margin-bottom: -1px; ">Timepoint</div></th>
<th style="padding-bottom:0; padding-left:3px;padding-right:3px;text-align: center; position: sticky; top:0; background-color: #FFFFFF;" colspan="3"><div style="border-bottom: 1px solid #111111; margin-bottom: -1px; ">Fetal sex</div></th>
</tr>
  <tr>
   <th style="text-align:left;position: sticky; top:0; background-color: #FFFFFF;">   </th>
   <th style="text-align:left;position: sticky; top:0; background-color: #FFFFFF;"> Missing </th>
   <th style="text-align:left;position: sticky; top:0; background-color: #FFFFFF;"> SCOPE </th>
   <th style="text-align:left;position: sticky; top:0; background-color: #FFFFFF;"> STOP </th>
   <th style="text-align:left;position: sticky; top:0; background-color: #FFFFFF;"> Missing </th>
   <th style="text-align:left;position: sticky; top:0; background-color: #FFFFFF;"> 12wks </th>
   <th style="text-align:left;position: sticky; top:0; background-color: #FFFFFF;"> 15wks </th>
   <th style="text-align:left;position: sticky; top:0; background-color: #FFFFFF;"> Missing </th>
   <th style="text-align:left;position: sticky; top:0; background-color: #FFFFFF;"> Male </th>
   <th style="text-align:left;position: sticky; top:0; background-color: #FFFFFF;"> Female </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td style="text-align:left;"> Plate 1 (n=206) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 206 (100.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 206 (100.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 92 (44.7) </td>
   <td style="text-align:left;"> 114 (55.3) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate 2 (n=86) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 8 (9.3) </td>
   <td style="text-align:left;"> 78 (90.7) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 86 (100.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 63 (73.3) </td>
   <td style="text-align:left;"> 23 (26.7) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate 3 (n=49) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 5 (10.2) </td>
   <td style="text-align:left;"> 44 (89.8) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 49 (100.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 29 (59.2) </td>
   <td style="text-align:left;"> 20 (40.8) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate 4 (n=43) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 5 (11.6) </td>
   <td style="text-align:left;"> 38 (88.4) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 43 (100.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 23 (53.5) </td>
   <td style="text-align:left;"> 20 (46.5) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate 5 (n=45) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 5 (11.1) </td>
   <td style="text-align:left;"> 40 (88.9) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 45 (100.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 25 (55.6) </td>
   <td style="text-align:left;"> 20 (44.4) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate 6 (n=45) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 5 (11.1) </td>
   <td style="text-align:left;"> 40 (88.9) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 45 (100.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 16 (35.6) </td>
   <td style="text-align:left;"> 29 (64.4) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate 7 (n=48) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 8 (16.7) </td>
   <td style="text-align:left;"> 40 (83.3) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 48 (100.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 34 (70.8) </td>
   <td style="text-align:left;"> 14 (29.2) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate 8 (n=40) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 5 (12.5) </td>
   <td style="text-align:left;"> 35 (87.5) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 40 (100.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 18 (45.0) </td>
   <td style="text-align:left;"> 22 (55.0) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate 9 (n=48) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 8 (16.7) </td>
   <td style="text-align:left;"> 40 (83.3) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 48 (100.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 27 (56.2) </td>
   <td style="text-align:left;"> 21 (43.8) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate 10 (n=44) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 6 (13.6) </td>
   <td style="text-align:left;"> 38 (86.4) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 44 (100.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 20 (45.5) </td>
   <td style="text-align:left;"> 24 (54.5) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate 11 (n=44) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 4 (9.1) </td>
   <td style="text-align:left;"> 40 (90.9) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 44 (100.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 14 (31.8) </td>
   <td style="text-align:left;"> 30 (68.2) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate 12 (n=41) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 4 (9.8) </td>
   <td style="text-align:left;"> 37 (90.2) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 41 (100.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 18 (43.9) </td>
   <td style="text-align:left;"> 23 (56.1) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate 13 (n=46) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 4 (8.7) </td>
   <td style="text-align:left;"> 42 (91.3) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 46 (100.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 23 (50.0) </td>
   <td style="text-align:left;"> 23 (50.0) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate 14 (n=50) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 4 (8.0) </td>
   <td style="text-align:left;"> 46 (92.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 50 (100.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 26 (52.0) </td>
   <td style="text-align:left;"> 24 (48.0) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate 15 (n=48) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 4 (8.3) </td>
   <td style="text-align:left;"> 44 (91.7) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 48 (100.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 30 (62.5) </td>
   <td style="text-align:left;"> 18 (37.5) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate 16 (n=50) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 4 (8.0) </td>
   <td style="text-align:left;"> 46 (92.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 50 (100.0) </td>
   <td style="text-align:left;"> 1 (2.0) </td>
   <td style="text-align:left;"> 26 (52.0) </td>
   <td style="text-align:left;"> 23 (46.0) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate 17 (n=50) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 4 (8.0) </td>
   <td style="text-align:left;"> 46 (92.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 50 (100.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 15 (30.0) </td>
   <td style="text-align:left;"> 35 (70.0) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate 18 (n=51) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 27 (52.9) </td>
   <td style="text-align:left;"> 24 (47.1) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 17 (33.3) </td>
   <td style="text-align:left;"> 34 (66.7) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 24 (47.1) </td>
   <td style="text-align:left;"> 27 (52.9) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate 19 (n=24) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 23 (95.8) </td>
   <td style="text-align:left;"> 1 (4.2) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 14 (58.3) </td>
   <td style="text-align:left;"> 10 (41.7) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 7 (29.2) </td>
   <td style="text-align:left;"> 17 (70.8) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate 20 (n=53) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 15 (28.3) </td>
   <td style="text-align:left;"> 38 (71.7) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 53 (100.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 34 (64.2) </td>
   <td style="text-align:left;"> 19 (35.8) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate 21 (n=130) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 29 (22.3) </td>
   <td style="text-align:left;"> 101 (77.7) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 130 (100.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 56 (43.1) </td>
   <td style="text-align:left;"> 74 (56.9) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate 22 (n=112) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 44 (39.3) </td>
   <td style="text-align:left;"> 68 (60.7) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 112 (100.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 72 (64.3) </td>
   <td style="text-align:left;"> 40 (35.7) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate 23 (n=42) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 15 (35.7) </td>
   <td style="text-align:left;"> 27 (64.3) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 42 (100.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 21 (50.0) </td>
   <td style="text-align:left;"> 21 (50.0) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate 24 (n=40) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 15 (37.5) </td>
   <td style="text-align:left;"> 25 (62.5) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 40 (100.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 28 (70.0) </td>
   <td style="text-align:left;"> 12 (30.0) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate 25 (n=40) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 26 (65.0) </td>
   <td style="text-align:left;"> 14 (35.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 40 (100.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 21 (52.5) </td>
   <td style="text-align:left;"> 19 (47.5) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate 26 (n=40) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 23 (57.5) </td>
   <td style="text-align:left;"> 17 (42.5) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 40 (100.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 24 (60.0) </td>
   <td style="text-align:left;"> 16 (40.0) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate 27 (n=40) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 23 (57.5) </td>
   <td style="text-align:left;"> 17 (42.5) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 40 (100.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 24 (60.0) </td>
   <td style="text-align:left;"> 16 (40.0) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate 28 (n=40) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 18 (45.0) </td>
   <td style="text-align:left;"> 22 (55.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 40 (100.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 17 (42.5) </td>
   <td style="text-align:left;"> 23 (57.5) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate 29 (n=40) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 21 (52.5) </td>
   <td style="text-align:left;"> 19 (47.5) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 40 (100.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 13 (32.5) </td>
   <td style="text-align:left;"> 27 (67.5) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate 30 (n=46) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 26 (56.5) </td>
   <td style="text-align:left;"> 20 (43.5) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 46 (100.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 22 (47.8) </td>
   <td style="text-align:left;"> 24 (52.2) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate 31 (n=40) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 17 (42.5) </td>
   <td style="text-align:left;"> 23 (57.5) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 40 (100.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 25 (62.5) </td>
   <td style="text-align:left;"> 15 (37.5) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate 32 (n=40) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 30 (75.0) </td>
   <td style="text-align:left;"> 10 (25.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 40 (100.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 21 (52.5) </td>
   <td style="text-align:left;"> 19 (47.5) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate 33 (n=40) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 18 (45.0) </td>
   <td style="text-align:left;"> 22 (55.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 40 (100.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 23 (57.5) </td>
   <td style="text-align:left;"> 17 (42.5) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate 34 (n=40) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 25 (62.5) </td>
   <td style="text-align:left;"> 15 (37.5) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 40 (100.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 21 (52.5) </td>
   <td style="text-align:left;"> 19 (47.5) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate 35 (n=44) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 29 (65.9) </td>
   <td style="text-align:left;"> 15 (34.1) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 44 (100.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 24 (54.5) </td>
   <td style="text-align:left;"> 20 (45.5) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate 36 (n=40) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 23 (57.5) </td>
   <td style="text-align:left;"> 17 (42.5) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 40 (100.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 17 (42.5) </td>
   <td style="text-align:left;"> 23 (57.5) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate 37 (n=40) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 24 (60.0) </td>
   <td style="text-align:left;"> 16 (40.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 40 (100.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 21 (52.5) </td>
   <td style="text-align:left;"> 19 (47.5) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate 38 (n=40) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 22 (55.0) </td>
   <td style="text-align:left;"> 18 (45.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 40 (100.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 18 (45.0) </td>
   <td style="text-align:left;"> 22 (55.0) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate 39 (n=40) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 20 (50.0) </td>
   <td style="text-align:left;"> 20 (50.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 40 (100.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 24 (60.0) </td>
   <td style="text-align:left;"> 16 (40.0) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate 40 (n=43) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 28 (65.1) </td>
   <td style="text-align:left;"> 15 (34.9) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 43 (100.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 17 (39.5) </td>
   <td style="text-align:left;"> 26 (60.5) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate 41 (n=40) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 21 (52.5) </td>
   <td style="text-align:left;"> 19 (47.5) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 40 (100.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 12 (30.0) </td>
   <td style="text-align:left;"> 28 (70.0) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate 42 (n=43) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 23 (53.5) </td>
   <td style="text-align:left;"> 20 (46.5) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 43 (100.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 17 (39.5) </td>
   <td style="text-align:left;"> 26 (60.5) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate 43 (n=40) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 14 (35.0) </td>
   <td style="text-align:left;"> 26 (65.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 40 (100.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 24 (60.0) </td>
   <td style="text-align:left;"> 16 (40.0) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate 44 (n=40) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 24 (60.0) </td>
   <td style="text-align:left;"> 16 (40.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 40 (100.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 19 (47.5) </td>
   <td style="text-align:left;"> 21 (52.5) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate 45 (n=40) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 17 (42.5) </td>
   <td style="text-align:left;"> 23 (57.5) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 40 (100.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 18 (45.0) </td>
   <td style="text-align:left;"> 22 (55.0) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate 46 (n=40) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 21 (52.5) </td>
   <td style="text-align:left;"> 19 (47.5) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 40 (100.0) </td>
   <td style="text-align:left;"> 1 (2.5) </td>
   <td style="text-align:left;"> 23 (57.5) </td>
   <td style="text-align:left;"> 16 (40.0) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate 47 (n=40) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 18 (45.0) </td>
   <td style="text-align:left;"> 22 (55.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 40 (100.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 18 (45.0) </td>
   <td style="text-align:left;"> 22 (55.0) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate 48 (n=40) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 23 (57.5) </td>
   <td style="text-align:left;"> 17 (42.5) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 40 (100.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 24 (60.0) </td>
   <td style="text-align:left;"> 16 (40.0) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate 49 (n=46) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 28 (60.9) </td>
   <td style="text-align:left;"> 18 (39.1) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 46 (100.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 28 (60.9) </td>
   <td style="text-align:left;"> 18 (39.1) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate 50 (n=40) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 21 (52.5) </td>
   <td style="text-align:left;"> 19 (47.5) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 40 (100.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 13 (32.5) </td>
   <td style="text-align:left;"> 27 (67.5) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate 51 (n=40) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 20 (50.0) </td>
   <td style="text-align:left;"> 20 (50.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 40 (100.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 22 (55.0) </td>
   <td style="text-align:left;"> 18 (45.0) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate 52 (n=40) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 21 (52.5) </td>
   <td style="text-align:left;"> 19 (47.5) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 40 (100.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 18 (45.0) </td>
   <td style="text-align:left;"> 22 (55.0) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate 53 (n=40) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 28 (70.0) </td>
   <td style="text-align:left;"> 12 (30.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 40 (100.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 22 (55.0) </td>
   <td style="text-align:left;"> 18 (45.0) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate 54 (n=43) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 29 (67.4) </td>
   <td style="text-align:left;"> 14 (32.6) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 43 (100.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 22 (51.2) </td>
   <td style="text-align:left;"> 21 (48.8) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate 55 (n=43) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 26 (60.5) </td>
   <td style="text-align:left;"> 17 (39.5) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 43 (100.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 28 (65.1) </td>
   <td style="text-align:left;"> 15 (34.9) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate 56 (n=40) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 18 (45.0) </td>
   <td style="text-align:left;"> 22 (55.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 40 (100.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 20 (50.0) </td>
   <td style="text-align:left;"> 20 (50.0) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate 57 (n=33) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 19 (57.6) </td>
   <td style="text-align:left;"> 14 (42.4) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 33 (100.0) </td>
   <td style="text-align:left;"> 3 (9.1) </td>
   <td style="text-align:left;"> 17 (51.5) </td>
   <td style="text-align:left;"> 13 (39.4) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate Total (n=2776) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 1201 (43.3) </td>
   <td style="text-align:left;"> 1575 (56.7) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 31 (1.1) </td>
   <td style="text-align:left;"> 2745 (98.9) </td>
   <td style="text-align:left;"> 5 (0.2) </td>
   <td style="text-align:left;"> 1418 (51.1) </td>
   <td style="text-align:left;"> 1353 (48.7) </td>
  </tr>
</tbody>
</table></div>


## HPL
<img src="03_Plate_effect_files/figure-html/unnamed-chunk-1-1.png" width="1440" />
<b>Type III Sum of Squares</b>
<table class=" lightable-classic" style='font-size: 18px; font-family: "Arial Narrow", "Source Sans Pro", sans-serif; width: auto !important; '>
 <thead>
  <tr>
   <th style="text-align:left;">   </th>
   <th style="text-align:right;"> Chisq </th>
   <th style="text-align:right;"> Df </th>
   <th style="text-align:left;"> Pr(&gt;Chisq) </th>
   <th style="text-align:left;">  </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td style="text-align:left;"> (Intercept) </td>
   <td style="text-align:right;"> 89.04744 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:left;"> &lt;0.0001 </td>
   <td style="text-align:left;"> *** </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.HPL </td>
   <td style="text-align:right;"> 738.44227 </td>
   <td style="text-align:right;"> 56 </td>
   <td style="text-align:left;"> &lt;0.0001 </td>
   <td style="text-align:left;"> *** </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Study </td>
   <td style="text-align:right;"> 12.65682 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:left;"> 0.0004 </td>
   <td style="text-align:left;"> *** </td>
  </tr>
  <tr>
   <td style="text-align:left;"> BMI </td>
   <td style="text-align:right;"> 281.91493 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:left;"> &lt;0.0001 </td>
   <td style="text-align:left;"> *** </td>
  </tr>
  <tr>
   <td style="text-align:left;"> GA_samp </td>
   <td style="text-align:right;"> 3001.83025 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:left;"> &lt;0.0001 </td>
   <td style="text-align:left;"> *** </td>
  </tr>
</tbody>
</table>


### Model summary
<div style="border: 1px solid #ddd; padding: 0px; overflow-y: scroll; height:500px; overflow-x: scroll; width:100%; "><table class=" lightable-classic" style='font-size: 14px; font-family: "Arial Narrow", "Source Sans Pro", sans-serif; width: auto !important; '>
 <thead>
  <tr>
   <th style="text-align:left;position: sticky; top:0; background-color: #FFFFFF;">   </th>
   <th style="text-align:right;position: sticky; top:0; background-color: #FFFFFF;"> Estimate </th>
   <th style="text-align:right;position: sticky; top:0; background-color: #FFFFFF;"> Std. Error </th>
   <th style="text-align:right;position: sticky; top:0; background-color: #FFFFFF;"> df </th>
   <th style="text-align:right;position: sticky; top:0; background-color: #FFFFFF;"> t value </th>
   <th style="text-align:left;position: sticky; top:0; background-color: #FFFFFF;"> Pr(&gt;|t|) </th>
   <th style="text-align:left;position: sticky; top:0; background-color: #FFFFFF;">  </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td style="text-align:left;"> (Intercept) </td>
   <td style="text-align:right;"> 0.9918178 </td>
   <td style="text-align:right;"> 0.1051045 </td>
   <td style="text-align:right;"> 2533.466 </td>
   <td style="text-align:right;"> 9.4364953 </td>
   <td style="text-align:left;"> &lt;0.0001 </td>
   <td style="text-align:left;"> *** </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.HPL1 </td>
   <td style="text-align:right;"> 0.0921711 </td>
   <td style="text-align:right;"> 0.0606656 </td>
   <td style="text-align:right;"> 2625.550 </td>
   <td style="text-align:right;"> 1.5193305 </td>
   <td style="text-align:left;"> 0.1 </td>
   <td style="text-align:left;"> ns </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.HPL2 </td>
   <td style="text-align:right;"> 0.2305057 </td>
   <td style="text-align:right;"> 0.0664929 </td>
   <td style="text-align:right;"> 2693.257 </td>
   <td style="text-align:right;"> 3.4666206 </td>
   <td style="text-align:left;"> 0.0005 </td>
   <td style="text-align:left;"> *** </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.HPL3 </td>
   <td style="text-align:right;"> 0.0324389 </td>
   <td style="text-align:right;"> 0.0715481 </td>
   <td style="text-align:right;"> 2652.110 </td>
   <td style="text-align:right;"> 0.4533860 </td>
   <td style="text-align:left;"> 0.7 </td>
   <td style="text-align:left;"> ns </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.HPL4 </td>
   <td style="text-align:right;"> 0.0768561 </td>
   <td style="text-align:right;"> 0.0735279 </td>
   <td style="text-align:right;"> 2622.508 </td>
   <td style="text-align:right;"> 1.0452644 </td>
   <td style="text-align:left;"> 0.3 </td>
   <td style="text-align:left;"> ns </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.HPL5 </td>
   <td style="text-align:right;"> 0.1891226 </td>
   <td style="text-align:right;"> 0.0678734 </td>
   <td style="text-align:right;"> 2497.891 </td>
   <td style="text-align:right;"> 2.7864029 </td>
   <td style="text-align:left;"> 0.005 </td>
   <td style="text-align:left;"> ** </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.HPL6 </td>
   <td style="text-align:right;"> 0.2354691 </td>
   <td style="text-align:right;"> 0.0716632 </td>
   <td style="text-align:right;"> 2692.436 </td>
   <td style="text-align:right;"> 3.2857748 </td>
   <td style="text-align:left;"> 0.001 </td>
   <td style="text-align:left;"> ** </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.HPL7 </td>
   <td style="text-align:right;"> -0.0648563 </td>
   <td style="text-align:right;"> 0.0703540 </td>
   <td style="text-align:right;"> 2693.768 </td>
   <td style="text-align:right;"> -0.9218564 </td>
   <td style="text-align:left;"> 0.4 </td>
   <td style="text-align:left;"> ns </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.HPL8 </td>
   <td style="text-align:right;"> 0.2909962 </td>
   <td style="text-align:right;"> 0.0722893 </td>
   <td style="text-align:right;"> 2693.732 </td>
   <td style="text-align:right;"> 4.0254407 </td>
   <td style="text-align:left;"> &lt;0.0001 </td>
   <td style="text-align:left;"> *** </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.HPL9 </td>
   <td style="text-align:right;"> 0.0574963 </td>
   <td style="text-align:right;"> 0.0703906 </td>
   <td style="text-align:right;"> 2690.741 </td>
   <td style="text-align:right;"> 0.8168175 </td>
   <td style="text-align:left;"> 0.4 </td>
   <td style="text-align:left;"> ns </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.HPL10 </td>
   <td style="text-align:right;"> 0.0977651 </td>
   <td style="text-align:right;"> 0.0719626 </td>
   <td style="text-align:right;"> 2689.477 </td>
   <td style="text-align:right;"> 1.3585548 </td>
   <td style="text-align:left;"> 0.2 </td>
   <td style="text-align:left;"> ns </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.HPL11 </td>
   <td style="text-align:right;"> 0.1245978 </td>
   <td style="text-align:right;"> 0.0718970 </td>
   <td style="text-align:right;"> 2684.512 </td>
   <td style="text-align:right;"> 1.7330032 </td>
   <td style="text-align:left;"> 0.08 </td>
   <td style="text-align:left;"> ns </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.HPL12 </td>
   <td style="text-align:right;"> 0.2577725 </td>
   <td style="text-align:right;"> 0.0734449 </td>
   <td style="text-align:right;"> 2646.439 </td>
   <td style="text-align:right;"> 3.5097395 </td>
   <td style="text-align:left;"> 0.0005 </td>
   <td style="text-align:left;"> *** </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.HPL13 </td>
   <td style="text-align:right;"> 0.3311287 </td>
   <td style="text-align:right;"> 0.0709268 </td>
   <td style="text-align:right;"> 2692.442 </td>
   <td style="text-align:right;"> 4.6685975 </td>
   <td style="text-align:left;"> &lt;0.0001 </td>
   <td style="text-align:left;"> *** </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.HPL14 </td>
   <td style="text-align:right;"> 0.1470589 </td>
   <td style="text-align:right;"> 0.0691096 </td>
   <td style="text-align:right;"> 2677.509 </td>
   <td style="text-align:right;"> 2.1279094 </td>
   <td style="text-align:left;"> 0.03 </td>
   <td style="text-align:left;"> \* </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.HPL15 </td>
   <td style="text-align:right;"> 0.1324150 </td>
   <td style="text-align:right;"> 0.0693577 </td>
   <td style="text-align:right;"> 2673.204 </td>
   <td style="text-align:right;"> 1.9091614 </td>
   <td style="text-align:left;"> 0.06 </td>
   <td style="text-align:left;"> ns </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.HPL16 </td>
   <td style="text-align:right;"> 0.2984871 </td>
   <td style="text-align:right;"> 0.0693148 </td>
   <td style="text-align:right;"> 2677.391 </td>
   <td style="text-align:right;"> 4.3062555 </td>
   <td style="text-align:left;"> &lt;0.0001 </td>
   <td style="text-align:left;"> *** </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.HPL17 </td>
   <td style="text-align:right;"> -0.0358695 </td>
   <td style="text-align:right;"> 0.0686740 </td>
   <td style="text-align:right;"> 2651.758 </td>
   <td style="text-align:right;"> -0.5223152 </td>
   <td style="text-align:left;"> 0.6 </td>
   <td style="text-align:left;"> ns </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.HPL18 </td>
   <td style="text-align:right;"> 0.0544943 </td>
   <td style="text-align:right;"> 0.0644116 </td>
   <td style="text-align:right;"> 2626.621 </td>
   <td style="text-align:right;"> 0.8460317 </td>
   <td style="text-align:left;"> 0.4 </td>
   <td style="text-align:left;"> ns </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.HPL19 </td>
   <td style="text-align:right;"> 0.2686786 </td>
   <td style="text-align:right;"> 0.0990292 </td>
   <td style="text-align:right;"> 2143.426 </td>
   <td style="text-align:right;"> 2.7131257 </td>
   <td style="text-align:left;"> 0.007 </td>
   <td style="text-align:left;"> ** </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.HPL20 </td>
   <td style="text-align:right;"> -0.2121390 </td>
   <td style="text-align:right;"> 0.0631995 </td>
   <td style="text-align:right;"> 2582.169 </td>
   <td style="text-align:right;"> -3.3566574 </td>
   <td style="text-align:left;"> 0.0008 </td>
   <td style="text-align:left;"> *** </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.HPL21 </td>
   <td style="text-align:right;"> -0.1312074 </td>
   <td style="text-align:right;"> 0.0586272 </td>
   <td style="text-align:right;"> 2671.829 </td>
   <td style="text-align:right;"> -2.2379947 </td>
   <td style="text-align:left;"> 0.03 </td>
   <td style="text-align:left;"> \* </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.HPL22 </td>
   <td style="text-align:right;"> -0.0543114 </td>
   <td style="text-align:right;"> 0.0643441 </td>
   <td style="text-align:right;"> 2617.564 </td>
   <td style="text-align:right;"> -0.8440767 </td>
   <td style="text-align:left;"> 0.4 </td>
   <td style="text-align:left;"> ns </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.HPL23 </td>
   <td style="text-align:right;"> 0.7437893 </td>
   <td style="text-align:right;"> 0.0723670 </td>
   <td style="text-align:right;"> 2692.466 </td>
   <td style="text-align:right;"> 10.2780225 </td>
   <td style="text-align:left;"> &lt;0.0001 </td>
   <td style="text-align:left;"> *** </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.HPL24 </td>
   <td style="text-align:right;"> 0.0334058 </td>
   <td style="text-align:right;"> 0.0726732 </td>
   <td style="text-align:right;"> 2681.475 </td>
   <td style="text-align:right;"> 0.4596709 </td>
   <td style="text-align:left;"> 0.6 </td>
   <td style="text-align:left;"> ns </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.HPL25 </td>
   <td style="text-align:right;"> 0.6560953 </td>
   <td style="text-align:right;"> 0.0738694 </td>
   <td style="text-align:right;"> 2604.776 </td>
   <td style="text-align:right;"> 8.8818215 </td>
   <td style="text-align:left;"> &lt;0.0001 </td>
   <td style="text-align:left;"> *** </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.HPL26 </td>
   <td style="text-align:right;"> 0.0799927 </td>
   <td style="text-align:right;"> 0.0740999 </td>
   <td style="text-align:right;"> 2660.203 </td>
   <td style="text-align:right;"> 1.0795247 </td>
   <td style="text-align:left;"> 0.3 </td>
   <td style="text-align:left;"> ns </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.HPL27 </td>
   <td style="text-align:right;"> 0.1095021 </td>
   <td style="text-align:right;"> 0.0728614 </td>
   <td style="text-align:right;"> 2653.404 </td>
   <td style="text-align:right;"> 1.5028829 </td>
   <td style="text-align:left;"> 0.1 </td>
   <td style="text-align:left;"> ns </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.HPL28 </td>
   <td style="text-align:right;"> 0.0196264 </td>
   <td style="text-align:right;"> 0.0728741 </td>
   <td style="text-align:right;"> 2653.324 </td>
   <td style="text-align:right;"> 0.2693193 </td>
   <td style="text-align:left;"> 0.8 </td>
   <td style="text-align:left;"> ns </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.HPL29 </td>
   <td style="text-align:right;"> 0.1805839 </td>
   <td style="text-align:right;"> 0.0728864 </td>
   <td style="text-align:right;"> 2659.331 </td>
   <td style="text-align:right;"> 2.4776074 </td>
   <td style="text-align:left;"> 0.01 </td>
   <td style="text-align:left;"> \* </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.HPL30 </td>
   <td style="text-align:right;"> -0.0553226 </td>
   <td style="text-align:right;"> 0.0734201 </td>
   <td style="text-align:right;"> 2586.721 </td>
   <td style="text-align:right;"> -0.7535075 </td>
   <td style="text-align:left;"> 0.5 </td>
   <td style="text-align:left;"> ns </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.HPL31 </td>
   <td style="text-align:right;"> 0.1580722 </td>
   <td style="text-align:right;"> 0.0724168 </td>
   <td style="text-align:right;"> 2677.426 </td>
   <td style="text-align:right;"> 2.1828106 </td>
   <td style="text-align:left;"> 0.03 </td>
   <td style="text-align:left;"> \* </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.HPL32 </td>
   <td style="text-align:right;"> 0.3118338 </td>
   <td style="text-align:right;"> 0.0724805 </td>
   <td style="text-align:right;"> 2669.127 </td>
   <td style="text-align:right;"> 4.3023152 </td>
   <td style="text-align:left;"> &lt;0.0001 </td>
   <td style="text-align:left;"> *** </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.HPL33 </td>
   <td style="text-align:right;"> 0.1090237 </td>
   <td style="text-align:right;"> 0.0729327 </td>
   <td style="text-align:right;"> 2649.276 </td>
   <td style="text-align:right;"> 1.4948532 </td>
   <td style="text-align:left;"> 0.1 </td>
   <td style="text-align:left;"> ns </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.HPL34 </td>
   <td style="text-align:right;"> 0.1072198 </td>
   <td style="text-align:right;"> 0.0723386 </td>
   <td style="text-align:right;"> 2688.378 </td>
   <td style="text-align:right;"> 1.4821926 </td>
   <td style="text-align:left;"> 0.1 </td>
   <td style="text-align:left;"> ns </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.HPL35 </td>
   <td style="text-align:right;"> -0.1816678 </td>
   <td style="text-align:right;"> 0.0711618 </td>
   <td style="text-align:right;"> 2693.932 </td>
   <td style="text-align:right;"> -2.5528833 </td>
   <td style="text-align:left;"> 0.01 </td>
   <td style="text-align:left;"> \* </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.HPL36 </td>
   <td style="text-align:right;"> 0.0570492 </td>
   <td style="text-align:right;"> 0.0733728 </td>
   <td style="text-align:right;"> 2604.436 </td>
   <td style="text-align:right;"> 0.7775243 </td>
   <td style="text-align:left;"> 0.4 </td>
   <td style="text-align:left;"> ns </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.HPL37 </td>
   <td style="text-align:right;"> 0.1132805 </td>
   <td style="text-align:right;"> 0.0730191 </td>
   <td style="text-align:right;"> 2643.142 </td>
   <td style="text-align:right;"> 1.5513835 </td>
   <td style="text-align:left;"> 0.1 </td>
   <td style="text-align:left;"> ns </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.HPL38 </td>
   <td style="text-align:right;"> 0.3106045 </td>
   <td style="text-align:right;"> 0.0726500 </td>
   <td style="text-align:right;"> 2674.769 </td>
   <td style="text-align:right;"> 4.2753557 </td>
   <td style="text-align:left;"> &lt;0.0001 </td>
   <td style="text-align:left;"> *** </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.HPL39 </td>
   <td style="text-align:right;"> 0.1459116 </td>
   <td style="text-align:right;"> 0.0729377 </td>
   <td style="text-align:right;"> 2653.643 </td>
   <td style="text-align:right;"> 2.0004958 </td>
   <td style="text-align:left;"> 0.05 </td>
   <td style="text-align:left;"> ns </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.HPL40 </td>
   <td style="text-align:right;"> 0.0566781 </td>
   <td style="text-align:right;"> 0.0718851 </td>
   <td style="text-align:right;"> 2661.086 </td>
   <td style="text-align:right;"> 0.7884536 </td>
   <td style="text-align:left;"> 0.4 </td>
   <td style="text-align:left;"> ns </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.HPL41 </td>
   <td style="text-align:right;"> 0.1994536 </td>
   <td style="text-align:right;"> 0.0734263 </td>
   <td style="text-align:right;"> 2605.205 </td>
   <td style="text-align:right;"> 2.7163791 </td>
   <td style="text-align:left;"> 0.007 </td>
   <td style="text-align:left;"> ** </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.HPL42 </td>
   <td style="text-align:right;"> -0.0677224 </td>
   <td style="text-align:right;"> 0.0715788 </td>
   <td style="text-align:right;"> 2687.222 </td>
   <td style="text-align:right;"> -0.9461240 </td>
   <td style="text-align:left;"> 0.3 </td>
   <td style="text-align:left;"> ns </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.HPL43 </td>
   <td style="text-align:right;"> 0.2401154 </td>
   <td style="text-align:right;"> 0.0736095 </td>
   <td style="text-align:right;"> 2602.954 </td>
   <td style="text-align:right;"> 3.2620161 </td>
   <td style="text-align:left;"> 0.001 </td>
   <td style="text-align:left;"> ** </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.HPL44 </td>
   <td style="text-align:right;"> 0.1141842 </td>
   <td style="text-align:right;"> 0.0724814 </td>
   <td style="text-align:right;"> 2682.267 </td>
   <td style="text-align:right;"> 1.5753580 </td>
   <td style="text-align:left;"> 0.1 </td>
   <td style="text-align:left;"> ns </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.HPL45 </td>
   <td style="text-align:right;"> 0.1800752 </td>
   <td style="text-align:right;"> 0.0730007 </td>
   <td style="text-align:right;"> 2653.527 </td>
   <td style="text-align:right;"> 2.4667617 </td>
   <td style="text-align:left;"> 0.01 </td>
   <td style="text-align:left;"> \* </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.HPL46 </td>
   <td style="text-align:right;"> 0.1009820 </td>
   <td style="text-align:right;"> 0.0725317 </td>
   <td style="text-align:right;"> 2681.930 </td>
   <td style="text-align:right;"> 1.3922466 </td>
   <td style="text-align:left;"> 0.2 </td>
   <td style="text-align:left;"> ns </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.HPL47 </td>
   <td style="text-align:right;"> 0.2556517 </td>
   <td style="text-align:right;"> 0.0734007 </td>
   <td style="text-align:right;"> 2635.412 </td>
   <td style="text-align:right;"> 3.4829610 </td>
   <td style="text-align:left;"> 0.0005 </td>
   <td style="text-align:left;"> *** </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.HPL48 </td>
   <td style="text-align:right;"> 0.1066926 </td>
   <td style="text-align:right;"> 0.0730994 </td>
   <td style="text-align:right;"> 2653.596 </td>
   <td style="text-align:right;"> 1.4595558 </td>
   <td style="text-align:left;"> 0.1 </td>
   <td style="text-align:left;"> ns </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.HPL49 </td>
   <td style="text-align:right;"> -0.0254198 </td>
   <td style="text-align:right;"> 0.0733466 </td>
   <td style="text-align:right;"> 2592.945 </td>
   <td style="text-align:right;"> -0.3465716 </td>
   <td style="text-align:left;"> 0.7 </td>
   <td style="text-align:left;"> ns </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.HPL50 </td>
   <td style="text-align:right;"> 0.1892451 </td>
   <td style="text-align:right;"> 0.0721640 </td>
   <td style="text-align:right;"> 2687.798 </td>
   <td style="text-align:right;"> 2.6224304 </td>
   <td style="text-align:left;"> 0.009 </td>
   <td style="text-align:left;"> ** </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.HPL51 </td>
   <td style="text-align:right;"> 0.1394344 </td>
   <td style="text-align:right;"> 0.0731642 </td>
   <td style="text-align:right;"> 2634.829 </td>
   <td style="text-align:right;"> 1.9057741 </td>
   <td style="text-align:left;"> 0.06 </td>
   <td style="text-align:left;"> ns </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.HPL52 </td>
   <td style="text-align:right;"> 0.1119099 </td>
   <td style="text-align:right;"> 0.0728747 </td>
   <td style="text-align:right;"> 2665.948 </td>
   <td style="text-align:right;"> 1.5356468 </td>
   <td style="text-align:left;"> 0.1 </td>
   <td style="text-align:left;"> ns </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.HPL54 </td>
   <td style="text-align:right;"> 0.3039624 </td>
   <td style="text-align:right;"> 0.0717702 </td>
   <td style="text-align:right;"> 2675.625 </td>
   <td style="text-align:right;"> 4.2352185 </td>
   <td style="text-align:left;"> &lt;0.0001 </td>
   <td style="text-align:left;"> *** </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.HPL55 </td>
   <td style="text-align:right;"> 0.2546358 </td>
   <td style="text-align:right;"> 0.0717667 </td>
   <td style="text-align:right;"> 2676.413 </td>
   <td style="text-align:right;"> 3.5481031 </td>
   <td style="text-align:left;"> 0.0004 </td>
   <td style="text-align:left;"> *** </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.HPL56 </td>
   <td style="text-align:right;"> 0.0147899 </td>
   <td style="text-align:right;"> 0.0736068 </td>
   <td style="text-align:right;"> 2584.311 </td>
   <td style="text-align:right;"> 0.2009311 </td>
   <td style="text-align:left;"> 0.8 </td>
   <td style="text-align:left;"> ns </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.HPL57 </td>
   <td style="text-align:right;"> 0.0507690 </td>
   <td style="text-align:right;"> 0.0768536 </td>
   <td style="text-align:right;"> 2607.965 </td>
   <td style="text-align:right;"> 0.6605935 </td>
   <td style="text-align:left;"> 0.5 </td>
   <td style="text-align:left;"> ns </td>
  </tr>
  <tr>
   <td style="text-align:left;"> StudySTOP </td>
   <td style="text-align:right;"> 0.0926816 </td>
   <td style="text-align:right;"> 0.0260514 </td>
   <td style="text-align:right;"> 2576.298 </td>
   <td style="text-align:right;"> 3.5576422 </td>
   <td style="text-align:left;"> 0.0004 </td>
   <td style="text-align:left;"> *** </td>
  </tr>
  <tr>
   <td style="text-align:left;"> BMI </td>
   <td style="text-align:right;"> -0.0178690 </td>
   <td style="text-align:right;"> 0.0010642 </td>
   <td style="text-align:right;"> 2367.090 </td>
   <td style="text-align:right;"> -16.7903227 </td>
   <td style="text-align:left;"> &lt;0.0001 </td>
   <td style="text-align:left;"> *** </td>
  </tr>
  <tr>
   <td style="text-align:left;"> GA_samp </td>
   <td style="text-align:right;"> 0.2925421 </td>
   <td style="text-align:right;"> 0.0053394 </td>
   <td style="text-align:right;"> 2549.329 </td>
   <td style="text-align:right;"> 54.7889611 </td>
   <td style="text-align:left;"> &lt;0.0001 </td>
   <td style="text-align:left;"> *** </td>
  </tr>
</tbody>
</table></div>


### Sample descriptives
<div style="border: 1px solid #ddd; padding: 0px; overflow-y: scroll; height:600px; overflow-x: scroll; width:100%; "><table class=" lightable-classic" style='font-size: 14px; font-family: "Arial Narrow", "Source Sans Pro", sans-serif; '>
 <thead>
<tr>
<th style="empty-cells: hide;position: sticky; top:0; background-color: #FFFFFF;" colspan="1"></th>
<th style="padding-bottom:0; padding-left:3px;padding-right:3px;text-align: center; position: sticky; top:0; background-color: #FFFFFF;" colspan="3"><div style="border-bottom: 1px solid #111111; margin-bottom: -1px; ">Study</div></th>
<th style="padding-bottom:0; padding-left:3px;padding-right:3px;text-align: center; position: sticky; top:0; background-color: #FFFFFF;" colspan="3"><div style="border-bottom: 1px solid #111111; margin-bottom: -1px; ">Timepoint</div></th>
<th style="padding-bottom:0; padding-left:3px;padding-right:3px;text-align: center; position: sticky; top:0; background-color: #FFFFFF;" colspan="3"><div style="border-bottom: 1px solid #111111; margin-bottom: -1px; ">Fetal sex</div></th>
</tr>
  <tr>
   <th style="text-align:left;position: sticky; top:0; background-color: #FFFFFF;">   </th>
   <th style="text-align:left;position: sticky; top:0; background-color: #FFFFFF;"> Missing </th>
   <th style="text-align:left;position: sticky; top:0; background-color: #FFFFFF;"> SCOPE </th>
   <th style="text-align:left;position: sticky; top:0; background-color: #FFFFFF;"> STOP </th>
   <th style="text-align:left;position: sticky; top:0; background-color: #FFFFFF;"> Missing </th>
   <th style="text-align:left;position: sticky; top:0; background-color: #FFFFFF;"> 12wks </th>
   <th style="text-align:left;position: sticky; top:0; background-color: #FFFFFF;"> 15wks </th>
   <th style="text-align:left;position: sticky; top:0; background-color: #FFFFFF;"> Missing </th>
   <th style="text-align:left;position: sticky; top:0; background-color: #FFFFFF;"> Male </th>
   <th style="text-align:left;position: sticky; top:0; background-color: #FFFFFF;"> Female </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td style="text-align:left;"> Plate 1 (n=106) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 106 (100.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 106 (100.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 46 (43.4) </td>
   <td style="text-align:left;"> 60 (56.6) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate 2 (n=86) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 8 (9.3) </td>
   <td style="text-align:left;"> 78 (90.7) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 86 (100.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 63 (73.3) </td>
   <td style="text-align:left;"> 23 (26.7) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate 3 (n=48) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 5 (10.4) </td>
   <td style="text-align:left;"> 43 (89.6) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 48 (100.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 28 (58.3) </td>
   <td style="text-align:left;"> 20 (41.7) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate 4 (n=43) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 5 (11.6) </td>
   <td style="text-align:left;"> 38 (88.4) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 43 (100.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 23 (53.5) </td>
   <td style="text-align:left;"> 20 (46.5) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate 5 (n=81) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 8 (9.9) </td>
   <td style="text-align:left;"> 73 (90.1) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 81 (100.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 47 (58.0) </td>
   <td style="text-align:left;"> 34 (42.0) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate 6 (n=44) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 5 (11.4) </td>
   <td style="text-align:left;"> 39 (88.6) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 44 (100.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 15 (34.1) </td>
   <td style="text-align:left;"> 29 (65.9) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate 7 (n=47) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 6 (12.8) </td>
   <td style="text-align:left;"> 41 (87.2) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 47 (100.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 32 (68.1) </td>
   <td style="text-align:left;"> 15 (31.9) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate 8 (n=41) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 6 (14.6) </td>
   <td style="text-align:left;"> 35 (85.4) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 41 (100.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 19 (46.3) </td>
   <td style="text-align:left;"> 22 (53.7) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate 9 (n=48) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 8 (16.7) </td>
   <td style="text-align:left;"> 40 (83.3) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 48 (100.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 27 (56.2) </td>
   <td style="text-align:left;"> 21 (43.8) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate 10 (n=43) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 5 (11.6) </td>
   <td style="text-align:left;"> 38 (88.4) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 43 (100.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 20 (46.5) </td>
   <td style="text-align:left;"> 23 (53.5) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate 11 (n=44) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 4 (9.1) </td>
   <td style="text-align:left;"> 40 (90.9) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 44 (100.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 14 (31.8) </td>
   <td style="text-align:left;"> 30 (68.2) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate 12 (n=42) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 5 (11.9) </td>
   <td style="text-align:left;"> 37 (88.1) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 42 (100.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 19 (45.2) </td>
   <td style="text-align:left;"> 23 (54.8) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate 13 (n=46) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 4 (8.7) </td>
   <td style="text-align:left;"> 42 (91.3) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 46 (100.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 23 (50.0) </td>
   <td style="text-align:left;"> 23 (50.0) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate 14 (n=50) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 4 (8.0) </td>
   <td style="text-align:left;"> 46 (92.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 50 (100.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 26 (52.0) </td>
   <td style="text-align:left;"> 24 (48.0) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate 15 (n=49) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 5 (10.2) </td>
   <td style="text-align:left;"> 44 (89.8) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 49 (100.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 30 (61.2) </td>
   <td style="text-align:left;"> 19 (38.8) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate 16 (n=50) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 4 (8.0) </td>
   <td style="text-align:left;"> 46 (92.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 50 (100.0) </td>
   <td style="text-align:left;"> 1 (2.0) </td>
   <td style="text-align:left;"> 26 (52.0) </td>
   <td style="text-align:left;"> 23 (46.0) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate 17 (n=51) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 4 (7.8) </td>
   <td style="text-align:left;"> 47 (92.2) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 51 (100.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 15 (29.4) </td>
   <td style="text-align:left;"> 36 (70.6) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate 18 (n=71) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 46 (64.8) </td>
   <td style="text-align:left;"> 25 (35.2) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 14 (19.7) </td>
   <td style="text-align:left;"> 57 (80.3) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 25 (35.2) </td>
   <td style="text-align:left;"> 46 (64.8) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate 19 (n=13) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 13 (100.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 13 (100.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 4 (30.8) </td>
   <td style="text-align:left;"> 9 (69.2) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate 20 (n=72) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 50 (69.4) </td>
   <td style="text-align:left;"> 22 (30.6) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 72 (100.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 42 (58.3) </td>
   <td style="text-align:left;"> 30 (41.7) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate 21 (n=162) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 78 (48.1) </td>
   <td style="text-align:left;"> 84 (51.9) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 162 (100.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 74 (45.7) </td>
   <td style="text-align:left;"> 88 (54.3) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate 22 (n=112) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 44 (39.3) </td>
   <td style="text-align:left;"> 68 (60.7) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 112 (100.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 72 (64.3) </td>
   <td style="text-align:left;"> 40 (35.7) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate 23 (n=42) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 15 (35.7) </td>
   <td style="text-align:left;"> 27 (64.3) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 42 (100.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 21 (50.0) </td>
   <td style="text-align:left;"> 21 (50.0) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate 24 (n=40) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 15 (37.5) </td>
   <td style="text-align:left;"> 25 (62.5) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 40 (100.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 28 (70.0) </td>
   <td style="text-align:left;"> 12 (30.0) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate 25 (n=40) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 26 (65.0) </td>
   <td style="text-align:left;"> 14 (35.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 40 (100.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 21 (52.5) </td>
   <td style="text-align:left;"> 19 (47.5) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate 26 (n=40) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 23 (57.5) </td>
   <td style="text-align:left;"> 17 (42.5) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 40 (100.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 24 (60.0) </td>
   <td style="text-align:left;"> 16 (40.0) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate 27 (n=40) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 23 (57.5) </td>
   <td style="text-align:left;"> 17 (42.5) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 40 (100.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 24 (60.0) </td>
   <td style="text-align:left;"> 16 (40.0) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate 28 (n=40) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 18 (45.0) </td>
   <td style="text-align:left;"> 22 (55.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 40 (100.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 17 (42.5) </td>
   <td style="text-align:left;"> 23 (57.5) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate 29 (n=40) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 21 (52.5) </td>
   <td style="text-align:left;"> 19 (47.5) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 40 (100.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 13 (32.5) </td>
   <td style="text-align:left;"> 27 (67.5) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate 30 (n=46) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 26 (56.5) </td>
   <td style="text-align:left;"> 20 (43.5) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 46 (100.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 22 (47.8) </td>
   <td style="text-align:left;"> 24 (52.2) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate 31 (n=40) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 17 (42.5) </td>
   <td style="text-align:left;"> 23 (57.5) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 40 (100.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 25 (62.5) </td>
   <td style="text-align:left;"> 15 (37.5) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate 32 (n=40) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 30 (75.0) </td>
   <td style="text-align:left;"> 10 (25.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 40 (100.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 21 (52.5) </td>
   <td style="text-align:left;"> 19 (47.5) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate 33 (n=40) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 18 (45.0) </td>
   <td style="text-align:left;"> 22 (55.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 40 (100.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 23 (57.5) </td>
   <td style="text-align:left;"> 17 (42.5) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate 34 (n=40) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 25 (62.5) </td>
   <td style="text-align:left;"> 15 (37.5) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 40 (100.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 21 (52.5) </td>
   <td style="text-align:left;"> 19 (47.5) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate 35 (n=44) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 29 (65.9) </td>
   <td style="text-align:left;"> 15 (34.1) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 44 (100.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 24 (54.5) </td>
   <td style="text-align:left;"> 20 (45.5) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate 36 (n=40) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 23 (57.5) </td>
   <td style="text-align:left;"> 17 (42.5) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 40 (100.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 17 (42.5) </td>
   <td style="text-align:left;"> 23 (57.5) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate 37 (n=40) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 24 (60.0) </td>
   <td style="text-align:left;"> 16 (40.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 40 (100.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 21 (52.5) </td>
   <td style="text-align:left;"> 19 (47.5) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate 38 (n=40) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 22 (55.0) </td>
   <td style="text-align:left;"> 18 (45.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 40 (100.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 18 (45.0) </td>
   <td style="text-align:left;"> 22 (55.0) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate 39 (n=40) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 20 (50.0) </td>
   <td style="text-align:left;"> 20 (50.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 40 (100.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 24 (60.0) </td>
   <td style="text-align:left;"> 16 (40.0) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate 40 (n=43) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 28 (65.1) </td>
   <td style="text-align:left;"> 15 (34.9) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 43 (100.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 17 (39.5) </td>
   <td style="text-align:left;"> 26 (60.5) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate 41 (n=40) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 21 (52.5) </td>
   <td style="text-align:left;"> 19 (47.5) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 40 (100.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 12 (30.0) </td>
   <td style="text-align:left;"> 28 (70.0) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate 42 (n=43) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 23 (53.5) </td>
   <td style="text-align:left;"> 20 (46.5) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 43 (100.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 17 (39.5) </td>
   <td style="text-align:left;"> 26 (60.5) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate 43 (n=40) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 14 (35.0) </td>
   <td style="text-align:left;"> 26 (65.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 40 (100.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 24 (60.0) </td>
   <td style="text-align:left;"> 16 (40.0) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate 44 (n=40) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 24 (60.0) </td>
   <td style="text-align:left;"> 16 (40.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 40 (100.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 19 (47.5) </td>
   <td style="text-align:left;"> 21 (52.5) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate 45 (n=40) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 17 (42.5) </td>
   <td style="text-align:left;"> 23 (57.5) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 40 (100.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 18 (45.0) </td>
   <td style="text-align:left;"> 22 (55.0) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate 46 (n=40) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 21 (52.5) </td>
   <td style="text-align:left;"> 19 (47.5) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 40 (100.0) </td>
   <td style="text-align:left;"> 1 (2.5) </td>
   <td style="text-align:left;"> 23 (57.5) </td>
   <td style="text-align:left;"> 16 (40.0) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate 47 (n=40) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 18 (45.0) </td>
   <td style="text-align:left;"> 22 (55.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 40 (100.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 18 (45.0) </td>
   <td style="text-align:left;"> 22 (55.0) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate 48 (n=40) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 23 (57.5) </td>
   <td style="text-align:left;"> 17 (42.5) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 40 (100.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 24 (60.0) </td>
   <td style="text-align:left;"> 16 (40.0) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate 49 (n=46) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 28 (60.9) </td>
   <td style="text-align:left;"> 18 (39.1) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 46 (100.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 28 (60.9) </td>
   <td style="text-align:left;"> 18 (39.1) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate 50 (n=40) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 21 (52.5) </td>
   <td style="text-align:left;"> 19 (47.5) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 40 (100.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 13 (32.5) </td>
   <td style="text-align:left;"> 27 (67.5) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate 51 (n=40) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 20 (50.0) </td>
   <td style="text-align:left;"> 20 (50.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 40 (100.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 22 (55.0) </td>
   <td style="text-align:left;"> 18 (45.0) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate 52 (n=40) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 21 (52.5) </td>
   <td style="text-align:left;"> 19 (47.5) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 40 (100.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 18 (45.0) </td>
   <td style="text-align:left;"> 22 (55.0) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate 53 (n=40) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 28 (70.0) </td>
   <td style="text-align:left;"> 12 (30.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 40 (100.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 22 (55.0) </td>
   <td style="text-align:left;"> 18 (45.0) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate 54 (n=43) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 29 (67.4) </td>
   <td style="text-align:left;"> 14 (32.6) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 43 (100.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 22 (51.2) </td>
   <td style="text-align:left;"> 21 (48.8) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate 55 (n=43) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 26 (60.5) </td>
   <td style="text-align:left;"> 17 (39.5) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 43 (100.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 28 (65.1) </td>
   <td style="text-align:left;"> 15 (34.9) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate 56 (n=40) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 18 (45.0) </td>
   <td style="text-align:left;"> 22 (55.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 40 (100.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 20 (50.0) </td>
   <td style="text-align:left;"> 20 (50.0) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate 57 (n=33) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 19 (57.6) </td>
   <td style="text-align:left;"> 14 (42.4) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 33 (100.0) </td>
   <td style="text-align:left;"> 3 (9.1) </td>
   <td style="text-align:left;"> 17 (51.5) </td>
   <td style="text-align:left;"> 13 (39.4) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate Total (n=2772) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 1197 (43.2) </td>
   <td style="text-align:left;"> 1575 (56.8) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 27 (1.0) </td>
   <td style="text-align:left;"> 2745 (99.0) </td>
   <td style="text-align:left;"> 5 (0.2) </td>
   <td style="text-align:left;"> 1416 (51.1) </td>
   <td style="text-align:left;"> 1351 (48.7) </td>
  </tr>
</tbody>
</table></div>

## GH2
<img src="03_Plate_effect_files/figure-html/unnamed-chunk-2-1.png" width="1440" />
```{=html}
<svg aria-hidden="true" role="img" viewBox="0 0 512 512" style="height:1em;width:1em;vertical-align:-0.125em;margin-left:auto;margin-right:auto;font-size:inherit;fill:DarkOrange;overflow:visible;position:relative;"><path d="M256 512A256 256 0 1 0 256 0a256 256 0 1 0 0 512zm0-384c13.3 0 24 10.7 24 24V264c0 13.3-10.7 24-24 24s-24-10.7-24-24V152c0-13.3 10.7-24 24-24zM224 352a32 32 0 1 1 64 0 32 32 0 1 1 -64 0z"/></svg>
```
 <span style="color:DarkOrange;"><b>Plate 22 omitted due to invalid standard curve.</b></span><br /><br />
<b>Type III Sum of Squares</b>
<table class=" lightable-classic" style='font-size: 18px; font-family: "Arial Narrow", "Source Sans Pro", sans-serif; width: auto !important; '>
 <thead>
  <tr>
   <th style="text-align:left;">   </th>
   <th style="text-align:right;"> Chisq </th>
   <th style="text-align:right;"> Df </th>
   <th style="text-align:left;"> Pr(&gt;Chisq) </th>
   <th style="text-align:left;">  </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td style="text-align:left;"> (Intercept) </td>
   <td style="text-align:right;"> 212.579351 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:left;"> &lt;0.0001 </td>
   <td style="text-align:left;"> *** </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.GH2 </td>
   <td style="text-align:right;"> 228.193477 </td>
   <td style="text-align:right;"> 57 </td>
   <td style="text-align:left;"> &lt;0.0001 </td>
   <td style="text-align:left;"> *** </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Study </td>
   <td style="text-align:right;"> 4.354346 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:left;"> 0.04 </td>
   <td style="text-align:left;"> \* </td>
  </tr>
  <tr>
   <td style="text-align:left;"> BMI </td>
   <td style="text-align:right;"> 109.759740 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:left;"> &lt;0.0001 </td>
   <td style="text-align:left;"> *** </td>
  </tr>
  <tr>
   <td style="text-align:left;"> GA_samp </td>
   <td style="text-align:right;"> 1154.337251 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:left;"> &lt;0.0001 </td>
   <td style="text-align:left;"> *** </td>
  </tr>
</tbody>
</table>


### Model summary
<div style="border: 1px solid #ddd; padding: 0px; overflow-y: scroll; height:500px; overflow-x: scroll; width:100%; "><table class=" lightable-classic" style='font-size: 14px; font-family: "Arial Narrow", "Source Sans Pro", sans-serif; width: auto !important; '>
 <thead>
  <tr>
   <th style="text-align:left;position: sticky; top:0; background-color: #FFFFFF;">   </th>
   <th style="text-align:right;position: sticky; top:0; background-color: #FFFFFF;"> Estimate </th>
   <th style="text-align:right;position: sticky; top:0; background-color: #FFFFFF;"> Std. Error </th>
   <th style="text-align:right;position: sticky; top:0; background-color: #FFFFFF;"> df </th>
   <th style="text-align:right;position: sticky; top:0; background-color: #FFFFFF;"> t value </th>
   <th style="text-align:left;position: sticky; top:0; background-color: #FFFFFF;"> Pr(&gt;|t|) </th>
   <th style="text-align:left;position: sticky; top:0; background-color: #FFFFFF;">  </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td style="text-align:left;"> (Intercept) </td>
   <td style="text-align:right;"> -2.0852748 </td>
   <td style="text-align:right;"> 0.1430220 </td>
   <td style="text-align:right;"> 2582.496 </td>
   <td style="text-align:right;"> -14.5801012 </td>
   <td style="text-align:left;"> &lt;0.0001 </td>
   <td style="text-align:left;"> *** </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.GH21 </td>
   <td style="text-align:right;"> -0.0791846 </td>
   <td style="text-align:right;"> 0.0837897 </td>
   <td style="text-align:right;"> 2525.783 </td>
   <td style="text-align:right;"> -0.9450398 </td>
   <td style="text-align:left;"> 0.3 </td>
   <td style="text-align:left;"> ns </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.GH22 </td>
   <td style="text-align:right;"> 0.1754518 </td>
   <td style="text-align:right;"> 0.0903899 </td>
   <td style="text-align:right;"> 2634.047 </td>
   <td style="text-align:right;"> 1.9410538 </td>
   <td style="text-align:left;"> 0.05 </td>
   <td style="text-align:left;"> ns </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.GH23 </td>
   <td style="text-align:right;"> 0.2868065 </td>
   <td style="text-align:right;"> 0.0986797 </td>
   <td style="text-align:right;"> 2611.877 </td>
   <td style="text-align:right;"> 2.9064371 </td>
   <td style="text-align:left;"> 0.004 </td>
   <td style="text-align:left;"> ** </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.GH24 </td>
   <td style="text-align:right;"> -0.0048460 </td>
   <td style="text-align:right;"> 0.1050752 </td>
   <td style="text-align:right;"> 2438.502 </td>
   <td style="text-align:right;"> -0.0461189 </td>
   <td style="text-align:left;"> 1.0 </td>
   <td style="text-align:left;"> ns </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.GH25 </td>
   <td style="text-align:right;"> 0.1980649 </td>
   <td style="text-align:right;"> 0.0943090 </td>
   <td style="text-align:right;"> 2610.141 </td>
   <td style="text-align:right;"> 2.1001708 </td>
   <td style="text-align:left;"> 0.04 </td>
   <td style="text-align:left;"> \* </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.GH26 </td>
   <td style="text-align:right;"> 0.2803362 </td>
   <td style="text-align:right;"> 0.0976512 </td>
   <td style="text-align:right;"> 2634.714 </td>
   <td style="text-align:right;"> 2.8707907 </td>
   <td style="text-align:left;"> 0.004 </td>
   <td style="text-align:left;"> ** </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.GH27 </td>
   <td style="text-align:right;"> 0.0989152 </td>
   <td style="text-align:right;"> 0.0950059 </td>
   <td style="text-align:right;"> 2602.154 </td>
   <td style="text-align:right;"> 1.0411480 </td>
   <td style="text-align:left;"> 0.3 </td>
   <td style="text-align:left;"> ns </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.GH28 </td>
   <td style="text-align:right;"> -0.0810342 </td>
   <td style="text-align:right;"> 0.0973165 </td>
   <td style="text-align:right;"> 2610.799 </td>
   <td style="text-align:right;"> -0.8326878 </td>
   <td style="text-align:left;"> 0.4 </td>
   <td style="text-align:left;"> ns </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.GH29 </td>
   <td style="text-align:right;"> 0.0634070 </td>
   <td style="text-align:right;"> 0.0945526 </td>
   <td style="text-align:right;"> 2587.036 </td>
   <td style="text-align:right;"> 0.6706003 </td>
   <td style="text-align:left;"> 0.5 </td>
   <td style="text-align:left;"> ns </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.GH210 </td>
   <td style="text-align:right;"> -0.1162066 </td>
   <td style="text-align:right;"> 0.0994339 </td>
   <td style="text-align:right;"> 2636.863 </td>
   <td style="text-align:right;"> -1.1686820 </td>
   <td style="text-align:left;"> 0.2 </td>
   <td style="text-align:left;"> ns </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.GH211 </td>
   <td style="text-align:right;"> -0.1601729 </td>
   <td style="text-align:right;"> 0.0975028 </td>
   <td style="text-align:right;"> 2635.430 </td>
   <td style="text-align:right;"> -1.6427510 </td>
   <td style="text-align:left;"> 0.1 </td>
   <td style="text-align:left;"> ns </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.GH212 </td>
   <td style="text-align:right;"> -0.0603924 </td>
   <td style="text-align:right;"> 0.1011241 </td>
   <td style="text-align:right;"> 2609.689 </td>
   <td style="text-align:right;"> -0.5972102 </td>
   <td style="text-align:left;"> 0.6 </td>
   <td style="text-align:left;"> ns </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.GH213 </td>
   <td style="text-align:right;"> 0.1146427 </td>
   <td style="text-align:right;"> 0.0958679 </td>
   <td style="text-align:right;"> 2610.351 </td>
   <td style="text-align:right;"> 1.1958399 </td>
   <td style="text-align:left;"> 0.2 </td>
   <td style="text-align:left;"> ns </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.GH214 </td>
   <td style="text-align:right;"> 0.2642879 </td>
   <td style="text-align:right;"> 0.0932988 </td>
   <td style="text-align:right;"> 2565.499 </td>
   <td style="text-align:right;"> 2.8327037 </td>
   <td style="text-align:left;"> 0.005 </td>
   <td style="text-align:left;"> ** </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.GH215 </td>
   <td style="text-align:right;"> 0.1451245 </td>
   <td style="text-align:right;"> 0.0937086 </td>
   <td style="text-align:right;"> 2575.083 </td>
   <td style="text-align:right;"> 1.5486792 </td>
   <td style="text-align:left;"> 0.1 </td>
   <td style="text-align:left;"> ns </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.GH216 </td>
   <td style="text-align:right;"> 0.1255673 </td>
   <td style="text-align:right;"> 0.0931174 </td>
   <td style="text-align:right;"> 2556.264 </td>
   <td style="text-align:right;"> 1.3484842 </td>
   <td style="text-align:left;"> 0.2 </td>
   <td style="text-align:left;"> ns </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.GH217 </td>
   <td style="text-align:right;"> 0.3126568 </td>
   <td style="text-align:right;"> 0.0924637 </td>
   <td style="text-align:right;"> 2539.728 </td>
   <td style="text-align:right;"> 3.3814022 </td>
   <td style="text-align:left;"> 0.0007 </td>
   <td style="text-align:left;"> *** </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.GH218 </td>
   <td style="text-align:right;"> 0.3073315 </td>
   <td style="text-align:right;"> 0.1247045 </td>
   <td style="text-align:right;"> 2637.952 </td>
   <td style="text-align:right;"> 2.4644781 </td>
   <td style="text-align:left;"> 0.01 </td>
   <td style="text-align:left;"> \* </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.GH219 </td>
   <td style="text-align:right;"> 0.0798359 </td>
   <td style="text-align:right;"> 0.0908369 </td>
   <td style="text-align:right;"> 2308.265 </td>
   <td style="text-align:right;"> 0.8788927 </td>
   <td style="text-align:left;"> 0.4 </td>
   <td style="text-align:left;"> ns </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.GH220 </td>
   <td style="text-align:right;"> -0.0715429 </td>
   <td style="text-align:right;"> 0.0892041 </td>
   <td style="text-align:right;"> 2582.031 </td>
   <td style="text-align:right;"> -0.8020143 </td>
   <td style="text-align:left;"> 0.4 </td>
   <td style="text-align:left;"> ns </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.GH221 </td>
   <td style="text-align:right;"> 0.1159995 </td>
   <td style="text-align:right;"> 0.0818348 </td>
   <td style="text-align:right;"> 2553.780 </td>
   <td style="text-align:right;"> 1.4174827 </td>
   <td style="text-align:left;"> 0.2 </td>
   <td style="text-align:left;"> ns </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.GH223 </td>
   <td style="text-align:right;"> 0.1156668 </td>
   <td style="text-align:right;"> 0.0814530 </td>
   <td style="text-align:right;"> 2562.999 </td>
   <td style="text-align:right;"> 1.4200437 </td>
   <td style="text-align:left;"> 0.2 </td>
   <td style="text-align:left;"> ns </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.GH224 </td>
   <td style="text-align:right;"> -0.0715429 </td>
   <td style="text-align:right;"> 0.0892041 </td>
   <td style="text-align:right;"> 2582.031 </td>
   <td style="text-align:right;"> -0.8020143 </td>
   <td style="text-align:left;"> 0.4 </td>
   <td style="text-align:left;"> ns </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.GH225 </td>
   <td style="text-align:right;"> 0.3472763 </td>
   <td style="text-align:right;"> 0.0978500 </td>
   <td style="text-align:right;"> 2627.980 </td>
   <td style="text-align:right;"> 3.5490665 </td>
   <td style="text-align:left;"> 0.0004 </td>
   <td style="text-align:left;"> *** </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.GH226 </td>
   <td style="text-align:right;"> 0.0567823 </td>
   <td style="text-align:right;"> 0.0990734 </td>
   <td style="text-align:right;"> 2639.989 </td>
   <td style="text-align:right;"> 0.5731334 </td>
   <td style="text-align:left;"> 0.6 </td>
   <td style="text-align:left;"> ns </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.GH227 </td>
   <td style="text-align:right;"> 0.0386721 </td>
   <td style="text-align:right;"> 0.1019304 </td>
   <td style="text-align:right;"> 2567.883 </td>
   <td style="text-align:right;"> 0.3793975 </td>
   <td style="text-align:left;"> 0.7 </td>
   <td style="text-align:left;"> ns </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.GH228 </td>
   <td style="text-align:right;"> 0.0803651 </td>
   <td style="text-align:right;"> 0.1012572 </td>
   <td style="text-align:right;"> 2594.081 </td>
   <td style="text-align:right;"> 0.7936724 </td>
   <td style="text-align:left;"> 0.4 </td>
   <td style="text-align:left;"> ns </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.GH229 </td>
   <td style="text-align:right;"> 0.0381013 </td>
   <td style="text-align:right;"> 0.1005929 </td>
   <td style="text-align:right;"> 2630.209 </td>
   <td style="text-align:right;"> 0.3787673 </td>
   <td style="text-align:left;"> 0.7 </td>
   <td style="text-align:left;"> ns </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.GH230 </td>
   <td style="text-align:right;"> -0.1241027 </td>
   <td style="text-align:right;"> 0.1001082 </td>
   <td style="text-align:right;"> 2626.523 </td>
   <td style="text-align:right;"> -1.2396856 </td>
   <td style="text-align:left;"> 0.2 </td>
   <td style="text-align:left;"> ns </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.GH231 </td>
   <td style="text-align:right;"> -0.0019059 </td>
   <td style="text-align:right;"> 0.0999963 </td>
   <td style="text-align:right;"> 2631.126 </td>
   <td style="text-align:right;"> -0.0190602 </td>
   <td style="text-align:left;"> 1.0 </td>
   <td style="text-align:left;"> ns </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.GH232 </td>
   <td style="text-align:right;"> 0.2835346 </td>
   <td style="text-align:right;"> 0.1018710 </td>
   <td style="text-align:right;"> 2571.564 </td>
   <td style="text-align:right;"> 2.7832699 </td>
   <td style="text-align:left;"> 0.005 </td>
   <td style="text-align:left;"> ** </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.GH233 </td>
   <td style="text-align:right;"> -0.0613889 </td>
   <td style="text-align:right;"> 0.1005350 </td>
   <td style="text-align:right;"> 2618.603 </td>
   <td style="text-align:right;"> -0.6106217 </td>
   <td style="text-align:left;"> 0.5 </td>
   <td style="text-align:left;"> ns </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.GH234 </td>
   <td style="text-align:right;"> 0.0560195 </td>
   <td style="text-align:right;"> 0.1009235 </td>
   <td style="text-align:right;"> 2612.151 </td>
   <td style="text-align:right;"> 0.5550687 </td>
   <td style="text-align:left;"> 0.6 </td>
   <td style="text-align:left;"> ns </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.GH235 </td>
   <td style="text-align:right;"> -0.0076636 </td>
   <td style="text-align:right;"> 0.0989012 </td>
   <td style="text-align:right;"> 2638.810 </td>
   <td style="text-align:right;"> -0.0774879 </td>
   <td style="text-align:left;"> 0.9 </td>
   <td style="text-align:left;"> ns </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.GH236 </td>
   <td style="text-align:right;"> 0.2298988 </td>
   <td style="text-align:right;"> 0.0997097 </td>
   <td style="text-align:right;"> 2639.804 </td>
   <td style="text-align:right;"> 2.3056812 </td>
   <td style="text-align:left;"> 0.02 </td>
   <td style="text-align:left;"> \* </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.GH237 </td>
   <td style="text-align:right;"> 0.1735538 </td>
   <td style="text-align:right;"> 0.0961543 </td>
   <td style="text-align:right;"> 2619.356 </td>
   <td style="text-align:right;"> 1.8049509 </td>
   <td style="text-align:left;"> 0.07 </td>
   <td style="text-align:left;"> ns </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.GH238 </td>
   <td style="text-align:right;"> -0.0645211 </td>
   <td style="text-align:right;"> 0.1017993 </td>
   <td style="text-align:right;"> 2566.048 </td>
   <td style="text-align:right;"> -0.6338064 </td>
   <td style="text-align:left;"> 0.5 </td>
   <td style="text-align:left;"> ns </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.GH239 </td>
   <td style="text-align:right;"> -0.0706903 </td>
   <td style="text-align:right;"> 0.1007704 </td>
   <td style="text-align:right;"> 2613.399 </td>
   <td style="text-align:right;"> -0.7014987 </td>
   <td style="text-align:left;"> 0.5 </td>
   <td style="text-align:left;"> ns </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.GH240 </td>
   <td style="text-align:right;"> 0.0480588 </td>
   <td style="text-align:right;"> 0.0993875 </td>
   <td style="text-align:right;"> 2638.649 </td>
   <td style="text-align:right;"> 0.4835499 </td>
   <td style="text-align:left;"> 0.6 </td>
   <td style="text-align:left;"> ns </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.GH241 </td>
   <td style="text-align:right;"> -0.0688661 </td>
   <td style="text-align:right;"> 0.0987487 </td>
   <td style="text-align:right;"> 2639.995 </td>
   <td style="text-align:right;"> -0.6973873 </td>
   <td style="text-align:left;"> 0.5 </td>
   <td style="text-align:left;"> ns </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.GH242 </td>
   <td style="text-align:right;"> -0.0583906 </td>
   <td style="text-align:right;"> 0.0987406 </td>
   <td style="text-align:right;"> 2633.463 </td>
   <td style="text-align:right;"> -0.5913532 </td>
   <td style="text-align:left;"> 0.6 </td>
   <td style="text-align:left;"> ns </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.GH243 </td>
   <td style="text-align:right;"> -0.1163097 </td>
   <td style="text-align:right;"> 0.1017559 </td>
   <td style="text-align:right;"> 2568.225 </td>
   <td style="text-align:right;"> -1.1430258 </td>
   <td style="text-align:left;"> 0.3 </td>
   <td style="text-align:left;"> ns </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.GH244 </td>
   <td style="text-align:right;"> 0.1624526 </td>
   <td style="text-align:right;"> 0.0972865 </td>
   <td style="text-align:right;"> 2637.584 </td>
   <td style="text-align:right;"> 1.6698366 </td>
   <td style="text-align:left;"> 0.10 </td>
   <td style="text-align:left;"> ns </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.GH245 </td>
   <td style="text-align:right;"> 0.2267436 </td>
   <td style="text-align:right;"> 0.1012045 </td>
   <td style="text-align:right;"> 2596.831 </td>
   <td style="text-align:right;"> 2.2404505 </td>
   <td style="text-align:left;"> 0.03 </td>
   <td style="text-align:left;"> \* </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.GH246 </td>
   <td style="text-align:right;"> -0.0126099 </td>
   <td style="text-align:right;"> 0.0989556 </td>
   <td style="text-align:right;"> 2639.895 </td>
   <td style="text-align:right;"> -0.1274296 </td>
   <td style="text-align:left;"> 0.9 </td>
   <td style="text-align:left;"> ns </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.GH247 </td>
   <td style="text-align:right;"> -0.0684904 </td>
   <td style="text-align:right;"> 0.1001997 </td>
   <td style="text-align:right;"> 2628.590 </td>
   <td style="text-align:right;"> -0.6835389 </td>
   <td style="text-align:left;"> 0.5 </td>
   <td style="text-align:left;"> ns </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.GH248 </td>
   <td style="text-align:right;"> 0.0704647 </td>
   <td style="text-align:right;"> 0.0985888 </td>
   <td style="text-align:right;"> 2636.871 </td>
   <td style="text-align:right;"> 0.7147330 </td>
   <td style="text-align:left;"> 0.5 </td>
   <td style="text-align:left;"> ns </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.GH249 </td>
   <td style="text-align:right;"> 0.1156909 </td>
   <td style="text-align:right;"> 0.1011720 </td>
   <td style="text-align:right;"> 2614.499 </td>
   <td style="text-align:right;"> 1.1435066 </td>
   <td style="text-align:left;"> 0.3 </td>
   <td style="text-align:left;"> ns </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.GH250 </td>
   <td style="text-align:right;"> 0.0953516 </td>
   <td style="text-align:right;"> 0.1005831 </td>
   <td style="text-align:right;"> 2629.596 </td>
   <td style="text-align:right;"> 0.9479887 </td>
   <td style="text-align:left;"> 0.3 </td>
   <td style="text-align:left;"> ns </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.GH251 </td>
   <td style="text-align:right;"> 0.1946719 </td>
   <td style="text-align:right;"> 0.1015888 </td>
   <td style="text-align:right;"> 2587.762 </td>
   <td style="text-align:right;"> 1.9162727 </td>
   <td style="text-align:left;"> 0.06 </td>
   <td style="text-align:left;"> ns </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.GH252 </td>
   <td style="text-align:right;"> -0.0969296 </td>
   <td style="text-align:right;"> 0.0997871 </td>
   <td style="text-align:right;"> 2634.971 </td>
   <td style="text-align:right;"> -0.9713637 </td>
   <td style="text-align:left;"> 0.3 </td>
   <td style="text-align:left;"> ns </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.GH254 </td>
   <td style="text-align:right;"> -0.0028326 </td>
   <td style="text-align:right;"> 0.0997500 </td>
   <td style="text-align:right;"> 2635.834 </td>
   <td style="text-align:right;"> -0.0283965 </td>
   <td style="text-align:left;"> 1.0 </td>
   <td style="text-align:left;"> ns </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.GH255 </td>
   <td style="text-align:right;"> -0.0164475 </td>
   <td style="text-align:right;"> 0.0987908 </td>
   <td style="text-align:right;"> 2638.169 </td>
   <td style="text-align:right;"> -0.1664878 </td>
   <td style="text-align:left;"> 0.9 </td>
   <td style="text-align:left;"> ns </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.GH256 </td>
   <td style="text-align:right;"> 0.0426585 </td>
   <td style="text-align:right;"> 0.0980730 </td>
   <td style="text-align:right;"> 2639.719 </td>
   <td style="text-align:right;"> 0.4349666 </td>
   <td style="text-align:left;"> 0.7 </td>
   <td style="text-align:left;"> ns </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.GH257 </td>
   <td style="text-align:right;"> 0.2281709 </td>
   <td style="text-align:right;"> 0.0978808 </td>
   <td style="text-align:right;"> 2639.943 </td>
   <td style="text-align:right;"> 2.3311089 </td>
   <td style="text-align:left;"> 0.02 </td>
   <td style="text-align:left;"> \* </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.GH258 </td>
   <td style="text-align:right;"> 0.0975326 </td>
   <td style="text-align:right;"> 0.1022645 </td>
   <td style="text-align:right;"> 2535.274 </td>
   <td style="text-align:right;"> 0.9537292 </td>
   <td style="text-align:left;"> 0.3 </td>
   <td style="text-align:left;"> ns </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay.GH259 </td>
   <td style="text-align:right;"> 0.1453408 </td>
   <td style="text-align:right;"> 0.1081603 </td>
   <td style="text-align:right;"> 2495.146 </td>
   <td style="text-align:right;"> 1.3437527 </td>
   <td style="text-align:left;"> 0.2 </td>
   <td style="text-align:left;"> ns </td>
  </tr>
  <tr>
   <td style="text-align:left;"> StudySTOP </td>
   <td style="text-align:right;"> -0.0754529 </td>
   <td style="text-align:right;"> 0.0361588 </td>
   <td style="text-align:right;"> 2632.840 </td>
   <td style="text-align:right;"> -2.0867070 </td>
   <td style="text-align:left;"> 0.04 </td>
   <td style="text-align:left;"> \* </td>
  </tr>
  <tr>
   <td style="text-align:left;"> BMI </td>
   <td style="text-align:right;"> -0.0155536 </td>
   <td style="text-align:right;"> 0.0014846 </td>
   <td style="text-align:right;"> 2542.218 </td>
   <td style="text-align:right;"> -10.4766283 </td>
   <td style="text-align:left;"> &lt;0.0001 </td>
   <td style="text-align:left;"> *** </td>
  </tr>
  <tr>
   <td style="text-align:left;"> GA_samp </td>
   <td style="text-align:right;"> 0.2526113 </td>
   <td style="text-align:right;"> 0.0074351 </td>
   <td style="text-align:right;"> 2610.748 </td>
   <td style="text-align:right;"> 33.9755390 </td>
   <td style="text-align:left;"> &lt;0.0001 </td>
   <td style="text-align:left;"> *** </td>
  </tr>
</tbody>
</table></div>


### Sample descriptives
<div style="border: 1px solid #ddd; padding: 0px; overflow-y: scroll; height:600px; overflow-x: scroll; width:100%; "><table class=" lightable-classic" style='font-size: 14px; font-family: "Arial Narrow", "Source Sans Pro", sans-serif; '>
 <thead>
<tr>
<th style="empty-cells: hide;position: sticky; top:0; background-color: #FFFFFF;" colspan="1"></th>
<th style="padding-bottom:0; padding-left:3px;padding-right:3px;text-align: center; position: sticky; top:0; background-color: #FFFFFF;" colspan="3"><div style="border-bottom: 1px solid #111111; margin-bottom: -1px; ">Study</div></th>
<th style="padding-bottom:0; padding-left:3px;padding-right:3px;text-align: center; position: sticky; top:0; background-color: #FFFFFF;" colspan="3"><div style="border-bottom: 1px solid #111111; margin-bottom: -1px; ">Timepoint</div></th>
<th style="padding-bottom:0; padding-left:3px;padding-right:3px;text-align: center; position: sticky; top:0; background-color: #FFFFFF;" colspan="3"><div style="border-bottom: 1px solid #111111; margin-bottom: -1px; ">Fetal sex</div></th>
</tr>
  <tr>
   <th style="text-align:left;position: sticky; top:0; background-color: #FFFFFF;">   </th>
   <th style="text-align:left;position: sticky; top:0; background-color: #FFFFFF;"> Missing </th>
   <th style="text-align:left;position: sticky; top:0; background-color: #FFFFFF;"> SCOPE </th>
   <th style="text-align:left;position: sticky; top:0; background-color: #FFFFFF;"> STOP </th>
   <th style="text-align:left;position: sticky; top:0; background-color: #FFFFFF;"> Missing </th>
   <th style="text-align:left;position: sticky; top:0; background-color: #FFFFFF;"> 12wks </th>
   <th style="text-align:left;position: sticky; top:0; background-color: #FFFFFF;"> 15wks </th>
   <th style="text-align:left;position: sticky; top:0; background-color: #FFFFFF;"> Missing </th>
   <th style="text-align:left;position: sticky; top:0; background-color: #FFFFFF;"> Male </th>
   <th style="text-align:left;position: sticky; top:0; background-color: #FFFFFF;"> Female </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td style="text-align:left;"> Plate 1 (n=91) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 91 (100.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 91 (100.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 38 (41.8) </td>
   <td style="text-align:left;"> 53 (58.2) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate 2 (n=70) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 8 (11.4) </td>
   <td style="text-align:left;"> 62 (88.6) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 70 (100.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 49 (70.0) </td>
   <td style="text-align:left;"> 21 (30.0) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate 3 (n=47) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 5 (10.6) </td>
   <td style="text-align:left;"> 42 (89.4) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 47 (100.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 29 (61.7) </td>
   <td style="text-align:left;"> 18 (38.3) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate 4 (n=42) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 5 (11.9) </td>
   <td style="text-align:left;"> 37 (88.1) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 42 (100.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 23 (54.8) </td>
   <td style="text-align:left;"> 19 (45.2) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate 5 (n=79) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 8 (10.1) </td>
   <td style="text-align:left;"> 71 (89.9) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 79 (100.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 47 (59.5) </td>
   <td style="text-align:left;"> 32 (40.5) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate 6 (n=43) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 5 (11.6) </td>
   <td style="text-align:left;"> 38 (88.4) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 43 (100.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 16 (37.2) </td>
   <td style="text-align:left;"> 27 (62.8) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate 7 (n=45) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 6 (13.3) </td>
   <td style="text-align:left;"> 39 (86.7) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 45 (100.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 30 (66.7) </td>
   <td style="text-align:left;"> 15 (33.3) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate 8 (n=41) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 6 (14.6) </td>
   <td style="text-align:left;"> 35 (85.4) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 41 (100.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 19 (46.3) </td>
   <td style="text-align:left;"> 22 (53.7) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate 9 (n=46) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 8 (17.4) </td>
   <td style="text-align:left;"> 38 (82.6) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 46 (100.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 25 (54.3) </td>
   <td style="text-align:left;"> 21 (45.7) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate 10 (n=44) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 6 (13.6) </td>
   <td style="text-align:left;"> 38 (86.4) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 44 (100.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 20 (45.5) </td>
   <td style="text-align:left;"> 24 (54.5) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate 11 (n=43) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 4 (9.3) </td>
   <td style="text-align:left;"> 39 (90.7) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 43 (100.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 14 (32.6) </td>
   <td style="text-align:left;"> 29 (67.4) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate 12 (n=43) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 5 (11.6) </td>
   <td style="text-align:left;"> 38 (88.4) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 43 (100.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 19 (44.2) </td>
   <td style="text-align:left;"> 24 (55.8) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate 13 (n=45) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 4 (8.9) </td>
   <td style="text-align:left;"> 41 (91.1) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 45 (100.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 24 (53.3) </td>
   <td style="text-align:left;"> 21 (46.7) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate 14 (n=46) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 4 (8.7) </td>
   <td style="text-align:left;"> 42 (91.3) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 46 (100.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 22 (47.8) </td>
   <td style="text-align:left;"> 24 (52.2) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate 15 (n=47) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 5 (10.6) </td>
   <td style="text-align:left;"> 42 (89.4) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 47 (100.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 28 (59.6) </td>
   <td style="text-align:left;"> 19 (40.4) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate 16 (n=46) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 4 (8.7) </td>
   <td style="text-align:left;"> 42 (91.3) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 46 (100.0) </td>
   <td style="text-align:left;"> 1 (2.2) </td>
   <td style="text-align:left;"> 24 (52.2) </td>
   <td style="text-align:left;"> 21 (45.7) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate 17 (n=47) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 4 (8.5) </td>
   <td style="text-align:left;"> 43 (91.5) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 47 (100.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 15 (31.9) </td>
   <td style="text-align:left;"> 32 (68.1) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate 18 (n=20) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 20 (100.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 20 (100.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 11 (55.0) </td>
   <td style="text-align:left;"> 9 (45.0) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate 19 (n=48) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 43 (89.6) </td>
   <td style="text-align:left;"> 5 (10.4) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 35 (72.9) </td>
   <td style="text-align:left;"> 13 (27.1) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 21 (43.8) </td>
   <td style="text-align:left;"> 27 (56.2) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate 20 (n=64) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 22 (34.4) </td>
   <td style="text-align:left;"> 42 (65.6) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 64 (100.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 43 (67.2) </td>
   <td style="text-align:left;"> 21 (32.8) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate 21 (n=109) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 55 (50.5) </td>
   <td style="text-align:left;"> 54 (49.5) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 109 (100.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 44 (40.4) </td>
   <td style="text-align:left;"> 65 (59.6) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate 22 (n=72) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 50 (69.4) </td>
   <td style="text-align:left;"> 22 (30.6) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 72 (100.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 39 (54.2) </td>
   <td style="text-align:left;"> 33 (45.8) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate 23 (n=115) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 61 (53.0) </td>
   <td style="text-align:left;"> 54 (47.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 115 (100.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 50 (43.5) </td>
   <td style="text-align:left;"> 65 (56.5) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate 24 (n=64) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 22 (34.4) </td>
   <td style="text-align:left;"> 42 (65.6) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 64 (100.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 43 (67.2) </td>
   <td style="text-align:left;"> 21 (32.8) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate 25 (n=42) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 15 (35.7) </td>
   <td style="text-align:left;"> 27 (64.3) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 42 (100.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 21 (50.0) </td>
   <td style="text-align:left;"> 21 (50.0) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate 26 (n=40) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 15 (37.5) </td>
   <td style="text-align:left;"> 25 (62.5) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 40 (100.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 28 (70.0) </td>
   <td style="text-align:left;"> 12 (30.0) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate 27 (n=40) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 26 (65.0) </td>
   <td style="text-align:left;"> 14 (35.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 40 (100.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 21 (52.5) </td>
   <td style="text-align:left;"> 19 (47.5) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate 28 (n=40) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 23 (57.5) </td>
   <td style="text-align:left;"> 17 (42.5) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 40 (100.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 24 (60.0) </td>
   <td style="text-align:left;"> 16 (40.0) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate 29 (n=40) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 23 (57.5) </td>
   <td style="text-align:left;"> 17 (42.5) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 40 (100.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 24 (60.0) </td>
   <td style="text-align:left;"> 16 (40.0) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate 30 (n=40) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 18 (45.0) </td>
   <td style="text-align:left;"> 22 (55.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 40 (100.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 17 (42.5) </td>
   <td style="text-align:left;"> 23 (57.5) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate 31 (n=40) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 21 (52.5) </td>
   <td style="text-align:left;"> 19 (47.5) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 40 (100.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 13 (32.5) </td>
   <td style="text-align:left;"> 27 (67.5) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate 32 (n=46) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 26 (56.5) </td>
   <td style="text-align:left;"> 20 (43.5) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 46 (100.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 22 (47.8) </td>
   <td style="text-align:left;"> 24 (52.2) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate 33 (n=40) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 17 (42.5) </td>
   <td style="text-align:left;"> 23 (57.5) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 40 (100.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 25 (62.5) </td>
   <td style="text-align:left;"> 15 (37.5) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate 34 (n=40) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 30 (75.0) </td>
   <td style="text-align:left;"> 10 (25.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 40 (100.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 21 (52.5) </td>
   <td style="text-align:left;"> 19 (47.5) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate 35 (n=40) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 18 (45.0) </td>
   <td style="text-align:left;"> 22 (55.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 40 (100.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 23 (57.5) </td>
   <td style="text-align:left;"> 17 (42.5) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate 36 (n=40) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 25 (62.5) </td>
   <td style="text-align:left;"> 15 (37.5) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 40 (100.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 21 (52.5) </td>
   <td style="text-align:left;"> 19 (47.5) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate 37 (n=44) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 29 (65.9) </td>
   <td style="text-align:left;"> 15 (34.1) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 44 (100.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 24 (54.5) </td>
   <td style="text-align:left;"> 20 (45.5) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate 38 (n=40) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 23 (57.5) </td>
   <td style="text-align:left;"> 17 (42.5) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 40 (100.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 17 (42.5) </td>
   <td style="text-align:left;"> 23 (57.5) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate 39 (n=40) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 24 (60.0) </td>
   <td style="text-align:left;"> 16 (40.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 40 (100.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 21 (52.5) </td>
   <td style="text-align:left;"> 19 (47.5) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate 40 (n=40) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 22 (55.0) </td>
   <td style="text-align:left;"> 18 (45.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 40 (100.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 18 (45.0) </td>
   <td style="text-align:left;"> 22 (55.0) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate 41 (n=40) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 20 (50.0) </td>
   <td style="text-align:left;"> 20 (50.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 40 (100.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 24 (60.0) </td>
   <td style="text-align:left;"> 16 (40.0) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate 42 (n=43) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 28 (65.1) </td>
   <td style="text-align:left;"> 15 (34.9) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 43 (100.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 17 (39.5) </td>
   <td style="text-align:left;"> 26 (60.5) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate 43 (n=40) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 21 (52.5) </td>
   <td style="text-align:left;"> 19 (47.5) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 40 (100.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 12 (30.0) </td>
   <td style="text-align:left;"> 28 (70.0) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate 44 (n=43) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 23 (53.5) </td>
   <td style="text-align:left;"> 20 (46.5) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 43 (100.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 17 (39.5) </td>
   <td style="text-align:left;"> 26 (60.5) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate 45 (n=40) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 14 (35.0) </td>
   <td style="text-align:left;"> 26 (65.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 40 (100.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 24 (60.0) </td>
   <td style="text-align:left;"> 16 (40.0) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate 46 (n=40) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 24 (60.0) </td>
   <td style="text-align:left;"> 16 (40.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 40 (100.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 19 (47.5) </td>
   <td style="text-align:left;"> 21 (52.5) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate 47 (n=40) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 17 (42.5) </td>
   <td style="text-align:left;"> 23 (57.5) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 40 (100.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 18 (45.0) </td>
   <td style="text-align:left;"> 22 (55.0) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate 48 (n=40) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 21 (52.5) </td>
   <td style="text-align:left;"> 19 (47.5) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 40 (100.0) </td>
   <td style="text-align:left;"> 1 (2.5) </td>
   <td style="text-align:left;"> 23 (57.5) </td>
   <td style="text-align:left;"> 16 (40.0) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate 49 (n=40) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 18 (45.0) </td>
   <td style="text-align:left;"> 22 (55.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 40 (100.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 18 (45.0) </td>
   <td style="text-align:left;"> 22 (55.0) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate 50 (n=40) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 23 (57.5) </td>
   <td style="text-align:left;"> 17 (42.5) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 40 (100.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 24 (60.0) </td>
   <td style="text-align:left;"> 16 (40.0) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate 51 (n=46) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 28 (60.9) </td>
   <td style="text-align:left;"> 18 (39.1) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 46 (100.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 28 (60.9) </td>
   <td style="text-align:left;"> 18 (39.1) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate 52 (n=40) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 21 (52.5) </td>
   <td style="text-align:left;"> 19 (47.5) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 40 (100.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 13 (32.5) </td>
   <td style="text-align:left;"> 27 (67.5) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate 53 (n=40) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 20 (50.0) </td>
   <td style="text-align:left;"> 20 (50.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 40 (100.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 22 (55.0) </td>
   <td style="text-align:left;"> 18 (45.0) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate 54 (n=40) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 21 (52.5) </td>
   <td style="text-align:left;"> 19 (47.5) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 40 (100.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 18 (45.0) </td>
   <td style="text-align:left;"> 22 (55.0) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate 55 (n=40) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 28 (70.0) </td>
   <td style="text-align:left;"> 12 (30.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 40 (100.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 22 (55.0) </td>
   <td style="text-align:left;"> 18 (45.0) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate 56 (n=43) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 29 (67.4) </td>
   <td style="text-align:left;"> 14 (32.6) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 43 (100.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 22 (51.2) </td>
   <td style="text-align:left;"> 21 (48.8) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate 57 (n=43) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 26 (60.5) </td>
   <td style="text-align:left;"> 17 (39.5) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 43 (100.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 28 (65.1) </td>
   <td style="text-align:left;"> 15 (34.9) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate 58 (n=40) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 18 (45.0) </td>
   <td style="text-align:left;"> 22 (55.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 40 (100.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 20 (50.0) </td>
   <td style="text-align:left;"> 20 (50.0) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate 59 (n=33) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 19 (57.6) </td>
   <td style="text-align:left;"> 14 (42.4) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 33 (100.0) </td>
   <td style="text-align:left;"> 3 (9.1) </td>
   <td style="text-align:left;"> 17 (51.5) </td>
   <td style="text-align:left;"> 13 (39.4) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Plate Total (n=2780) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 1205 (43.3) </td>
   <td style="text-align:left;"> 1575 (56.7) </td>
   <td style="text-align:left;"> 0 (0.0) </td>
   <td style="text-align:left;"> 35 (1.3) </td>
   <td style="text-align:left;"> 2745 (98.7) </td>
   <td style="text-align:left;"> 5 (0.2) </td>
   <td style="text-align:left;"> 1419 (51.0) </td>
   <td style="text-align:left;"> 1356 (48.8) </td>
  </tr>
</tbody>
</table></div>

## Session info
**Results generated on: 2023-08-27 22:54:54.694134**
<details><summary>Click for more details</summary>

```r
sessionInfo()
```

```
## R version 4.3.1 (2023-06-16)
## Platform: x86_64-pc-linux-gnu (64-bit)
## Running under: Ubuntu 22.04.3 LTS
## 
## Matrix products: default
## BLAS:   /usr/lib/x86_64-linux-gnu/blas/libblas.so.3.10.0 
## LAPACK: /usr/lib/x86_64-linux-gnu/lapack/liblapack.so.3.10.0
## 
## locale:
##  [1] LC_CTYPE=en_AU.UTF-8          LC_NUMERIC=C                 
##  [3] LC_TIME=en_AU.UTF-8           LC_COLLATE=en_AU.UTF-8       
##  [5] LC_MONETARY=en_AU.UTF-8       LC_MESSAGES=en_AU.UTF-8      
##  [7] LC_PAPER=en_AU.UTF-8          LC_NAME=en_AU.UTF-8          
##  [9] LC_ADDRESS=en_AU.UTF-8        LC_TELEPHONE=en_AU.UTF-8     
## [11] LC_MEASUREMENT=en_AU.UTF-8    LC_IDENTIFICATION=en_AU.UTF-8
## 
## time zone: Australia/Adelaide
## tzcode source: system (glibc)
## 
## attached base packages:
## [1] grid      stats     graphics  grDevices utils     datasets  methods  
## [8] base     
## 
## other attached packages:
##  [1] xlsx_0.6.5        plotly_4.10.2     geepack_1.3.9     lmerTest_3.1-3   
##  [5] lme4_1.1-33       Matrix_1.6-0      ggpubr_0.6.0      emmeans_1.8.5    
##  [9] car_3.1-2         carData_3.0-5     readxl_1.4.2      Hmisc_5.1-0      
## [13] fontawesome_0.5.1 htmlwidgets_1.6.2 kableExtra_1.3.4  knitr_1.42       
## [17] rmarkdown_2.21    ggplot2_3.4.2     devtools_2.4.3    usethis_2.1.5    
## [21] pander_0.6.5      magrittr_2.0.3    gridExtra_2.3    
## 
## loaded via a namespace (and not attached):
##  [1] remotes_2.4.2       sandwich_3.0-1      rlang_1.1.1        
##  [4] multcomp_1.4-18     compiler_4.3.1      systemfonts_1.0.4  
##  [7] callr_3.7.3         vctrs_0.6.3         rvest_1.0.3        
## [10] stringr_1.5.0       pkgconfig_2.0.3     crayon_1.5.2       
## [13] fastmap_1.1.1       backports_1.4.1     ellipsis_0.3.2     
## [16] labeling_0.4.2      utf8_1.2.3          sessioninfo_1.2.2  
## [19] nloptr_2.0.0        ps_1.7.5            purrr_1.0.1        
## [22] xfun_0.39           cachem_1.0.8        jsonlite_1.8.4     
## [25] highr_0.10          xlsxjars_0.6.1      broom_1.0.4        
## [28] prettyunits_1.1.1   cluster_2.1.4       R6_2.5.1           
## [31] bslib_0.4.2         stringi_1.7.12      boot_1.3-28        
## [34] pkgload_1.3.2       rpart_4.1.19        numDeriv_2016.8-1.1
## [37] jquerylib_0.1.4     cellranger_1.1.0    estimability_1.4.1 
## [40] Rcpp_1.0.11         bookdown_0.34       zoo_1.8-9          
## [43] base64enc_0.1-3     splines_4.3.1       nnet_7.3-19        
## [46] tidyselect_1.2.0    rstudioapi_0.14     abind_1.4-5        
## [49] yaml_2.3.7          codetools_0.2-19    processx_3.8.1     
## [52] pkgbuild_1.4.0      lattice_0.21-8      tibble_3.2.1       
## [55] withr_2.5.0         coda_0.19-4         evaluate_0.21      
## [58] foreign_0.8-82      survival_3.5-5      rJava_1.0-6        
## [61] xml2_1.3.3          pillar_1.9.0        checkmate_2.0.0    
## [64] generics_0.1.3      munsell_0.5.0       scales_1.2.1       
## [67] minqa_1.2.4         xtable_1.8-4        glue_1.6.2         
## [70] lazyeval_0.2.2      tools_4.3.1         data.table_1.14.8  
## [73] webshot_0.5.4       ggsignif_0.6.4      fs_1.6.2           
## [76] mvtnorm_1.1-3       tidyr_1.3.0         colorspace_2.1-0   
## [79] nlme_3.1-162        htmlTable_2.4.0     Formula_1.2-4      
## [82] cli_3.6.1           fansi_1.0.4         viridisLite_0.4.2  
## [85] svglite_2.1.0       dplyr_1.1.2         gtable_0.3.3       
## [88] rstatix_0.7.2       sass_0.4.6          digest_0.6.33      
## [91] TH.data_1.1-0       farver_2.1.1        memoise_2.0.1      
## [94] htmltools_0.5.5     lifecycle_1.0.3     httr_1.4.2         
## [97] MASS_7.3-60
```
</details>

