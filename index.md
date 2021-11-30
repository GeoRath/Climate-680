# Climate 680 Final Project

## __Exploring Tropical Relationships Between Sea Surface Height and ENSO from 1993-2015__
## _Geoffrey Rath_

## Introduction
The primary focus of my project is on sea surface height in the tropics between 15N-15S, as the tropics are a major location of upwelling of colder water from the deep ocean. Study of the tropical ocean may become even more critical as the impacts that anthropogenic warming may increase the area of the ocean classified as tropical waters. Sea surface height research is well documented but zooming in on the tropics and utilizing satellite data allows for clearer visualization of oceanic behavior and relationships.

An El Nino Southern Oscillation (ENSO) index will be used for comparison and to explore how sea surface height behaves during El Nino, La Nina, and Neutral conditions.

Associated Jupyter Notebooks are linked at the end of their corresponding section.

## Data

### AVISO

The data utilized in the following analysis is taken from the AVISO altimetry data from 1993-2015 from 15N-15S. AVISO is satellite derived sea surface height relative to the mean ocean surface of the Earth. AVISO's dataset was created by binning and averaging monthly values. AVISO stands for "Archiving, Validation, and Interpolation of Satellite Oceanographic data" 

The reference mission used for the altimeter inter-calibration processing is Topex/Poseidon between 1993-01-01 and 2002-04-23, Jason-1 between 2002-04-24 and 2008-10-18, OSTM/Jason-2 between 2008-10-19 and 2016-06-25, Jason-3 since 2016-06-25.

Those products were processed by SSALTO/DUACS and distributed by [AVISO+](https://www.aviso.altimetry.fr) with support from CNES.

Resolution: 1 degree grids

### ENSO Index

The NOAA 1/4° Daily Optimum Interpolation Sea Surface Temperature (OISST) is a long term Climate Data Record that incorporates observations from different platforms (satellites, ships, buoys and Argo floats) into a regular global grid. The dataset is interpolated to fill gaps on the grid and create a spatially complete map of sea surface temperature. Satellite and ship observations are referenced to buoys to compensate for platform differences and sensor biases.

NOAA High Resolution SST data provided by the NOAA/OAR/ESRL PSL, Boulder, Colorado, USA, from their Web site at [NOAA PSL](https://psl.noaa.gov/data/gridded/data.noaa.oisst.v2.highres.html#detail)

Resoltion: 1/4 degree global grid

## Data Analysis
### General Characteristics

![12 Month Climatology](/Climate-680/Figures/12_month_clim.png)

Pictured above is the 12 month climatology for the monthly mean Sea Level Anomolies. As can be seen sea surface height anomalies vary widely across all 12 months. This mean average is run across the full span of the data from 1993-2015. This climatology illustrates sea surface height behaviors from month to month.

![AVISO Contour Plot](/Climate-680/Figures/aviso_contour.png)

This contour plot shows the mean change of sea level anomalies from 1993-2015. In it we can clearly see that the anomalous behavior of sea surface height shows a widespread increase in sea surface height across the measured domain.

[Climatology Workbook](https://github.com/GeoRath/Climate-680/blob/master/Project_Workbooks/12_month_climatology.ipynb)

[Aviso Contour Data Workbook](https://github.com/GeoRath/Climate-680/blob/master/Project_Workbooks/aviso_contour.ipynb)

### Composite Analysis

![Nino 3.4 and AVISO Composite](/Climate-680/Figures/nino34_aviso_composite.png)

The specific question addressed in this composite analysis is what sea surface level anomalies are present during El Nino, La Nina, and Neutral conditions. The amount of events in the time band is denoted next to each graphs title. As can be seen in the El Nino subplot the anomalies present correspond well with known ENSO behavior. The La Nina subplot also shows similar maximum magnitudes to the El Nino graphic but in opposite regions, lower sea level in the Eastern Pacific and higher sea levels in the Western Pacific. The Neutral condition subplot shows that during neutral conditions there is very little anomolous sea level behavior.

[Composite Analysis Workbook](https://github.com/GeoRath/Climate-680/blob/master/Project_Workbooks/composite_analysis.ipynb)

### Correlation Coefficient

![Nino 3.4 and AVISO Correlation](/Climate-680/Figures/nino34_aviso_correlation.png)

As expected the correlation between ENSO and AVISO is strong. There is a strong positive correlation in the Eastern Pacific which agrees with our composite data showing anomolous sea levels under ENSO conditions. We also see that there is a negative correlation outside of the ocean directly impacted by ENSO behavior. The only region that does not show significance is the portion of the Atlantic Ocean captured in the region which agrees with previous research on ENSO conditions and behaviors.

[Correlation Workbook](https://github.com/GeoRath/Climate-680/blob/master/Project_Workbooks/aviso_nino34_correlation.ipynb)

### Regression

![Nino 3.4 and AVISO Regression Map](/Climate-680/Figures/nino34_aviso_regression.png)

In the above regression map we can see similar color gradients as the correlation graph but with no significance. This shows that the relationship between sea surface temperature and sea level anomalies is more complicated than a simple linear regression and that there are other variables that contribute to both of their behaviors, wind speed, cloud cover, and upwelling to name a few.

[Regression Workbook](https://github.com/GeoRath/Climate-680/blob/master/Project_Workbooks/aviso_nino34_regression.ipynb)

### Conda Environment
An environment.yml file can be found to define a consistent environment for the execution of the above code.

## Summary
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Nunc congue nisi vitae suscipit. Sollicitudin ac orci phasellus egestas. Proin nibh nisl condimentum id venenatis a condimentum vitae sapien. Et magnis dis parturient montes nascetur ridiculus mus mauris. Nullam ac tortor vitae purus faucibus ornare suspendisse. Sed risus pretium quam vulputate dignissim suspendisse in. Tempor orci dapibus ultrices in iaculis nunc sed augue. Dolor magna eget est lorem. Nulla posuere sollicitudin aliquam ultrices sagittis orci a scelerisque. Auctor elit sed vulputate mi sit. Pulvinar pellentesque habitant morbi tristique senectus et netus. Pellentesque habitant morbi tristique senectus et. Praesent semper feugiat nibh sed pulvinar proin gravida hendrerit. Dui accumsan sit amet nulla facilisi morbi tempus iaculis. Elit eget gravida cum sociis natoque penatibus et magnis dis. Facilisi nullam vehicula ipsum a arcu cursus.

### Acknowledgements
#### Timberlake - Executive Coding Assistant
![Ancient Beagle](/Climate-680/Timberlake.jpeg)

Always willing to lend a paw, forcefully, and without warning straight onto the keyboard.





