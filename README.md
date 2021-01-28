# Mix Leaf Area Index (MixLAI)

## Intrudoction

Globally, improving remotely sensed characterization of biophysical properties of vegetation is of paramount importance for a variety of applications. Changes of Plant Leaf Area and Its Relationships with Soil Factors in the Process of Grassland Desertification.In particular, the non-destructive estimation of the Leaf Area Index (LAI) from earth observation data has been topical for decades. LAI is defined as the one-sided green leaf area per unit ground area.
This script represents the leaf area index using the Sentinel 2 satellite. There are examples of this equation, but this equation uses the value of several different bands to calculate the leaf index value in a simple way.
Leaf area index is one of the most important parameters in determining plant yields.
On the other hand, agricultural scientists calculate this index using special hardware. But because of the global reach of the index in this method, the basis of validation is the data of MODIS product : MCD15A3H(500 M, 4 DAY).
The present script is the result of combining and simplifying the previous methods.

But the initial idea of ​​the script was based on the following basic method:

Lymburner, L., Beggs, P.J., Jacobson, C.R., 2000. Estimation of canopy-average surface-specific leaf area using Landsat TM data. Photogramm. Eng. Remote Sens. 66, 183–191.

## Validate

Leaf area index is one of the most important parameters in determining plant yields. On the other hand, agricultural scientists calculate this index using special hardware. But because of the global reach of the index in this method, the basis of validation is the data of MODIS product: MCD15A3H(500 M, 4 DAY).

 Random data analysis has been selected from all over the world. Product data is obtained from the following address:
https://lpdaacsvc.cr.usgs.gov/appeears/explore.

Pearson correlation and mean error methods were used to check the validity of the data. The average error is obtained with this method:

MAE = (ABS(MODIS - S2)/C); MAE:  mean absolute error; C: count image (Picture of the same day) in the year: Sep 2019-Sep2020.


exam point of world:

long	lat

-3.787585	40.089773

-4.991665	33.647475

75.28038	24.862526

24.106951	-31.276369

-82.253509	34.582171

-101.92016	22.943836

-73.503856	3.385921

149.130662	-30.375819

22.50151	45.943571

11.464104	43.512098

11.664784	51.26062

1.229418  44.669143

-122.048149	44.590588

-67.949633	-5.25761

## Exam Result

<img src="./report.jpg">

## Export Chart

<img src="./2.jpg">

## Export Image

<img src="./3.jpg">

## Function

MixLAI = ((B08/(B04+B11))+(B08/(B04+B12)))/2.0

## EO Browser View Code
https://apps.sentinel-hub.com/eo-browser/?zoom=12&lat=34.53951&lng=46.92638&themeId=DEFAULT-THEME&datasetId=S2L2A&fromTime=2020-09-20T00%3A00%3A00.000Z&toTime=2020-09-20T23%3A59%3A59.999Z&visualizationUrl=https%3A%2F%2Fservices.sentinel-hub.com%2Fogc%2Fwms%2Fbd86bcc0-f318-402b-a145-015f85b9427e&evalscript=dmFyIE1peExBSSA9ICgoQjA4LyhCMDQrQjExKSkrKEIwOC8oQjA0K0IxMikpKS8yLjAgLy8gY2FsY3VsYXRlIHRoZSBpbmRleAppZiAoTWl4TEFJPDAuMCkgcmV0dXJuIFswLDAsMF07CmVsc2UgaWYgKE1peExBSTwwLjI1KSByZXR1cm4gWzAuOTUsMC45NSwwLjhdOwplbHNlIGlmIChNaXhMQUk8MC41KSByZXR1cm4gWzAuOTMsMC45MSwwLjcxXTsKZWxzZSBpZiAoTWl4TEFJPDAuNzUpIHJldHVybiBbMC44NywwLjg1LDAuNjFdOwplbHNlIGlmIChNaXhMQUk8MS4wKSByZXR1cm4gWzAuNTcsMC43NSwwLjMyXTsKZWxzZSBpZiAoTWl4TEFJPDEuNSkgcmV0dXJuIFswLjQ0LDAuNjQsMC4yNV07CmVsc2UgaWYgKE1peExBSTwyLjApIHJldHVybiBbMC4zMSwwLjU0LDAuMThdOwplbHNlIGlmIChNaXhMQUk8Mi41KSByZXR1cm4gWzAuMTksMC40MywwLjExXTsKZWxzZSBpZiAoTWl4TEFJPDMuMCkgcmV0dXJuIFswLjU3LDAuNzUsMC4zMl07CmVsc2UgaWYgKE1peExBSTwzLjUpIHJldHVybiBbMC40NCwwLjY0LDAuMjVdOwplbHNlIGlmIChNaXhMQUk8NC4wKSByZXR1cm4gWzAuMzEsMC41NCwwLjE4XTsKZWxzZSBpZiAoTWl4TEFJPDQuNSkgcmV0dXJuIFswLjE5LDAuNDMsMC4xMV07CmVsc2UgaWYgKE1peExBSTw1LjApIHJldHVybiBbMC4wNiwwLjMzLDAuMDRdOwplbHNlIHJldHVybiBbMCwwLjE1LDBdOwoK#custom-script
