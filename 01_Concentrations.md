# (PART\*) Raw Data {-}




# Standard Curves
This section contains standard curves fitted for Prolactin, HPL, and GH2.

`<svg aria-hidden="true" role="img" viewBox="0 0 512 512" style="height:1em;width:1em;vertical-align:-0.125em;margin-left:auto;margin-right:auto;font-size:inherit;fill:red;overflow:visible;position:relative;"><path d="M256 512A256 256 0 1 0 256 0a256 256 0 1 0 0 512zM216 336h24V272H216c-13.3 0-24-10.7-24-24s10.7-24 24-24h48c13.3 0 24 10.7 24 24v88h8c13.3 0 24 10.7 24 24s-10.7 24-24 24H216c-13.3 0-24-10.7-24-24s10.7-24 24-24zm40-208a32 32 0 1 1 0 64 32 32 0 1 1 0-64z"/></svg>`{=html} <span style="color:red;"><b>GH2 Plate 22 (28-2-22) omitted due to invalid standard curve.</b></span><br />
`<svg aria-hidden="true" role="img" viewBox="0 0 512 512" style="height:1em;width:1em;vertical-align:-0.125em;margin-left:auto;margin-right:auto;font-size:inherit;fill:DarkOrange;overflow:visible;position:relative;"><path d="M256 512A256 256 0 1 0 256 0a256 256 0 1 0 0 512zM216 336h24V272H216c-13.3 0-24-10.7-24-24s10.7-24 24-24h48c13.3 0 24 10.7 24 24v88h8c13.3 0 24 10.7 24 24s-10.7 24-24 24H216c-13.3 0-24-10.7-24-24s10.7-24 24-24zm40-208a32 32 0 1 1 0 64 32 32 0 1 1 0-64z"/></svg>`{=html} <span style="color:DarkOrange;"><b>Inter-assay CV for Prolactin and HPL higher than recommended 15%.</b></span><br />

According to the protocols, the following methods were used for curve fitting:<br />
- <strong>Prolactin:</strong> Quadratic<br />
- <strong>HPL:</strong> 4-parameter Logistic<br />
- <strong>GH2:</strong> non-linear splines<br />


## Prolactin





### Data {.tabset}

```r
# standards
std_raw <- read_excel(file.path("..","data","hormones","Prolactin_absorbance_combined_20220728.xlsx"),sheet="SL Combined Abs standards only")
std_raw$Abs.ave <- apply(std_raw[,c("Abs 1","Abs 2")],1,mean,na.rm=T) #average replicates

# samples
samp_raw <- read_excel(file.path("..","data","hormones","Prolactin_absorbance_combined_20220728.xlsx"),sheet="SL SCOPE and STOP combined Abs ")
samp_raw$Abs.ave <- apply(samp_raw[,c("Abs 1","Abs 2")],1,mean,na.rm=T) #average replicates
```

#### **Standard concentration by plate**
<details><summary>Click for more details</summary>
<table class=" lightable-classic" style='font-size: 18px; font-family: "Arial Narrow", "Source Sans Pro", sans-serif; width: auto !important; '>
 <thead>
<tr>
<th style="empty-cells: hide;" colspan="1"></th>
<th style="padding-bottom:0; padding-left:3px;padding-right:3px;text-align: center; " colspan="6"><div style="border-bottom: 1px solid #111111; margin-bottom: -1px; ">Concentration</div></th>
</tr>
  <tr>
   <th style="text-align:left;">   </th>
   <th style="text-align:right;"> 0 </th>
   <th style="text-align:right;"> 5 </th>
   <th style="text-align:right;"> 15 </th>
   <th style="text-align:right;"> 50 </th>
   <th style="text-align:right;"> 100 </th>
   <th style="text-align:right;"> 200 </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td style="text-align:left;"> Assay 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 2 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 3 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 4 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 5 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 6 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 7 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 8 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 9 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 10 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 11 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 12 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 13 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 14 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 15 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 16 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 17 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 18 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 19 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 20 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 21 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 22 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 23 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 24 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 25 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 26 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 27 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 28 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 29 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 30 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 31 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 32 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 33 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 34 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 35 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 36 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 37 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 38 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 39 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 40 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 41 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 42 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 43 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 44 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 45 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 46 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 47 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 48 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 49 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 50 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 51 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 52 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 53 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 54 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 55 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 56 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 57 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
</tbody>
</table>

</details>

#### **Samples by plate**
<details><summary>Click for more details</summary>
<table class=" lightable-classic" style='font-size: 18px; font-family: "Arial Narrow", "Source Sans Pro", sans-serif; width: auto !important; '>
 <thead>
<tr>
<th style="empty-cells: hide;" colspan="1"></th>
<th style="padding-bottom:0; padding-left:3px;padding-right:3px;text-align: center; " colspan="3"><div style="border-bottom: 1px solid #111111; margin-bottom: -1px; ">Study</div></th>
</tr>
  <tr>
   <th style="text-align:left;">   </th>
   <th style="text-align:right;"> SCOPE </th>
   <th style="text-align:right;"> STOP </th>
   <th style="text-align:right;"> Total </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td style="text-align:left;"> Assay 1 </td>
   <td style="text-align:right;"> 39 </td>
   <td style="text-align:right;"> 0 </td>
   <td style="text-align:right;"> 39 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 2 </td>
   <td style="text-align:right;"> 5 </td>
   <td style="text-align:right;"> 35 </td>
   <td style="text-align:right;"> 40 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 3 </td>
   <td style="text-align:right;"> 5 </td>
   <td style="text-align:right;"> 35 </td>
   <td style="text-align:right;"> 40 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 4 </td>
   <td style="text-align:right;"> 5 </td>
   <td style="text-align:right;"> 34 </td>
   <td style="text-align:right;"> 39 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 5 </td>
   <td style="text-align:right;"> 5 </td>
   <td style="text-align:right;"> 35 </td>
   <td style="text-align:right;"> 40 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 6 </td>
   <td style="text-align:right;"> 5 </td>
   <td style="text-align:right;"> 34 </td>
   <td style="text-align:right;"> 39 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 7 </td>
   <td style="text-align:right;"> 5 </td>
   <td style="text-align:right;"> 35 </td>
   <td style="text-align:right;"> 40 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 8 </td>
   <td style="text-align:right;"> 5 </td>
   <td style="text-align:right;"> 35 </td>
   <td style="text-align:right;"> 40 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 9 </td>
   <td style="text-align:right;"> 5 </td>
   <td style="text-align:right;"> 35 </td>
   <td style="text-align:right;"> 40 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 10 </td>
   <td style="text-align:right;"> 5 </td>
   <td style="text-align:right;"> 35 </td>
   <td style="text-align:right;"> 40 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 11 </td>
   <td style="text-align:right;"> 4 </td>
   <td style="text-align:right;"> 36 </td>
   <td style="text-align:right;"> 40 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 12 </td>
   <td style="text-align:right;"> 4 </td>
   <td style="text-align:right;"> 36 </td>
   <td style="text-align:right;"> 40 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 13 </td>
   <td style="text-align:right;"> 4 </td>
   <td style="text-align:right;"> 36 </td>
   <td style="text-align:right;"> 40 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 14 </td>
   <td style="text-align:right;"> 4 </td>
   <td style="text-align:right;"> 36 </td>
   <td style="text-align:right;"> 40 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 15 </td>
   <td style="text-align:right;"> 4 </td>
   <td style="text-align:right;"> 36 </td>
   <td style="text-align:right;"> 40 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 16 </td>
   <td style="text-align:right;"> 4 </td>
   <td style="text-align:right;"> 36 </td>
   <td style="text-align:right;"> 40 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 17 </td>
   <td style="text-align:right;"> 4 </td>
   <td style="text-align:right;"> 36 </td>
   <td style="text-align:right;"> 40 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 18 </td>
   <td style="text-align:right;"> 22 </td>
   <td style="text-align:right;"> 18 </td>
   <td style="text-align:right;"> 40 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 19 </td>
   <td style="text-align:right;"> 15 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 16 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 20 </td>
   <td style="text-align:right;"> 12 </td>
   <td style="text-align:right;"> 29 </td>
   <td style="text-align:right;"> 41 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 21 </td>
   <td style="text-align:right;"> 5 </td>
   <td style="text-align:right;"> 35 </td>
   <td style="text-align:right;"> 40 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 22 </td>
   <td style="text-align:right;"> 22 </td>
   <td style="text-align:right;"> 18 </td>
   <td style="text-align:right;"> 40 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 23 </td>
   <td style="text-align:right;"> 15 </td>
   <td style="text-align:right;"> 25 </td>
   <td style="text-align:right;"> 40 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 24 </td>
   <td style="text-align:right;"> 15 </td>
   <td style="text-align:right;"> 25 </td>
   <td style="text-align:right;"> 40 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 25 </td>
   <td style="text-align:right;"> 26 </td>
   <td style="text-align:right;"> 14 </td>
   <td style="text-align:right;"> 40 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 26 </td>
   <td style="text-align:right;"> 23 </td>
   <td style="text-align:right;"> 17 </td>
   <td style="text-align:right;"> 40 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 27 </td>
   <td style="text-align:right;"> 23 </td>
   <td style="text-align:right;"> 17 </td>
   <td style="text-align:right;"> 40 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 28 </td>
   <td style="text-align:right;"> 18 </td>
   <td style="text-align:right;"> 22 </td>
   <td style="text-align:right;"> 40 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 29 </td>
   <td style="text-align:right;"> 21 </td>
   <td style="text-align:right;"> 19 </td>
   <td style="text-align:right;"> 40 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 30 </td>
   <td style="text-align:right;"> 20 </td>
   <td style="text-align:right;"> 20 </td>
   <td style="text-align:right;"> 40 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 31 </td>
   <td style="text-align:right;"> 17 </td>
   <td style="text-align:right;"> 23 </td>
   <td style="text-align:right;"> 40 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 32 </td>
   <td style="text-align:right;"> 30 </td>
   <td style="text-align:right;"> 10 </td>
   <td style="text-align:right;"> 40 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 33 </td>
   <td style="text-align:right;"> 18 </td>
   <td style="text-align:right;"> 22 </td>
   <td style="text-align:right;"> 40 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 34 </td>
   <td style="text-align:right;"> 25 </td>
   <td style="text-align:right;"> 15 </td>
   <td style="text-align:right;"> 40 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 35 </td>
   <td style="text-align:right;"> 25 </td>
   <td style="text-align:right;"> 15 </td>
   <td style="text-align:right;"> 40 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 36 </td>
   <td style="text-align:right;"> 23 </td>
   <td style="text-align:right;"> 17 </td>
   <td style="text-align:right;"> 40 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 37 </td>
   <td style="text-align:right;"> 24 </td>
   <td style="text-align:right;"> 16 </td>
   <td style="text-align:right;"> 40 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 38 </td>
   <td style="text-align:right;"> 22 </td>
   <td style="text-align:right;"> 18 </td>
   <td style="text-align:right;"> 40 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 39 </td>
   <td style="text-align:right;"> 20 </td>
   <td style="text-align:right;"> 20 </td>
   <td style="text-align:right;"> 40 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 40 </td>
   <td style="text-align:right;"> 25 </td>
   <td style="text-align:right;"> 15 </td>
   <td style="text-align:right;"> 40 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 41 </td>
   <td style="text-align:right;"> 21 </td>
   <td style="text-align:right;"> 19 </td>
   <td style="text-align:right;"> 40 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 42 </td>
   <td style="text-align:right;"> 20 </td>
   <td style="text-align:right;"> 20 </td>
   <td style="text-align:right;"> 40 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 43 </td>
   <td style="text-align:right;"> 14 </td>
   <td style="text-align:right;"> 26 </td>
   <td style="text-align:right;"> 40 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 44 </td>
   <td style="text-align:right;"> 24 </td>
   <td style="text-align:right;"> 16 </td>
   <td style="text-align:right;"> 40 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 45 </td>
   <td style="text-align:right;"> 17 </td>
   <td style="text-align:right;"> 23 </td>
   <td style="text-align:right;"> 40 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 46 </td>
   <td style="text-align:right;"> 21 </td>
   <td style="text-align:right;"> 19 </td>
   <td style="text-align:right;"> 40 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 47 </td>
   <td style="text-align:right;"> 18 </td>
   <td style="text-align:right;"> 22 </td>
   <td style="text-align:right;"> 40 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 48 </td>
   <td style="text-align:right;"> 23 </td>
   <td style="text-align:right;"> 17 </td>
   <td style="text-align:right;"> 40 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 49 </td>
   <td style="text-align:right;"> 22 </td>
   <td style="text-align:right;"> 18 </td>
   <td style="text-align:right;"> 40 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 50 </td>
   <td style="text-align:right;"> 21 </td>
   <td style="text-align:right;"> 19 </td>
   <td style="text-align:right;"> 40 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 51 </td>
   <td style="text-align:right;"> 20 </td>
   <td style="text-align:right;"> 20 </td>
   <td style="text-align:right;"> 40 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 52 </td>
   <td style="text-align:right;"> 21 </td>
   <td style="text-align:right;"> 19 </td>
   <td style="text-align:right;"> 40 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 53 </td>
   <td style="text-align:right;"> 28 </td>
   <td style="text-align:right;"> 12 </td>
   <td style="text-align:right;"> 40 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 54 </td>
   <td style="text-align:right;"> 26 </td>
   <td style="text-align:right;"> 14 </td>
   <td style="text-align:right;"> 40 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 55 </td>
   <td style="text-align:right;"> 23 </td>
   <td style="text-align:right;"> 17 </td>
   <td style="text-align:right;"> 40 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 56 </td>
   <td style="text-align:right;"> 18 </td>
   <td style="text-align:right;"> 22 </td>
   <td style="text-align:right;"> 40 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 57 </td>
   <td style="text-align:right;"> 19 </td>
   <td style="text-align:right;"> 14 </td>
   <td style="text-align:right;"> 33 </td>
  </tr>
</tbody>
</table>

</details>

### CV

```r
## Inter-assay CV
cv_dat <- std_raw
#cv_dat <- std_raw[with(std_raw,get(conc_name)<=50),]
#cv_dat <- std_raw[!std_raw$Assay%in%c(2,6,7,11,18,19),]
cv_dat$Group <- as.factor(with(cv_dat,get(conc_name)))
assay_ls <- split(cv_dat,cv_dat$Assay)
cv_mean_dat <- Reduce(rbind,lapply(assay_ls,function(x) tapply(x$"Abs Ave",x$Group,mean,na.tm=T)))
cv_mean_dat[cv_mean_dat<0.0000001] <- 0
cv_mean <- apply(cv_mean_dat,2,mean,na.rm=T)
cv_sd <- apply(cv_mean_dat,2,sd,na.rm=T)
cv_gps <- (cv_sd/cv_mean)*100
cv_gps[is.nan(cv_gps)] <- 0
cv_inter <- mean(cv_gps,na.rm=T)

## Intra-assay CV
samp_cv <- unlist(lapply(1:nrow(samp_raw),function(x){
				tmp_dat <- data.frame(samp_raw[x,])
			    tmp_mean <- mean(as.numeric(tmp_dat[5:6]))
			    tmp_sd <- sd(as.numeric(tmp_dat[5:6]))
			    return((tmp_sd/tmp_mean)*100)}))
cv_intra <- mean(samp_cv)
```
Inter-assay CV = 25.25% from 57 assays.<br />
Intra-assay CV = 3.85% from 2247 sample measurements.<br />

<img src="01_Concentrations_files/figure-html/cv_plot-1.png" width="1056" />

### Standard curves

```r
std_ls <- split(std_raw,std_raw$Assay) #split data by plate
std_fit <- lapply(1:length(std_ls),function(k){lm(Abs.ave ~ poly(Conc,2,raw=T),data=std_ls[[k]])}) #fit quadratic
#std_fit <- lapply(1:length(std_ls),function(k){lm(Abs.ave ~ Conc + I(Conc^2),data=std_ls[[k]])}) #fit model
std_fit2 <- lapply(1:length(std_ls),function(k){lm(Abs.ave ~ ns(Conc,df=3),data=std_ls[[k]])}) #fit splines
```





<details open="open"><summary>Plate  1  -  10 </summary>
<p>
<iframe src="_book/widgets/Prolactin_p1_ls1.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>
<iframe src="_book/widgets/Prolactin_p1_ls2.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>
<iframe src="_book/widgets/Prolactin_p1_ls3.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>
<iframe src="_book/widgets/Prolactin_p1_ls4.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>
<iframe src="_book/widgets/Prolactin_p1_ls5.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>
<iframe src="_book/widgets/Prolactin_p1_ls6.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>
<iframe src="_book/widgets/Prolactin_p1_ls7.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>
<iframe src="_book/widgets/Prolactin_p1_ls8.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>
<iframe src="_book/widgets/Prolactin_p1_ls9.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>
<iframe src="_book/widgets/Prolactin_p1_ls10.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>

</p>
</details>

<details open="open"><summary>Plate  11  -  20 </summary>
<p>
<iframe src="_book/widgets/Prolactin_p1_ls11.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>
<iframe src="_book/widgets/Prolactin_p1_ls12.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>
<iframe src="_book/widgets/Prolactin_p1_ls13.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>
<iframe src="_book/widgets/Prolactin_p1_ls14.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>
<iframe src="_book/widgets/Prolactin_p1_ls15.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>
<iframe src="_book/widgets/Prolactin_p1_ls16.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>
<iframe src="_book/widgets/Prolactin_p1_ls17.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>
<iframe src="_book/widgets/Prolactin_p1_ls18.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>
<iframe src="_book/widgets/Prolactin_p1_ls19.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>
<iframe src="_book/widgets/Prolactin_p1_ls20.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>

</p>
</details>

<details open="open"><summary>Plate  21  -  30 </summary>
<p>
<iframe src="_book/widgets/Prolactin_p1_ls21.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>
<iframe src="_book/widgets/Prolactin_p1_ls22.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>
<iframe src="_book/widgets/Prolactin_p1_ls23.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>
<iframe src="_book/widgets/Prolactin_p1_ls24.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>
<iframe src="_book/widgets/Prolactin_p1_ls25.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>
<iframe src="_book/widgets/Prolactin_p1_ls26.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>
<iframe src="_book/widgets/Prolactin_p1_ls27.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>
<iframe src="_book/widgets/Prolactin_p1_ls28.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>
<iframe src="_book/widgets/Prolactin_p1_ls29.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>
<iframe src="_book/widgets/Prolactin_p1_ls30.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>

</p>
</details>

<details open="open"><summary>Plate  31  -  40 </summary>
<p>
<iframe src="_book/widgets/Prolactin_p1_ls31.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>
<iframe src="_book/widgets/Prolactin_p1_ls32.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>
<iframe src="_book/widgets/Prolactin_p1_ls33.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>
<iframe src="_book/widgets/Prolactin_p1_ls34.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>
<iframe src="_book/widgets/Prolactin_p1_ls35.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>
<iframe src="_book/widgets/Prolactin_p1_ls36.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>
<iframe src="_book/widgets/Prolactin_p1_ls37.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>
<iframe src="_book/widgets/Prolactin_p1_ls38.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>
<iframe src="_book/widgets/Prolactin_p1_ls39.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>
<iframe src="_book/widgets/Prolactin_p1_ls40.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>

</p>
</details>

<details open="open"><summary>Plate  41  -  50 </summary>
<p>
<iframe src="_book/widgets/Prolactin_p1_ls41.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>
<iframe src="_book/widgets/Prolactin_p1_ls42.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>
<iframe src="_book/widgets/Prolactin_p1_ls43.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>
<iframe src="_book/widgets/Prolactin_p1_ls44.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>
<iframe src="_book/widgets/Prolactin_p1_ls45.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>
<iframe src="_book/widgets/Prolactin_p1_ls46.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>
<iframe src="_book/widgets/Prolactin_p1_ls47.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>
<iframe src="_book/widgets/Prolactin_p1_ls48.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>
<iframe src="_book/widgets/Prolactin_p1_ls49.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>
<iframe src="_book/widgets/Prolactin_p1_ls50.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>

</p>
</details>

<details open="open"><summary>Plate  51  -  57 </summary>
<p>
<iframe src="_book/widgets/Prolactin_p1_ls51.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>
<iframe src="_book/widgets/Prolactin_p1_ls52.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>
<iframe src="_book/widgets/Prolactin_p1_ls53.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>
<iframe src="_book/widgets/Prolactin_p1_ls54.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>
<iframe src="_book/widgets/Prolactin_p1_ls55.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>
<iframe src="_book/widgets/Prolactin_p1_ls56.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>
<iframe src="_book/widgets/Prolactin_p1_ls57.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>

</p>
</details>

### Session info
**Results generated on: 2023-04-28 13:35:42**
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
##  [1] LC_CTYPE=en_AU.UTF-8       LC_NUMERIC=C              
##  [3] LC_TIME=en_AU.UTF-8        LC_COLLATE=en_AU.UTF-8    
##  [5] LC_MONETARY=en_AU.UTF-8    LC_MESSAGES=en_AU.UTF-8   
##  [7] LC_PAPER=en_AU.UTF-8       LC_NAME=C                 
##  [9] LC_ADDRESS=C               LC_TELEPHONE=C            
## [11] LC_MEASUREMENT=en_AU.UTF-8 LC_IDENTIFICATION=C       
## 
## attached base packages:
##  [1] parallel  splines   grid      stats     graphics  grDevices utils    
##  [8] datasets  methods   base     
## 
## other attached packages:
##  [1] widgetframe_0.3.1 fontawesome_0.5.1 doParallel_1.0.17 iterators_1.0.14 
##  [5] foreach_1.5.2     plotly_4.10.1     investr_1.4.2     readxl_1.4.2     
##  [9] htmlwidgets_1.6.2 kableExtra_1.3.4  knitr_1.42        rmarkdown_2.21   
## [13] ggplot2_3.4.2     devtools_2.4.5    usethis_2.1.6     pander_0.6.5     
## [17] magrittr_2.0.3    gridExtra_2.3     nvimcom_0.9-75   
## 
## loaded via a namespace (and not attached):
##  [1] httr_1.4.5        tidyr_1.3.0       sass_0.4.5        pkgload_1.3.2    
##  [5] jsonlite_1.8.4    viridisLite_0.4.1 bslib_0.4.2       shiny_1.7.4      
##  [9] highr_0.10        cellranger_1.1.0  yaml_2.3.7        remotes_2.4.2    
## [13] sessioninfo_1.2.2 pillar_1.9.0      glue_1.6.2        digest_0.6.31    
## [17] promises_1.2.0.1  rvest_1.0.3       colorspace_2.1-0  htmltools_0.5.5  
## [21] httpuv_1.6.9      pkgconfig_2.0.3   bookdown_0.33     purrr_1.0.1      
## [25] xtable_1.8-4      scales_1.2.1      webshot_0.5.4     processx_3.8.1   
## [29] svglite_2.1.1     later_1.3.0       tibble_3.2.1      generics_0.1.3   
## [33] ellipsis_0.3.2    cachem_1.0.7      withr_2.5.0       lazyeval_0.2.2   
## [37] cli_3.6.1         crayon_1.5.2      mime_0.12         memoise_2.0.1    
## [41] evaluate_0.20     ps_1.7.5          fs_1.6.1          fansi_1.0.4      
## [45] xml2_1.3.3        pkgbuild_1.4.0    data.table_1.14.8 profvis_0.3.7    
## [49] tools_4.2.3       prettyunits_1.1.1 lifecycle_1.0.3   stringr_1.5.0    
## [53] munsell_0.5.0     callr_3.7.3       compiler_4.2.3    jquerylib_0.1.4  
## [57] systemfonts_1.0.4 rlang_1.1.0       rstudioapi_0.14   crosstalk_1.2.0  
## [61] miniUI_0.1.1.1    codetools_0.2-19  gtable_0.3.3      R6_2.5.1         
## [65] dplyr_1.1.2       fastmap_1.1.1     utf8_1.2.3        stringi_1.7.12   
## [69] Rcpp_1.0.10       vctrs_0.6.2       tidyselect_1.2.0  xfun_0.39        
## [73] urlchecker_1.0.1
```
</details>

## HPL





### Data

```r
# standards
std_raw <- read_excel(file.path("..","data","hormones","HPL_absorbance_combined_20220728.xlsx"),sheet="SL  combined Abs standards")
std_raw$Abs.ave <- apply(std_raw[,c("Abs 1","Abs 2")],1,mean,na.rm=T) #average replicates
#std_raw$Abs.ave <- std_raw$"Abs Ave"
std_qc <- read.csv(file.path("..","data","hormones","HPL_QC.csv"),header=T) #standards QC
std_qc$Abs.ave <- apply(std_qc[,c("Abs.1","Abs.2")],1,mean,na.rm=T) #average replicates

# samples
samp_raw <- read_excel(file.path("..","data","hormones","HPL_absorbance_combined_20220728.xlsx"),sheet="SL combined Abs samples") #samples
samp_raw$Abs.ave <- apply(samp_raw[,c("Abs 1","Abs 2")],1,mean,na.rm=T) #average replicates
samp_raw$Abs.ave[samp_raw$Abs.ave<0] <- 0 #restrict to >=0
```

**Standard concentration by plate**
<details><summary>Click for more details</summary>
<table class=" lightable-classic" style='font-size: 18px; font-family: "Arial Narrow", "Source Sans Pro", sans-serif; width: auto !important; '>
 <thead>
<tr>
<th style="empty-cells: hide;" colspan="1"></th>
<th style="padding-bottom:0; padding-left:3px;padding-right:3px;text-align: center; " colspan="5"><div style="border-bottom: 1px solid #111111; margin-bottom: -1px; ">Concentration</div></th>
</tr>
  <tr>
   <th style="text-align:left;">   </th>
   <th style="text-align:right;"> St 0 </th>
   <th style="text-align:right;"> St 1.25 </th>
   <th style="text-align:right;"> St 10 </th>
   <th style="text-align:right;"> St 20 </th>
   <th style="text-align:right;"> St 5 </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td style="text-align:left;"> Assay 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 2 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 3 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 4 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 5 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 6 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 7 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 8 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 9 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 10 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 11 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 12 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 13 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 14 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 15 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 16 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 17 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 18 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 19 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 20 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 21 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 22 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 23 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 24 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 25 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 26 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 27 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 28 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 29 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 30 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 31 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 32 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 33 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 34 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 35 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 36 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 37 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 38 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 39 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 40 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 41 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 42 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 43 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 44 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 45 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 46 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 47 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 48 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 49 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 50 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 51 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 52 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 53 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 54 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 55 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 56 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 57 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
</tbody>
</table>

</details>

**Samples by plate**
<details><summary>Click for more details</summary>
<table class=" lightable-classic" style='font-size: 18px; font-family: "Arial Narrow", "Source Sans Pro", sans-serif; width: auto !important; '>
 <thead>
<tr>
<th style="empty-cells: hide;" colspan="1"></th>
<th style="padding-bottom:0; padding-left:3px;padding-right:3px;text-align: center; " colspan="3"><div style="border-bottom: 1px solid #111111; margin-bottom: -1px; ">Concentration</div></th>
</tr>
  <tr>
   <th style="text-align:left;">   </th>
   <th style="text-align:right;"> SCOPE </th>
   <th style="text-align:right;"> STOP </th>
   <th style="text-align:right;"> Total </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td style="text-align:left;"> Assay 1 </td>
   <td style="text-align:right;"> 39 </td>
   <td style="text-align:right;"> 0 </td>
   <td style="text-align:right;"> 39 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 2 </td>
   <td style="text-align:right;"> 5 </td>
   <td style="text-align:right;"> 35 </td>
   <td style="text-align:right;"> 40 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 3 </td>
   <td style="text-align:right;"> 5 </td>
   <td style="text-align:right;"> 35 </td>
   <td style="text-align:right;"> 40 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 4 </td>
   <td style="text-align:right;"> 5 </td>
   <td style="text-align:right;"> 34 </td>
   <td style="text-align:right;"> 39 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 5 </td>
   <td style="text-align:right;"> 5 </td>
   <td style="text-align:right;"> 35 </td>
   <td style="text-align:right;"> 40 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 6 </td>
   <td style="text-align:right;"> 5 </td>
   <td style="text-align:right;"> 34 </td>
   <td style="text-align:right;"> 39 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 7 </td>
   <td style="text-align:right;"> 5 </td>
   <td style="text-align:right;"> 35 </td>
   <td style="text-align:right;"> 40 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 8 </td>
   <td style="text-align:right;"> 5 </td>
   <td style="text-align:right;"> 35 </td>
   <td style="text-align:right;"> 40 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 9 </td>
   <td style="text-align:right;"> 5 </td>
   <td style="text-align:right;"> 35 </td>
   <td style="text-align:right;"> 40 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 10 </td>
   <td style="text-align:right;"> 5 </td>
   <td style="text-align:right;"> 35 </td>
   <td style="text-align:right;"> 40 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 11 </td>
   <td style="text-align:right;"> 4 </td>
   <td style="text-align:right;"> 36 </td>
   <td style="text-align:right;"> 40 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 12 </td>
   <td style="text-align:right;"> 4 </td>
   <td style="text-align:right;"> 36 </td>
   <td style="text-align:right;"> 40 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 13 </td>
   <td style="text-align:right;"> 4 </td>
   <td style="text-align:right;"> 36 </td>
   <td style="text-align:right;"> 40 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 14 </td>
   <td style="text-align:right;"> 4 </td>
   <td style="text-align:right;"> 36 </td>
   <td style="text-align:right;"> 40 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 15 </td>
   <td style="text-align:right;"> 4 </td>
   <td style="text-align:right;"> 36 </td>
   <td style="text-align:right;"> 40 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 16 </td>
   <td style="text-align:right;"> 4 </td>
   <td style="text-align:right;"> 36 </td>
   <td style="text-align:right;"> 40 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 17 </td>
   <td style="text-align:right;"> 4 </td>
   <td style="text-align:right;"> 36 </td>
   <td style="text-align:right;"> 40 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 18 </td>
   <td style="text-align:right;"> 23 </td>
   <td style="text-align:right;"> 18 </td>
   <td style="text-align:right;"> 41 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 19 </td>
   <td style="text-align:right;"> 12 </td>
   <td style="text-align:right;"> 0 </td>
   <td style="text-align:right;"> 12 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 20 </td>
   <td style="text-align:right;"> 27 </td>
   <td style="text-align:right;"> 13 </td>
   <td style="text-align:right;"> 40 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 21 </td>
   <td style="text-align:right;"> 22 </td>
   <td style="text-align:right;"> 18 </td>
   <td style="text-align:right;"> 40 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 22 </td>
   <td style="text-align:right;"> 22 </td>
   <td style="text-align:right;"> 18 </td>
   <td style="text-align:right;"> 40 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 23 </td>
   <td style="text-align:right;"> 15 </td>
   <td style="text-align:right;"> 25 </td>
   <td style="text-align:right;"> 40 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 24 </td>
   <td style="text-align:right;"> 15 </td>
   <td style="text-align:right;"> 25 </td>
   <td style="text-align:right;"> 40 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 25 </td>
   <td style="text-align:right;"> 26 </td>
   <td style="text-align:right;"> 14 </td>
   <td style="text-align:right;"> 40 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 26 </td>
   <td style="text-align:right;"> 23 </td>
   <td style="text-align:right;"> 17 </td>
   <td style="text-align:right;"> 40 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 27 </td>
   <td style="text-align:right;"> 23 </td>
   <td style="text-align:right;"> 17 </td>
   <td style="text-align:right;"> 40 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 28 </td>
   <td style="text-align:right;"> 18 </td>
   <td style="text-align:right;"> 22 </td>
   <td style="text-align:right;"> 40 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 29 </td>
   <td style="text-align:right;"> 21 </td>
   <td style="text-align:right;"> 19 </td>
   <td style="text-align:right;"> 40 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 30 </td>
   <td style="text-align:right;"> 20 </td>
   <td style="text-align:right;"> 20 </td>
   <td style="text-align:right;"> 40 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 31 </td>
   <td style="text-align:right;"> 17 </td>
   <td style="text-align:right;"> 23 </td>
   <td style="text-align:right;"> 40 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 32 </td>
   <td style="text-align:right;"> 30 </td>
   <td style="text-align:right;"> 10 </td>
   <td style="text-align:right;"> 40 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 33 </td>
   <td style="text-align:right;"> 18 </td>
   <td style="text-align:right;"> 22 </td>
   <td style="text-align:right;"> 40 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 34 </td>
   <td style="text-align:right;"> 25 </td>
   <td style="text-align:right;"> 15 </td>
   <td style="text-align:right;"> 40 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 35 </td>
   <td style="text-align:right;"> 25 </td>
   <td style="text-align:right;"> 15 </td>
   <td style="text-align:right;"> 40 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 36 </td>
   <td style="text-align:right;"> 23 </td>
   <td style="text-align:right;"> 17 </td>
   <td style="text-align:right;"> 40 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 37 </td>
   <td style="text-align:right;"> 24 </td>
   <td style="text-align:right;"> 16 </td>
   <td style="text-align:right;"> 40 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 38 </td>
   <td style="text-align:right;"> 22 </td>
   <td style="text-align:right;"> 18 </td>
   <td style="text-align:right;"> 40 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 39 </td>
   <td style="text-align:right;"> 20 </td>
   <td style="text-align:right;"> 20 </td>
   <td style="text-align:right;"> 40 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 40 </td>
   <td style="text-align:right;"> 25 </td>
   <td style="text-align:right;"> 15 </td>
   <td style="text-align:right;"> 40 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 41 </td>
   <td style="text-align:right;"> 21 </td>
   <td style="text-align:right;"> 19 </td>
   <td style="text-align:right;"> 40 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 42 </td>
   <td style="text-align:right;"> 20 </td>
   <td style="text-align:right;"> 20 </td>
   <td style="text-align:right;"> 40 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 43 </td>
   <td style="text-align:right;"> 14 </td>
   <td style="text-align:right;"> 26 </td>
   <td style="text-align:right;"> 40 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 44 </td>
   <td style="text-align:right;"> 24 </td>
   <td style="text-align:right;"> 16 </td>
   <td style="text-align:right;"> 40 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 45 </td>
   <td style="text-align:right;"> 17 </td>
   <td style="text-align:right;"> 23 </td>
   <td style="text-align:right;"> 40 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 46 </td>
   <td style="text-align:right;"> 21 </td>
   <td style="text-align:right;"> 19 </td>
   <td style="text-align:right;"> 40 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 47 </td>
   <td style="text-align:right;"> 18 </td>
   <td style="text-align:right;"> 22 </td>
   <td style="text-align:right;"> 40 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 48 </td>
   <td style="text-align:right;"> 23 </td>
   <td style="text-align:right;"> 17 </td>
   <td style="text-align:right;"> 40 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 49 </td>
   <td style="text-align:right;"> 22 </td>
   <td style="text-align:right;"> 18 </td>
   <td style="text-align:right;"> 40 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 50 </td>
   <td style="text-align:right;"> 21 </td>
   <td style="text-align:right;"> 19 </td>
   <td style="text-align:right;"> 40 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 51 </td>
   <td style="text-align:right;"> 20 </td>
   <td style="text-align:right;"> 20 </td>
   <td style="text-align:right;"> 40 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 52 </td>
   <td style="text-align:right;"> 21 </td>
   <td style="text-align:right;"> 19 </td>
   <td style="text-align:right;"> 40 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 53 </td>
   <td style="text-align:right;"> 28 </td>
   <td style="text-align:right;"> 12 </td>
   <td style="text-align:right;"> 40 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 54 </td>
   <td style="text-align:right;"> 26 </td>
   <td style="text-align:right;"> 14 </td>
   <td style="text-align:right;"> 40 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 55 </td>
   <td style="text-align:right;"> 23 </td>
   <td style="text-align:right;"> 17 </td>
   <td style="text-align:right;"> 40 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 56 </td>
   <td style="text-align:right;"> 18 </td>
   <td style="text-align:right;"> 22 </td>
   <td style="text-align:right;"> 40 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 57 </td>
   <td style="text-align:right;"> 19 </td>
   <td style="text-align:right;"> 14 </td>
   <td style="text-align:right;"> 33 </td>
  </tr>
</tbody>
</table>

</details>

### CV

```r
## Inter-assay CV
cv_dat <- std_qc
cv_dat$Group <- as.factor(with(cv_dat,Standard.conc..pg.ml.))
assay_ls <- split(cv_dat,cv_dat$Assay)
cv_mean_dat <- Reduce(rbind,lapply(assay_ls,function(x) tapply(x$Abs.Ave,x$Group,mean,na.tm=T)))
cv_mean <- apply(cv_mean_dat,2,mean,na.rm=T)
cv_sd <- apply(cv_mean_dat,2,sd,na.rm=T)
cv_gps <- (cv_sd/cv_mean)*100
cv_inter <- mean(cv_gps,na.rm=T)

## Intra-assay CV
samp_cv <- unlist(lapply(1:nrow(samp_raw),function(x){
				tmp_dat <- data.frame(samp_raw[x,])
			    tmp_mean <- mean(as.numeric(tmp_dat[5:6]))
			    tmp_sd <- sd(as.numeric(tmp_dat[5:6]))
			    return((tmp_sd/tmp_mean)*100)}))
cv_intra <- mean(samp_cv)
```
Inter-assay CV = 20% from 57 assays.<br />
Intra-assay CV = 7.81% from 2243 sample measurements.<br />

### Standard curves

```r
std_ls <- split(std_raw,std_raw$Assay) #split data by plate
fit.4PL <- function(x,a,b,g,d){return(d + ((a-d)/(1+((x/g)^b))))}
#f1 <- nls(Abs.ave ~ d + ((a-d)/(1+((Conc/g)^b))),data=std_ls[[1]],start=list(a=-1,b=1,g=5,d=2))

#std_fit <- lapply(1:length(std_ls),function(k){lm(Abs.ave ~ ns(Conc,df=3),data=std_ls[[k]])}) #fit splines
std_fit <- lapply(1:length(std_ls),function(k){ #fit 4PL
			  start_ls <- list(a=floor(min(std_ls[[k]][,c("Abs 1","Abs 2")])),
					   b=1,g=5,
					   d=ceiling(max(std_ls[[k]][,c("Abs 1","Abs 2")])))
			  fit <- NULL
			  try(fit <- nls(Abs.ave ~ fit.4PL(Conc,a,b,g,d),data=std_ls[[k]],start=start_ls),silent=T)
			  if(is.null(fit)){fit <- nlsLM(Abs.ave ~ fit.4PL(Conc,a,b,g,d),data=std_ls[[k]],start=start_ls)}
			  return(fit)})
```




<details open="open"><summary>Plate  1  -  10 </summary>
<p>
<iframe name="plotIframe" src="_book/widgets/HPL_p1_ls1.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>
<iframe name="plotIframe" src="_book/widgets/HPL_p1_ls2.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>
<iframe name="plotIframe" src="_book/widgets/HPL_p1_ls3.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>
<iframe name="plotIframe" src="_book/widgets/HPL_p1_ls4.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>
<iframe name="plotIframe" src="_book/widgets/HPL_p1_ls5.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>
<iframe name="plotIframe" src="_book/widgets/HPL_p1_ls6.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>
<iframe name="plotIframe" src="_book/widgets/HPL_p1_ls7.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>
<iframe name="plotIframe" src="_book/widgets/HPL_p1_ls8.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>
<iframe name="plotIframe" src="_book/widgets/HPL_p1_ls9.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>
<iframe name="plotIframe" src="_book/widgets/HPL_p1_ls10.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>

</p>
</details>

<details open="open"><summary>Plate  11  -  20 </summary>
<p>
<iframe name="plotIframe" src="_book/widgets/HPL_p1_ls11.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>
<iframe name="plotIframe" src="_book/widgets/HPL_p1_ls12.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>
<iframe name="plotIframe" src="_book/widgets/HPL_p1_ls13.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>
<iframe name="plotIframe" src="_book/widgets/HPL_p1_ls14.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>
<iframe name="plotIframe" src="_book/widgets/HPL_p1_ls15.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>
<iframe name="plotIframe" src="_book/widgets/HPL_p1_ls16.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>
<iframe name="plotIframe" src="_book/widgets/HPL_p1_ls17.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>
<iframe name="plotIframe" src="_book/widgets/HPL_p1_ls18.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>
<iframe name="plotIframe" src="_book/widgets/HPL_p1_ls19.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>
<iframe name="plotIframe" src="_book/widgets/HPL_p1_ls20.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>

</p>
</details>

<details open="open"><summary>Plate  21  -  30 </summary>
<p>
<iframe name="plotIframe" src="_book/widgets/HPL_p1_ls21.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>
<iframe name="plotIframe" src="_book/widgets/HPL_p1_ls22.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>
<iframe name="plotIframe" src="_book/widgets/HPL_p1_ls23.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>
<iframe name="plotIframe" src="_book/widgets/HPL_p1_ls24.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>
<iframe name="plotIframe" src="_book/widgets/HPL_p1_ls25.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>
<iframe name="plotIframe" src="_book/widgets/HPL_p1_ls26.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>
<iframe name="plotIframe" src="_book/widgets/HPL_p1_ls27.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>
<iframe name="plotIframe" src="_book/widgets/HPL_p1_ls28.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>
<iframe name="plotIframe" src="_book/widgets/HPL_p1_ls29.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>
<iframe name="plotIframe" src="_book/widgets/HPL_p1_ls30.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>

</p>
</details>

<details open="open"><summary>Plate  31  -  40 </summary>
<p>
<iframe name="plotIframe" src="_book/widgets/HPL_p1_ls31.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>
<iframe name="plotIframe" src="_book/widgets/HPL_p1_ls32.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>
<iframe name="plotIframe" src="_book/widgets/HPL_p1_ls33.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>
<iframe name="plotIframe" src="_book/widgets/HPL_p1_ls34.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>
<iframe name="plotIframe" src="_book/widgets/HPL_p1_ls35.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>
<iframe name="plotIframe" src="_book/widgets/HPL_p1_ls36.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>
<iframe name="plotIframe" src="_book/widgets/HPL_p1_ls37.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>
<iframe name="plotIframe" src="_book/widgets/HPL_p1_ls38.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>
<iframe name="plotIframe" src="_book/widgets/HPL_p1_ls39.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>
<iframe name="plotIframe" src="_book/widgets/HPL_p1_ls40.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>

</p>
</details>

<details open="open"><summary>Plate  41  -  50 </summary>
<p>
<iframe name="plotIframe" src="_book/widgets/HPL_p1_ls41.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>
<iframe name="plotIframe" src="_book/widgets/HPL_p1_ls42.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>
<iframe name="plotIframe" src="_book/widgets/HPL_p1_ls43.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>
<iframe name="plotIframe" src="_book/widgets/HPL_p1_ls44.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>
<iframe name="plotIframe" src="_book/widgets/HPL_p1_ls45.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>
<iframe name="plotIframe" src="_book/widgets/HPL_p1_ls46.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>
<iframe name="plotIframe" src="_book/widgets/HPL_p1_ls47.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>
<iframe name="plotIframe" src="_book/widgets/HPL_p1_ls48.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>
<iframe name="plotIframe" src="_book/widgets/HPL_p1_ls49.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>
<iframe name="plotIframe" src="_book/widgets/HPL_p1_ls50.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>

</p>
</details>

<details open="open"><summary>Plate  51  -  57 </summary>
<p>
<iframe name="plotIframe" src="_book/widgets/HPL_p1_ls51.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>
<iframe name="plotIframe" src="_book/widgets/HPL_p1_ls52.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>
<iframe name="plotIframe" src="_book/widgets/HPL_p1_ls53.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>
<iframe name="plotIframe" src="_book/widgets/HPL_p1_ls54.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>
<iframe name="plotIframe" src="_book/widgets/HPL_p1_ls55.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>
<iframe name="plotIframe" src="_book/widgets/HPL_p1_ls56.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>
<iframe name="plotIframe" src="_book/widgets/HPL_p1_ls57.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>

</p>
</details>

### Session info
**Results generated on: 2023-04-28 13:35:42**
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
##  [1] LC_CTYPE=en_AU.UTF-8       LC_NUMERIC=C              
##  [3] LC_TIME=en_AU.UTF-8        LC_COLLATE=en_AU.UTF-8    
##  [5] LC_MONETARY=en_AU.UTF-8    LC_MESSAGES=en_AU.UTF-8   
##  [7] LC_PAPER=en_AU.UTF-8       LC_NAME=C                 
##  [9] LC_ADDRESS=C               LC_TELEPHONE=C            
## [11] LC_MEASUREMENT=en_AU.UTF-8 LC_IDENTIFICATION=C       
## 
## attached base packages:
##  [1] parallel  splines   grid      stats     graphics  grDevices utils    
##  [8] datasets  methods   base     
## 
## other attached packages:
##  [1] minpack.lm_1.2-3  nlme_3.1-162      widgetframe_0.3.1 fontawesome_0.5.1
##  [5] doParallel_1.0.17 iterators_1.0.14  foreach_1.5.2     plotly_4.10.1    
##  [9] investr_1.4.2     readxl_1.4.2      htmlwidgets_1.6.2 kableExtra_1.3.4 
## [13] knitr_1.42        rmarkdown_2.21    ggplot2_3.4.2     devtools_2.4.5   
## [17] usethis_2.1.6     pander_0.6.5      magrittr_2.0.3    gridExtra_2.3    
## [21] nvimcom_0.9-75   
## 
## loaded via a namespace (and not attached):
##  [1] fs_1.6.1          webshot_0.5.4     httr_1.4.5        tools_4.2.3      
##  [5] profvis_0.3.7     bslib_0.4.2       utf8_1.2.3        R6_2.5.1         
##  [9] lazyeval_0.2.2    colorspace_2.1-0  urlchecker_1.0.1  withr_2.5.0      
## [13] tidyselect_1.2.0  prettyunits_1.1.1 processx_3.8.1    compiler_4.2.3   
## [17] cli_3.6.1         rvest_1.0.3       xml2_1.3.3        bookdown_0.33    
## [21] sass_0.4.5        scales_1.2.1      callr_3.7.3       systemfonts_1.0.4
## [25] stringr_1.5.0     digest_0.6.31     svglite_2.1.1     pkgconfig_2.0.3  
## [29] htmltools_0.5.5   sessioninfo_1.2.2 fastmap_1.1.1     highr_0.10       
## [33] rlang_1.1.0       rstudioapi_0.14   shiny_1.7.4       jquerylib_0.1.4  
## [37] generics_0.1.3    jsonlite_1.8.4    crosstalk_1.2.0   dplyr_1.1.2      
## [41] Rcpp_1.0.10       munsell_0.5.0     fansi_1.0.4       lifecycle_1.0.3  
## [45] stringi_1.7.12    yaml_2.3.7        pkgbuild_1.4.0    promises_1.2.0.1 
## [49] crayon_1.5.2      lattice_0.21-8    miniUI_0.1.1.1    ps_1.7.5         
## [53] pillar_1.9.0      codetools_0.2-19  pkgload_1.3.2     glue_1.6.2       
## [57] evaluate_0.20     data.table_1.14.8 remotes_2.4.2     vctrs_0.6.2      
## [61] httpuv_1.6.9      cellranger_1.1.0  gtable_0.3.3      purrr_1.0.1      
## [65] tidyr_1.3.0       cachem_1.0.7      xfun_0.39         mime_0.12        
## [69] xtable_1.8-4      later_1.3.0       viridisLite_0.4.1 tibble_3.2.1     
## [73] memoise_2.0.1     ellipsis_0.3.2
```
</details>


## GH2




### Data

```r
# standards
std_raw <- read_excel(file.path("..","data","hormones","GH2_absorbance_combined_20220728.xlsx"),sheet="SL combined Abs standards only") #standards
std_raw$Abs.ave <- apply(std_raw[,c("Abs 1","Abs 2")],1,mean,na.rm=T) #average replicates
std_raw$Abs.ave[std_raw$Abs.ave< 1e-10] <- 0

## samples
samp_raw <- read_excel(file.path("..","data","hormones","GH2_absorbance_combined_20220728.xlsx"),sheet="SL combined Abs samples") #samples
samp_raw$Abs.ave <- apply(samp_raw[,c("Abs 1","Abs 2")],1,mean,na.rm=T) #average replicates
```

**Standard concentration by plate**
<details><summary>Click for more details</summary>
<table class=" lightable-classic" style='font-size: 18px; font-family: "Arial Narrow", "Source Sans Pro", sans-serif; width: auto !important; '>
 <thead>
<tr>
<th style="empty-cells: hide;" colspan="1"></th>
<th style="padding-bottom:0; padding-left:3px;padding-right:3px;text-align: center; " colspan="8"><div style="border-bottom: 1px solid #111111; margin-bottom: -1px; ">Concentration</div></th>
</tr>
  <tr>
   <th style="text-align:left;">   </th>
   <th style="text-align:right;"> 0 </th>
   <th style="text-align:right;"> 78.125 </th>
   <th style="text-align:right;"> 156.25 </th>
   <th style="text-align:right;"> 312.5 </th>
   <th style="text-align:right;"> 625 </th>
   <th style="text-align:right;"> 1250 </th>
   <th style="text-align:right;"> 2500 </th>
   <th style="text-align:right;"> 5000 </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td style="text-align:left;"> Assay 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 2 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 3 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 4 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 5 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 6 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 7 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 8 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 9 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 10 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 11 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 12 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 13 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 14 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 15 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 16 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 17 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 18 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 19 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 20 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 21 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 22 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 23 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 24 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 25 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 26 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 27 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 28 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 29 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 30 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 31 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 32 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 33 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 34 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 35 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 36 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 37 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 38 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 39 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 40 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 41 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 42 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 43 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 44 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 45 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 46 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 47 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 48 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 49 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 50 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 51 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 52 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 53 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 54 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 55 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 56 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 57 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 58 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 59 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
</tbody>
</table>

</details>

**Samples by plate**
<details><summary>Click for more details</summary>
<table class=" lightable-classic" style='font-size: 18px; font-family: "Arial Narrow", "Source Sans Pro", sans-serif; width: auto !important; '>
 <thead>
<tr>
<th style="empty-cells: hide;" colspan="1"></th>
<th style="padding-bottom:0; padding-left:3px;padding-right:3px;text-align: center; " colspan="3"><div style="border-bottom: 1px solid #111111; margin-bottom: -1px; ">Concentration</div></th>
</tr>
  <tr>
   <th style="text-align:left;">   </th>
   <th style="text-align:right;"> SCOPE </th>
   <th style="text-align:right;"> STOP </th>
   <th style="text-align:right;"> Total </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td style="text-align:left;"> Assay 1 </td>
   <td style="text-align:right;"> 39 </td>
   <td style="text-align:right;"> 0 </td>
   <td style="text-align:right;"> 39 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 2 </td>
   <td style="text-align:right;"> 5 </td>
   <td style="text-align:right;"> 35 </td>
   <td style="text-align:right;"> 40 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 3 </td>
   <td style="text-align:right;"> 5 </td>
   <td style="text-align:right;"> 35 </td>
   <td style="text-align:right;"> 40 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 4 </td>
   <td style="text-align:right;"> 5 </td>
   <td style="text-align:right;"> 34 </td>
   <td style="text-align:right;"> 39 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 5 </td>
   <td style="text-align:right;"> 5 </td>
   <td style="text-align:right;"> 35 </td>
   <td style="text-align:right;"> 40 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 6 </td>
   <td style="text-align:right;"> 5 </td>
   <td style="text-align:right;"> 34 </td>
   <td style="text-align:right;"> 39 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 7 </td>
   <td style="text-align:right;"> 5 </td>
   <td style="text-align:right;"> 35 </td>
   <td style="text-align:right;"> 40 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 8 </td>
   <td style="text-align:right;"> 5 </td>
   <td style="text-align:right;"> 35 </td>
   <td style="text-align:right;"> 40 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 9 </td>
   <td style="text-align:right;"> 5 </td>
   <td style="text-align:right;"> 35 </td>
   <td style="text-align:right;"> 40 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 10 </td>
   <td style="text-align:right;"> 5 </td>
   <td style="text-align:right;"> 35 </td>
   <td style="text-align:right;"> 40 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 11 </td>
   <td style="text-align:right;"> 4 </td>
   <td style="text-align:right;"> 36 </td>
   <td style="text-align:right;"> 40 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 12 </td>
   <td style="text-align:right;"> 4 </td>
   <td style="text-align:right;"> 36 </td>
   <td style="text-align:right;"> 40 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 13 </td>
   <td style="text-align:right;"> 4 </td>
   <td style="text-align:right;"> 36 </td>
   <td style="text-align:right;"> 40 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 14 </td>
   <td style="text-align:right;"> 4 </td>
   <td style="text-align:right;"> 36 </td>
   <td style="text-align:right;"> 40 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 15 </td>
   <td style="text-align:right;"> 4 </td>
   <td style="text-align:right;"> 36 </td>
   <td style="text-align:right;"> 40 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 16 </td>
   <td style="text-align:right;"> 4 </td>
   <td style="text-align:right;"> 36 </td>
   <td style="text-align:right;"> 40 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 17 </td>
   <td style="text-align:right;"> 4 </td>
   <td style="text-align:right;"> 36 </td>
   <td style="text-align:right;"> 40 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 18 </td>
   <td style="text-align:right;"> 0 </td>
   <td style="text-align:right;"> 16 </td>
   <td style="text-align:right;"> 16 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 19 </td>
   <td style="text-align:right;"> 38 </td>
   <td style="text-align:right;"> 2 </td>
   <td style="text-align:right;"> 40 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 20 </td>
   <td style="text-align:right;"> 22 </td>
   <td style="text-align:right;"> 18 </td>
   <td style="text-align:right;"> 40 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 21 </td>
   <td style="text-align:right;"> 20 </td>
   <td style="text-align:right;"> 20 </td>
   <td style="text-align:right;"> 40 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 22 </td>
   <td style="text-align:right;"> 27 </td>
   <td style="text-align:right;"> 13 </td>
   <td style="text-align:right;"> 40 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 23 </td>
   <td style="text-align:right;"> 22 </td>
   <td style="text-align:right;"> 18 </td>
   <td style="text-align:right;"> 40 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 24 </td>
   <td style="text-align:right;"> 22 </td>
   <td style="text-align:right;"> 18 </td>
   <td style="text-align:right;"> 40 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 25 </td>
   <td style="text-align:right;"> 15 </td>
   <td style="text-align:right;"> 25 </td>
   <td style="text-align:right;"> 40 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 26 </td>
   <td style="text-align:right;"> 15 </td>
   <td style="text-align:right;"> 25 </td>
   <td style="text-align:right;"> 40 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 27 </td>
   <td style="text-align:right;"> 26 </td>
   <td style="text-align:right;"> 14 </td>
   <td style="text-align:right;"> 40 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 28 </td>
   <td style="text-align:right;"> 23 </td>
   <td style="text-align:right;"> 17 </td>
   <td style="text-align:right;"> 40 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 29 </td>
   <td style="text-align:right;"> 23 </td>
   <td style="text-align:right;"> 17 </td>
   <td style="text-align:right;"> 40 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 30 </td>
   <td style="text-align:right;"> 18 </td>
   <td style="text-align:right;"> 22 </td>
   <td style="text-align:right;"> 40 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 31 </td>
   <td style="text-align:right;"> 21 </td>
   <td style="text-align:right;"> 19 </td>
   <td style="text-align:right;"> 40 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 32 </td>
   <td style="text-align:right;"> 20 </td>
   <td style="text-align:right;"> 20 </td>
   <td style="text-align:right;"> 40 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 33 </td>
   <td style="text-align:right;"> 17 </td>
   <td style="text-align:right;"> 23 </td>
   <td style="text-align:right;"> 40 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 34 </td>
   <td style="text-align:right;"> 30 </td>
   <td style="text-align:right;"> 10 </td>
   <td style="text-align:right;"> 40 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 35 </td>
   <td style="text-align:right;"> 18 </td>
   <td style="text-align:right;"> 22 </td>
   <td style="text-align:right;"> 40 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 36 </td>
   <td style="text-align:right;"> 25 </td>
   <td style="text-align:right;"> 15 </td>
   <td style="text-align:right;"> 40 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 37 </td>
   <td style="text-align:right;"> 25 </td>
   <td style="text-align:right;"> 15 </td>
   <td style="text-align:right;"> 40 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 38 </td>
   <td style="text-align:right;"> 23 </td>
   <td style="text-align:right;"> 17 </td>
   <td style="text-align:right;"> 40 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 39 </td>
   <td style="text-align:right;"> 24 </td>
   <td style="text-align:right;"> 16 </td>
   <td style="text-align:right;"> 40 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 40 </td>
   <td style="text-align:right;"> 22 </td>
   <td style="text-align:right;"> 18 </td>
   <td style="text-align:right;"> 40 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 41 </td>
   <td style="text-align:right;"> 20 </td>
   <td style="text-align:right;"> 20 </td>
   <td style="text-align:right;"> 40 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 42 </td>
   <td style="text-align:right;"> 25 </td>
   <td style="text-align:right;"> 15 </td>
   <td style="text-align:right;"> 40 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 43 </td>
   <td style="text-align:right;"> 21 </td>
   <td style="text-align:right;"> 19 </td>
   <td style="text-align:right;"> 40 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 44 </td>
   <td style="text-align:right;"> 20 </td>
   <td style="text-align:right;"> 20 </td>
   <td style="text-align:right;"> 40 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 45 </td>
   <td style="text-align:right;"> 14 </td>
   <td style="text-align:right;"> 26 </td>
   <td style="text-align:right;"> 40 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 46 </td>
   <td style="text-align:right;"> 24 </td>
   <td style="text-align:right;"> 16 </td>
   <td style="text-align:right;"> 40 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 47 </td>
   <td style="text-align:right;"> 17 </td>
   <td style="text-align:right;"> 23 </td>
   <td style="text-align:right;"> 40 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 48 </td>
   <td style="text-align:right;"> 21 </td>
   <td style="text-align:right;"> 19 </td>
   <td style="text-align:right;"> 40 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 49 </td>
   <td style="text-align:right;"> 18 </td>
   <td style="text-align:right;"> 22 </td>
   <td style="text-align:right;"> 40 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 50 </td>
   <td style="text-align:right;"> 23 </td>
   <td style="text-align:right;"> 17 </td>
   <td style="text-align:right;"> 40 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 51 </td>
   <td style="text-align:right;"> 22 </td>
   <td style="text-align:right;"> 18 </td>
   <td style="text-align:right;"> 40 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 52 </td>
   <td style="text-align:right;"> 21 </td>
   <td style="text-align:right;"> 19 </td>
   <td style="text-align:right;"> 40 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 53 </td>
   <td style="text-align:right;"> 20 </td>
   <td style="text-align:right;"> 20 </td>
   <td style="text-align:right;"> 40 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 54 </td>
   <td style="text-align:right;"> 21 </td>
   <td style="text-align:right;"> 19 </td>
   <td style="text-align:right;"> 40 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 55 </td>
   <td style="text-align:right;"> 28 </td>
   <td style="text-align:right;"> 12 </td>
   <td style="text-align:right;"> 40 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 56 </td>
   <td style="text-align:right;"> 26 </td>
   <td style="text-align:right;"> 14 </td>
   <td style="text-align:right;"> 40 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 57 </td>
   <td style="text-align:right;"> 23 </td>
   <td style="text-align:right;"> 17 </td>
   <td style="text-align:right;"> 40 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 58 </td>
   <td style="text-align:right;"> 18 </td>
   <td style="text-align:right;"> 22 </td>
   <td style="text-align:right;"> 40 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Assay 59 </td>
   <td style="text-align:right;"> 19 </td>
   <td style="text-align:right;"> 14 </td>
   <td style="text-align:right;"> 33 </td>
  </tr>
</tbody>
</table>

</details>




### CV

```r
## Inter-assay CV
cv_dat <- std_raw[!std_raw$Assay%in%exc_plate,]
cv_dat <- std_raw
cv_dat$Group <- as.factor(with(cv_dat,get(conc_name)))
assay_ls <- split(cv_dat,cv_dat$Assay)
cv_mean_dat <- Reduce(rbind,lapply(assay_ls,function(x) tapply(x$"Abs Ave",x$Group,mean,na.tm=T)))
cv_mean <- apply(cv_mean_dat,2,mean,na.rm=T)
cv_sd <- apply(cv_mean_dat,2,sd,na.rm=T)
cv_gps <- (cv_sd/cv_mean)*100
cv_gps[is.nan(cv_gps)] <- 0
cv_inter <- mean(cv_gps,na.rm=T)

## Intra-assay CV
samp_cv <- unlist(lapply(1:nrow(samp_raw),function(x){
				tmp_dat <- data.frame(samp_raw[x,])
			    tmp_mean <- mean(as.numeric(tmp_dat[5:6]))
			    tmp_sd <- sd(as.numeric(tmp_dat[5:6]))
			    return((tmp_sd/tmp_mean)*100)}))
samp_cv[is.infinite(samp_cv)|samp_cv<0] <- NA
cv_intra <- mean(samp_cv,na.rm=T)
```
Inter-assay CV = 15.24% from 59 assays.<br />
Intra-assay CV = 3.78% from 2326 sample measurements.<br />

`<svg aria-hidden="true" role="img" viewBox="0 0 512 512" style="height:1em;width:1em;vertical-align:-0.125em;margin-left:auto;margin-right:auto;font-size:inherit;fill:red;overflow:visible;position:relative;"><path d="M256 512A256 256 0 1 0 256 0a256 256 0 1 0 0 512zM216 336h24V272H216c-13.3 0-24-10.7-24-24s10.7-24 24-24h48c13.3 0 24 10.7 24 24v88h8c13.3 0 24 10.7 24 24s-10.7 24-24 24H216c-13.3 0-24-10.7-24-24s10.7-24 24-24zm40-208a32 32 0 1 1 0 64 32 32 0 1 1 0-64z"/></svg>`{=html} <span style="color:red;"><b>Plate 22 (28-2-22) omitted due to invalid standard curve.</b></span><br />

### Standard curves

```r
std_ls <- split(std_raw,std_raw$Assay) #split data by plate
std_fit <- lapply(1:length(std_ls),function(k){lm(Abs.ave ~ ns(Conc,df=3),data=std_ls[[k]])}) #fit model
```




<details open="open"><summary>Plate  1  -  10 </summary>
<p>
<iframe src="_book/widgets/GH2_p1_ls1.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>
<iframe src="_book/widgets/GH2_p1_ls2.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>
<iframe src="_book/widgets/GH2_p1_ls3.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>
<iframe src="_book/widgets/GH2_p1_ls4.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>
<iframe src="_book/widgets/GH2_p1_ls5.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>
<iframe src="_book/widgets/GH2_p1_ls6.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>
<iframe src="_book/widgets/GH2_p1_ls7.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>
<iframe src="_book/widgets/GH2_p1_ls8.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>
<iframe src="_book/widgets/GH2_p1_ls9.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>
<iframe src="_book/widgets/GH2_p1_ls10.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>

</p>
</details>

<details open="open"><summary>Plate  11  -  20 </summary>
<p>
<iframe src="_book/widgets/GH2_p1_ls11.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>
<iframe src="_book/widgets/GH2_p1_ls12.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>
<iframe src="_book/widgets/GH2_p1_ls13.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>
<iframe src="_book/widgets/GH2_p1_ls14.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>
<iframe src="_book/widgets/GH2_p1_ls15.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>
<iframe src="_book/widgets/GH2_p1_ls16.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>
<iframe src="_book/widgets/GH2_p1_ls17.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>
<iframe src="_book/widgets/GH2_p1_ls18.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>
<iframe src="_book/widgets/GH2_p1_ls19.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>
<iframe src="_book/widgets/GH2_p1_ls20.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>

</p>
</details>

<details open="open"><summary>Plate  21  -  30 </summary>
<p>
<iframe src="_book/widgets/GH2_p1_ls21.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>
<iframe src="_book/widgets/GH2_p1_ls22.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>
<iframe src="_book/widgets/GH2_p1_ls23.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>
<iframe src="_book/widgets/GH2_p1_ls24.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>
<iframe src="_book/widgets/GH2_p1_ls25.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>
<iframe src="_book/widgets/GH2_p1_ls26.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>
<iframe src="_book/widgets/GH2_p1_ls27.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>
<iframe src="_book/widgets/GH2_p1_ls28.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>
<iframe src="_book/widgets/GH2_p1_ls29.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>
<iframe src="_book/widgets/GH2_p1_ls30.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>

</p>
</details>

<details open="open"><summary>Plate  31  -  40 </summary>
<p>
<iframe src="_book/widgets/GH2_p1_ls31.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>
<iframe src="_book/widgets/GH2_p1_ls32.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>
<iframe src="_book/widgets/GH2_p1_ls33.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>
<iframe src="_book/widgets/GH2_p1_ls34.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>
<iframe src="_book/widgets/GH2_p1_ls35.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>
<iframe src="_book/widgets/GH2_p1_ls36.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>
<iframe src="_book/widgets/GH2_p1_ls37.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>
<iframe src="_book/widgets/GH2_p1_ls38.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>
<iframe src="_book/widgets/GH2_p1_ls39.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>
<iframe src="_book/widgets/GH2_p1_ls40.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>

</p>
</details>

<details open="open"><summary>Plate  41  -  50 </summary>
<p>
<iframe src="_book/widgets/GH2_p1_ls41.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>
<iframe src="_book/widgets/GH2_p1_ls42.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>
<iframe src="_book/widgets/GH2_p1_ls43.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>
<iframe src="_book/widgets/GH2_p1_ls44.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>
<iframe src="_book/widgets/GH2_p1_ls45.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>
<iframe src="_book/widgets/GH2_p1_ls46.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>
<iframe src="_book/widgets/GH2_p1_ls47.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>
<iframe src="_book/widgets/GH2_p1_ls48.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>
<iframe src="_book/widgets/GH2_p1_ls49.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>
<iframe src="_book/widgets/GH2_p1_ls50.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>

</p>
</details>

<details open="open"><summary>Plate  51  -  59 </summary>
<p>
<iframe src="_book/widgets/GH2_p1_ls51.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>
<iframe src="_book/widgets/GH2_p1_ls52.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>
<iframe src="_book/widgets/GH2_p1_ls53.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>
<iframe src="_book/widgets/GH2_p1_ls54.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>
<iframe src="_book/widgets/GH2_p1_ls55.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>
<iframe src="_book/widgets/GH2_p1_ls56.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>
<iframe src="_book/widgets/GH2_p1_ls57.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>
<iframe src="_book/widgets/GH2_p1_ls58.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>
<iframe src="_book/widgets/GH2_p1_ls59.html" scrolling="no" seamless="seamless" frameBorder="0" loading="lazy" overflow="hidden" width="100%" height="300"></iframe>

</p>
</details>

### Session info
**Results generated on: 2023-04-28 13:35:42**
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
##  [1] LC_CTYPE=en_AU.UTF-8       LC_NUMERIC=C              
##  [3] LC_TIME=en_AU.UTF-8        LC_COLLATE=en_AU.UTF-8    
##  [5] LC_MONETARY=en_AU.UTF-8    LC_MESSAGES=en_AU.UTF-8   
##  [7] LC_PAPER=en_AU.UTF-8       LC_NAME=C                 
##  [9] LC_ADDRESS=C               LC_TELEPHONE=C            
## [11] LC_MEASUREMENT=en_AU.UTF-8 LC_IDENTIFICATION=C       
## 
## attached base packages:
##  [1] parallel  splines   grid      stats     graphics  grDevices utils    
##  [8] datasets  methods   base     
## 
## other attached packages:
##  [1] minpack.lm_1.2-3  nlme_3.1-162      widgetframe_0.3.1 fontawesome_0.5.1
##  [5] doParallel_1.0.17 iterators_1.0.14  foreach_1.5.2     plotly_4.10.1    
##  [9] investr_1.4.2     readxl_1.4.2      htmlwidgets_1.6.2 kableExtra_1.3.4 
## [13] knitr_1.42        rmarkdown_2.21    ggplot2_3.4.2     devtools_2.4.5   
## [17] usethis_2.1.6     pander_0.6.5      magrittr_2.0.3    gridExtra_2.3    
## [21] nvimcom_0.9-75   
## 
## loaded via a namespace (and not attached):
##  [1] fs_1.6.1          webshot_0.5.4     httr_1.4.5        tools_4.2.3      
##  [5] profvis_0.3.7     bslib_0.4.2       utf8_1.2.3        R6_2.5.1         
##  [9] lazyeval_0.2.2    colorspace_2.1-0  urlchecker_1.0.1  withr_2.5.0      
## [13] tidyselect_1.2.0  prettyunits_1.1.1 processx_3.8.1    compiler_4.2.3   
## [17] cli_3.6.1         rvest_1.0.3       xml2_1.3.3        bookdown_0.33    
## [21] sass_0.4.5        scales_1.2.1      callr_3.7.3       systemfonts_1.0.4
## [25] stringr_1.5.0     digest_0.6.31     svglite_2.1.1     pkgconfig_2.0.3  
## [29] htmltools_0.5.5   sessioninfo_1.2.2 fastmap_1.1.1     highr_0.10       
## [33] rlang_1.1.0       rstudioapi_0.14   shiny_1.7.4       jquerylib_0.1.4  
## [37] generics_0.1.3    jsonlite_1.8.4    crosstalk_1.2.0   dplyr_1.1.2      
## [41] Rcpp_1.0.10       munsell_0.5.0     fansi_1.0.4       lifecycle_1.0.3  
## [45] stringi_1.7.12    yaml_2.3.7        pkgbuild_1.4.0    promises_1.2.0.1 
## [49] crayon_1.5.2      lattice_0.21-8    miniUI_0.1.1.1    ps_1.7.5         
## [53] pillar_1.9.0      codetools_0.2-19  pkgload_1.3.2     glue_1.6.2       
## [57] evaluate_0.20     data.table_1.14.8 remotes_2.4.2     vctrs_0.6.2      
## [61] httpuv_1.6.9      cellranger_1.1.0  gtable_0.3.3      purrr_1.0.1      
## [65] tidyr_1.3.0       cachem_1.0.7      xfun_0.39         mime_0.12        
## [69] xtable_1.8-4      later_1.3.0       viridisLite_0.4.1 tibble_3.2.1     
## [73] memoise_2.0.1     ellipsis_0.3.2
```
</details>

