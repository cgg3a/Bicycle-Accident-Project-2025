These are files from a research project by Caleb Griffy analyzing bicycle crashes in Chicago.
For more information on how this data was collected and how it was used, please read the paper.
For a brief overview on what each file in this repository was for:

1) Data was collected from these sources as of April 11th, 2025:
https://data.cityofchicago.org/Transportation/Traffic-Crashes-Crashes/85ca-t3if/about_data
https://data.cityofchicago.org/Transportation/Traffic-Crashes-Vehicles/68nd-jvt3/about_data

Ensure that when downloading from the second source, the data is filtered to only bicycles first.
These datasets contain crashes in Chicago and information about the vehicles involved.
Copies of this data is not contained in this GitHub, as they are kept more up to date on the Chicago site for free.
However, the codes used on these files and how to use them is described in the paper.

2) The downloaded csv files were run through DataCleaning.ipynb.
This limited to crashes involving a bicycle, and split them into total, only fatal crashes, and only nonfatal crashes.

3) These files were used in the software QGIS in conjunction with the data from these sources:
https://data.cityofchicago.org/Transportation/Bike-Routes/hvv9-38ut/about_data

Using these together, files were created to split the crashes on whether the crashes were within range of a bike route.
Once all the crash types were decided, crashes of each type were counted for each of 29 traffic regions. The boundaries of these regions come from the data from this source:
https://data.cityofchicago.org/Transportation/Chicago-Traffic-Tracker-Historical-Congestion-Esti/kf7e-cur8/about_data

The results of this step are stored in "Crash Counts from QGIS"

4) The actual area of each region was determined in QGIS as well for a CSV titled Region_Area_Values.csv for use in finding crashes by area. To do this, the space of each region that occupies actual Chicago city land was measured. The Chicago boundaries were found with data from this source:
https://data.cityofchicago.org/Facilities-Geographic-Boundaries/Boundaries-City/ewy2-6yfk

5) The Average_Congestion.ipynb file is used to get the average congestion value for each of the regions, as discussed for the historical congestion estimate method in the paper. The results are stored in a file titled Avg_Congestions.csv for the next step. The Average_Congestion.ipynb uses data from this source:
https://data.cityofchicago.org/Transportation/Chicago-Traffic-Tracker-Historical-Congestion-Esti/kf7e-cur8/about_data

6) The file getCrashRatios.ipynb was used to determine the EB-Estimates and historical congestion estimates of each region. These resutls are stored in the folder "Final Results". These are compared in the figures generated, which are also stored in the folder "Final Figures". Interpretations of these figures and more information on how to read them is contained in the paper.
