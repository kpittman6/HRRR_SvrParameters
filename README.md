Workflow:

1 - Cell Tracking
===========================
22 May 2019 Manual Storm Tracking (.pptx)
- the notated position of each cell on hourly composite reflectivity images from each of the three radars

5-22_Storms (REVISED) (.xlsx)
- The list of individual storms tracked on the .pptx document. 
- Has a storm ID code, Start and end time that 40+ dBZ composite reflectivity was present, the reason for storm demise (dissipate or merger, and with which cell), and which radar was used for tracking.
  It has the approximate centroid location and time of storm initiation (the first timestep it had 40+ dBZ composite reflectivity)
  It also has the centroid location/time for each subsequent radar volume that the storm had 40+ dBZ CR

5_22_ObservedMotion (.csv)
- observed storm motion calculation using approximate 40 dBZ CR centroid location and time

2 - QC Near-Inflow Points
===========================
QC_Cell_Tracks_Master_PostBuffer.csv
- 115 storms remained after spatial buffer around inflow points


5_22_VerticalProfs_QC_Grouped.csv
- 210 sounding points (by time, and lat/lon location); several other characteristics tagged

3 - Calculate HRRR Parameters on Vertical Profiles
===========================
HRRR_NearInflow_Parameters.ipynb
- downloads HRRR data from Amazon S3 bucket, and creates a .csv file (5-22_NearInflowParameters.csv) of parameters that is read into the stats code (HRRR_Parameter_Statistics.ipynb)


4 - Visualize Statistics on Vertical Profiles
===========================
HRRR_Parameter_Statistics.ipynb
- creates .png images of box and whisker plots of all parameters. Reads in PlotList.xlsx for titles, axis lables, and plot limits

BoxPlots: Directory of all the box and whisker plot .png images created by HRRR_Parameter_Statistics.ipynb
