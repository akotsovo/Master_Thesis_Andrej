# Master_Thesis_Andrej

Below is a list of the different jupyter notebooks including a short description.

Note: some notebooks have been executed on a local machine and some on the workstation.
      The workstation seems to have a problem with reading and writing parquet. 
      CSV has to be used inestad. Coordinates then need to be converted to be read correctly.
      The same accounts for other type formats like datetime and timedelta.

Note: Some (most) notebooks take a lot of time to be processed.

The final datasets for Tier, Nextbike and Public Transit can be found on the workstation in the folder
Andrej -> Final Datasets. Files sizes are large. 

In addition, all produced tables can be found in Andrej -> Tables

The notebooks are seperated in three categories, data preparation, descriptive analysis, 
regression analysis.

Data Preparation:

01_Reduce Stations
Description: Create buffers around stations and reduce VRS stations to city of Bonn


02_Reduce_Stations_with_Tier
Description: Reduce stations in Bonn buffer to Tier operating area
Note:  RUN NOTEBOOK 11 PRIOR !

03_Combine_VRS_Realtime
Description: Realtime data split into many files. Combine them into three different datasets. Read filenames and save them in data. 
Note: Three datasets because of computational limitations
     

04_Merge_Planed_with_Bonn_stations
Description: merge "planned" PT data with Bonn station dataset


05_Reduce_VRS_to_Bonn
Description: Reduce PT data to Bonn area and combine them 
Note: Kernel died sometimes. Maybe each vrs_real dataset need to be executed and exported to then import and merge them. 

06_Get_Reatlime_Timestamp
Description: Extrace timestamp from filenames for later use


07_Merge_VRS_Trip_Realtime
Description: Merging realtime data with trips data


08_Merge_and_Delay
Description: Merge stop times with realtim data and compute delays

09_Merge_Service_Transfer
Description: Check if service is in place and station has transfer to other lines

10_Latest_VRS_Data
Description: Reduce data to latest timespan (latest actual arrival/departure) times


11_Tier_Part1
Description: Clean trips, calculate trip characteristics


12_Tier_Part2
Description: Check which Tier trips started / ended at stations; add station details to Tier data


13_Tier_Part3
Description: Merge Tier with VRS data


14_Next_Part1
Description: Clean trips, calculate trip characteristics


15_Next_Part2
Description: Check which Nextbike trips started / ended at stations; add station details to Nextbike data


16_Next_Part3
Description: Merge Nextbike with VRS data


17_Merge_Tier_Next
Description: Merge Tier and Nextbike data (both already merged with PT)

18_Weather
Description: Add weather data


19_Holiday
Description: Add holiday


20_Extend_Data
Description: Add features



Descriptive Analysis

21_1_Desc_Data
Description: Analysis of Data and Sub Data set delay, no delay, nan delay (cancelled trips)

21_2_Desc_Time
Description: Definition and analysis of time spans according to literature


21_3_Desc_Weather
Description: Definition and analysis of weather conditions and categories according to literature


21_4_Desc_Delay
Description: Definition and analysis of delay spans


21_5_Desc_Station
Description: Analysis of station usage


21_6_Desc_Other
Description: Lines, PT vehicle types, Service

21_7_Other_Visualization
Description: Visualization


21_8_Details
Description: Combination and analysis of Notebooks 21_1 to 21_4


Regression 

22_1 Tier
Description: Regression models with tier_trips_count as dependent variable


22_2 Tier Ending at Station
Description: Regression models with tier_trips_end_at_station_count as dependent variable


22_3 Nextbike
Description: Regression models with nextbike_trips_count as dependent variable


22_4 Nextbike end at Station
Description: Regression models with nextbike_trips_end_at_station_count as dependent variable
