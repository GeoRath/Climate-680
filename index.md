# Climate 680 Final Project

## __Exploring Tropical Relationships Between Sea Surface Height and ENSO from 1993-2015__
## _Geoffrey Rath_

## Introduction
The primary focus of my project is on sea surface height in the tropics between 15N-15S, as the tropics are a major location of upwelling of colder water from the deep ocean. Study of the tropical ocean may become even more critical as the impacts that anthropogenic warming may increase the area of the ocean classified as tropical waters. Sea surface height research is well documented but zooming in on the tropics and utilizing satellite data allows for clearer visualization of oceanic behavior and relationships. Relevant articles and citations to sea surface height will be included in the _References and Relevant Articles_ section below. Sea surface height varies globally and has far reaching impacts across the globe, these variations can be caused by wind stress, temperature fluctuations, as well as upwelling from the deep ocean.

Sea surface height is an important indicator of anthropogenic climate change and is a crucial element in flood mitigation, especially with around 80 percent of the global population living within 60 miles of the ocean. Sea level rise is being impcated both from an increase in sea surface temperature, SST, and melting sea ice. Warmer ocean waters cause water the ocean to expand and sea levels to rise, in addition global warming is melting sea ice as well as impacting ice formation on the poles which has added volume to the ocean and raised sea levels (Bamber; Hamlington et al 2016; WCRP) Rising ocean levels can and do cause billions of dollars in damage as well as posing a significant threat to human life as extreme flooding increases due to climate change.

An El Nino Southern Oscillation (ENSO) index will be used for comparison and to explore how sea surface height behaves during El Nino, La Nina, and Neutral conditions.

Associated Jupyter Notebooks are linked at the end of their corresponding section.

## Data

### AVISO

The data utilized in the following analysis is taken from the AVISO altimetry data from 1993-2015 from 15N-15S. AVISO is satellite derived sea surface height relative to the mean ocean surface of the Earth. AVISO's dataset was created by binning and averaging monthly values. AVISO stands for "Archiving, Validation, and Interpolation of Satellite Oceanographic data" 

The reference mission used for the altimeter inter-calibration processing is Topex/Poseidon between 1993-01-01 and 2002-04-23, Jason-1 between 2002-04-24 and 2008-10-18, OSTM/Jason-2 between 2008-10-19 and 2016-06-25, Jason-3 since 2016-06-25.

Those products were processed by SSALTO/DUACS and distributed by [AVISO+](https://www.aviso.altimetry.fr) with support from CNES.

Resolution: 1° grids

### ENSO Index

The NOAA 1/4° Daily Optimum Interpolation Sea Surface Temperature (OISST) is a long term Climate Data Record that incorporates observations from different platforms (satellites, ships, buoys and Argo floats) into a regular global grid. The dataset is interpolated to fill gaps on the grid and create a spatially complete map of sea surface temperature. Satellite and ship observations are referenced to buoys to compensate for platform differences and sensor biases.

NOAA High Resolution SST data provided by the NOAA/OAR/ESRL PSL, Boulder, Colorado, USA, from their Web site at [NOAA PSL](https://psl.noaa.gov/data/gridded/data.noaa.oisst.v2.highres.html#detail)

Resolution: 1/4° global grid

## Data Analysis
### General Characteristics

![12 Month Climatology](/Climate-680/Figures/12_month_clim.png)

Pictured above is the 12 month climatology for the monthly mean Sea Level Anomolies. As can be seen sea surface height anomalies vary widely across all 12 months. This mean average is run across the full span of the data from 1993-2015. This climatology illustrates sea surface height behaviors from month to month. From this climatology it is difficult to see what the overall mean behavior of the sea surface is but we can look at a plot of mean change in sea level anomalies to get a clearer image.

![AVISO Mean Decadal Difference](/Climate-680/Figures/aviso_decade_diff.png)

This plot shows the difference in sea level anomalies from the first decade, 1993-2003, and the last decade, 2005-2015. In this graph we can see that sea level anomalies are predominantly increasing in sea surface height except for in the eastern Pacific. This could be impacted from ENSO as well as upwelling of cooler water. Merrifield and Maltrud also discuss in their paper that this may also be impacted by multidecadal increases in the Pacific trade winds. This increase in trade winds is a seperate trend than that of La Nina events, but increases in trade winds have also been linked to global warming in multiple simulation models (Merrifield, M. A., and Maltrud, M. E.)

[Climatology Workbook](https://github.com/GeoRath/Climate-680/blob/master/Project_Workbooks/12_month_climatology.ipynb)

[Aviso Contour Data Workbook](https://github.com/GeoRath/Climate-680/blob/master/Project_Workbooks/aviso_contour.ipynb)

### Composite Analysis

![Nino 3.4 and AVISO Composite](/Climate-680/Figures/nino34_aviso_composite.png)

The specific question addressed in this composite analysis is what sea surface level anomalies are present during El Nino, La Nina, and Neutral conditions. The amount of events in the time band is denoted next to each graphs title, the composite graph contains data from all 12 months. 

During El Nino events the trade winds weaken and we will see warmer waters gathering in the eastern Pacific on the west coast of the United States. This also has a dampening effect on upwelling from the deep ocean and is often associated with wet conditions and rain in the southern United States. Contrarily, during La Nina the trade winds increase and push warm water towards Asia and bring an increase in upwelling of cool water from the deep ocean. These parameters often lead to droughts and drier conditions in the southern United States.

As can be seen in the El Nino subplot the anomalies present correspond well with known ENSO behavior. The La Nina subplot also shows similar maximum magnitudes to the El Nino graphic but in opposite regions, lower sea level in the Eastern Pacific and higher sea levels in the Western Pacific. The Neutral condition subplot shows that during neutral conditions there is very little anomolous sea level behavior.

[Composite Analysis Workbook](https://github.com/GeoRath/Climate-680/blob/master/Project_Workbooks/composite_analysis.ipynb)

### Correlation Coefficient

![Nino 3.4 and AVISO Correlation](/Climate-680/Figures/nino34_aviso_correlation.png)

As expected the correlation between ENSO and AVISO is strong. There is a strong positive correlation in the Eastern Pacific which agrees with our composite data showing anomolous sea levels under ENSO conditions. We also see that there is a negative correlation outside of the ocean directly impacted by ENSO behavior. The only region that does not show significance is the portion of the Atlantic Ocean captured in the region which agrees with previous research on ENSO conditions and behaviors (Cazenave; Hamlington et al 2021; WCRP).

[Correlation Workbook](https://github.com/GeoRath/Climate-680/blob/master/Project_Workbooks/aviso_nino34_correlation.ipynb)

### Regression

![Nino 3.4 and AVISO Regression Map](/Climate-680/Figures/nino34_aviso_regression.png)

In the above regression map we can see similar color gradients as the correlation graph but with no significance. This shows that the relationship between sea surface temperature and sea level anomalies is more complicated than a simple linear regression and that there are other variables that contribute to both of their behaviors, wind speed, cloud cover, and upwelling to name a few.

[Regression Workbook](https://github.com/GeoRath/Climate-680/blob/master/Project_Workbooks/aviso_nino34_regression.ipynb)

### Conda Environment and Resources
An environment.yml file can be found to define a consistent environment for the execution of the above code. All Jupyter Notebooks can be found in the Project Workbooks folder and created figures and graphs may be found in the Figures folder.

[Project Workbooks](https://github.com/GeoRath/Climate-680/tree/master/Project_Workbooks)

[Figures](https://github.com/GeoRath/Climate-680/tree/master/Figures)

[Environment](https://github.com/GeoRath/Climate-680/blob/master/environment.yml)

## Summary
Although my topic question was simple and already has a wealth of research behind it I still feel as though I have learned a lot from this project. I have learned a lot about coding in python and how to best utilze python to help me understand what my data is showing me. My data analysis also helped me visualize oceanic behaviors more clearly and helped me build a better understanding of how different variables in the ocean impact each other as well as how much is missing from painting the full picture of the ocean's behavior.

Technically, I had to work through NaN data creating issues in my data analysis as well as finding workarounds for computing around a large dataset like AVISO. I also furthered my competency with python but also found how to better address my own errors and problems with research and guides from different corners of the internet. In the future I would like to further explore other variables that impact sea surface height and work on making my plots more interesting to look at and find ways for them to provide even more context to the full story they can tell.

## References and Relevant Articles

Bamber J, et al. (2018). The land ice contribution to sea level during the satellite era. Environmental Research Letters : ERL., 13(6). (https://doi.org/10.1088/1748-9326/aac2f0)

Cazenave A, Henry O, Munier S, et al. Estimating ENSO Influence on the Global Mean Sea Level, 1993-2010. Marine Geodesy. 2012;35:82-97. (doi:10.1080/01490419.2012.718209)

Hamlington, B. D., Cheon, S. H., Thompson, P. R., Merrifield, M. A., Nerem, R. S., Leben, R. R., and Kim, K.-Y. (2016), An ongoing shift in Pacific Ocean sea level, J. Geophys. Res. Oceans, 121, 5084– 5097, (doi:10.1002/2016JC011815).

Hamlington, B. D., Frederikse, T., Thompson, P. R., Willis, J. K., Nerem, R. S., & Fasullo, J. T. (2021). Past, present, and future Pacific sea-level change. Earth's Future, 8, e2020EF001839. (https://doi.org/10.1029/2020EF001839)

Merrifield, M. A., and Maltrud, M. E. (2011), Regional sea level trends due to a Pacific trade wind intensification, Geophys. Res. Lett., 38, L21605, (doi:10.1029/2011GL049576).

WCRP Global Sea Level Budget Group: Global sea-level budget 1993–present, Earth Syst. Sci. Data, 10, 1551–1590, (https://doi.org/10.5194/essd-10-1551-2018), 2018.

### Acknowledgements
#### Timberlake - Executive Coding Assistant
![Ancient Beagle](/Climate-680/Timberlake.jpeg)

Always willing to lend a paw, forcefully, and without warning straight onto the keyboard.

I would also like to thank both Dr. Paul Dirmeyer and Dr. Natalie Burls for their knowledge, insight, and assistance throughout this project.

