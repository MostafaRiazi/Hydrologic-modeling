# Hydrologic-modeling
This repository showcases part of a project that simulates watershed hydrology using three sets of data: ground-truth, satellite-based, and bias corrected hydro-climatic data.

This study aims to simulate the Rainfall-Runoff (R-R) process within a watershed. Due to the lack of hydroclimatological data in the target area, remote sensing data was used. The Climate Hazards Group InfraRed Precipitation with Station data (CHIRPS) and Moderate Resolution Imaging Spectroradiometer/land surface temperature (MODIS-LST) data were obtained from Google Earth Engine. As the satellite-based hydroclimatology data is pixel data, the Thyssen polygon method was used to calculate the spatial average values of precipitation and temperature, which were then used as input for the models. To increase the accuracy of the modeling, an innovative pre-processing method called GF-WT was used. This method uses the Wavelet Transform analysis method followed by the Gaussian Filter analysis method to reveal hidden patterns in the data. The resulting data were then given to CatBoost and Voting algorithms, and their hyperparameters were tuned. Finally, the accuracy of each model was checked to determine the best performing model.

As such, the steps are as follows:
Step 1: pre-processing (Wavelet Transform)
Step 2: pre-processing (Gaussian Decomposition)
Step 3: pre-processing (Sliding Window)
Step 4: ML modeling & accuracy evaluation
Step 5: Visualization
