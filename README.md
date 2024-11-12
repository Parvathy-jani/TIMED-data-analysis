# TIMED-data-analysis
TIMED Data Analysis

This repository contains the code and data analysis workflow for the TIMED (Thermosphere Ionosphere Mesosphere Energetics and Dynamics) dataset. The main objective is to process and analyze the data from the SABER (Sounding of the Atmosphere using Broadband Emission Radiometry) instrument aboard the TIMED satellite. The analysis focuses on extracting neutral density values at an altitude of 110 km and plotting daily average trends over specified months and years.
Overview

#This repository includes:

    Data Preprocessing and Parsing: Scripts to load and parse raw text files, extracting key variables like time, altitude, latitude, longitude, neutral density, and tangent altitude.
    Data Filtering: Filtering the data based on latitude and longitude bounds, and extracting neutral density values at a precise altitude (110 km).
    Monthly Analysis: Calculation of daily average neutral density values for specific months (January, February, etc.), and saving the results in CSV files.
    Data Visualization: Code for plotting the daily average neutral density values relative to a chosen end date for different months.
    Combined Plotting: Combining multiple CSVs from different months and plotting them for comparative analysis.
    
  Requirements

To run this repository, you will need to have the following Python libraries installed:

    pandas
    numpy
    matplotlib

    Instructions

    Data Parsing and Filtering
        The script starts by reading the input data file (TIMED_L2A_SABER_3191544.txt) line by line.
        It extracts key data such as time, altitude, latitude, longitude, neutral density, and tangent altitude.
        The data is then filtered based on the latitude and longitude ranges defined in the code.

    Neutral Density Calculation
        For each data point, the neutral density at the altitude of 110 km is extracted if the tangent altitude is close to 110 km (within ±0.1 km).
        Any missing or erroneous data is handled by excluding or assigning NaN values.

    Monthly Analysis
        After filtering the data, the neutral density values are averaged daily, and the results are saved as CSV files for different months (e.g., December 2009, January 2010, February 2010).

    Plotting and Visualization
        The data_processing_and_analysis.ipynb Jupyter notebook combines the data from different months into a single dataset and plots the daily average neutral density values.
        The plot shows the trend of neutral density relative to a chosen end date, with the option to save the figure as a .png file.

    Final Output
        The final results, including the CSV files and the plot, are saved in the results/ directory.

Example Usage

Here’s a high-level overview of the steps in the notebook:

    Load and parse the raw text file (TIMED_L2A_SABER_3191544.txt).
    Filter the data based on latitude and longitude.
    Extract neutral density values at the 110 km tangent altitude.
    Calculate daily averages for specific months and save the results to CSV files.
    Combine the monthly CSV files and plot the daily neutral density values over time.
  

