
# Wildfire Impact Analysis in McMinnville City
This project aims to analyze the impact of wildfires in McMinnville City, focusing on estimating smoke impacts over the last 60 years. The analysis involves data extraction, filtering, smoke estimation, and correlation with Air Quality Index (AQI) data. Additionally, a predictive model has been developed for future smoke estimates.


## Introduction

More and more frequently, summers in the western US have been characterized by wildfires, leading to extensive smoke impacting various aspects of society. This project focuses on McMinnville City's wildfire impact analysis and aims to provide insights into the city's historical and predicted smoke exposure.

## Data Extraction

The dataset used for this analysis is the Combined Wildland Fire Datasets for the United States and certain territories, 1800s-Present (combined wildland fire polygons) collected and aggregated by the US Geological Survey. The project extracts and processes data using Python modules and various data processing techniques.

## Data Sources
The following is the data source:

USGS_Wildland_Fire_Combined_Dataset.json: The common analysis research question is based on one specific dataset which can be found at Combined wildland fire datasets for the United States and certain territories, 1800s-Present (combined wildland fire polygons). This dataset was collected and aggregated by the US Geological Survey. The dataset is relatively well documented. Fire polygons are available in ArcGIS and GeoJSON formats. We have been assigned one US city that will form the basis for our individual analysis. We can find our individual US city assignment from this Google spreadsheet.

The below sample codes were referenced for the following tasks and have been provided under the Creative Commons CC-BY license:

Sample notebook for Geodetic Distance Computation
Sample code for accessing the US EPA Air Quality System API
Sample code for GeoJSON reader

Link: https://drive.google.com/drive/folders/1OJktGAx86hvMtirCUkGnS292r-FpPvLo

## Reproducing the analysis
To reproduce this analysis, follow these steps:

1. Clone this repository to the local machine.
2. Ensure that Python is installed with the required libraries.
3. Download the GeoJSON Files.zip from this link and extract the "USGS_Wildland_Fire_Combined_Dataset.json" file and place it under the data folder.
4. Run wildfire_analysis.ipynb to generate smoke analysis, AQI analysis, comparision between them etc.
Analyze the results.

## Data Filtering and Preprocessing

Data filtering and preprocessing involve selecting fire perimeters within 1250 miles of McMinnville City, enabling the extraction of relevant fire data for analysis.

## Smoke Estimation Process

The smoke estimation process calculates and normalizes the smoke impact of each fire event based on defined parameters. The estimated smoke impacts are further processed and correlated with the available AQI data.

## Correlation Analysis

Correlation analysis involves exploring the relationship between the estimated smoke impacts and the Air Quality Index data, providing insights into the correlation between fire smoke and air quality in McMinnville City.

## Predictive Model

The project employs the Prophet library to develop a predictive model for future smoke estimates in McMinnville City, enabling the projection of potential smoke impacts over the next 25 years.

## Data Visualization

The data analysis results are visually represented through various time series graphs and histograms, providing a comprehensive view of the wildfire impact on McMinnville City.

Viz 1:
This histogram illustrates the distribution of wildfires based on their proximity to a specific city. The x-axis represents distance from the city in miles, divided into 50-mile intervals, while the y-axis indicates the number of wildfires.


![alt text](/images/viz1.png)


Viz 2:
This time series graph portrays the total acres burned by wildfires per year within a specified distance from the city. The x-axis represents the years, while the y-axis indicates the total acres burned by wildfires.

![alt text](/images/viz2.png)


Viz 3:
This time series graph presents the trends of the estimated fire smoke impact and the Air Quality Index (AQI) estimate for the city over the years. The x-axis represents the years, while the y-axis indicates the respective values of the fire smoke estimate and the AQI estimate.
![alt text](/images/viz3.png)

## Project Structure

The project structure includes the main data processing and analysis scripts, as well as the data visualization components. The repository also contains additional documentation and resources related to the project.

## Installation

To install the required dependencies, use the following command:


pip install -r requirements.txt




## Folder Structure

The project folder has the following structure:

- **data**: Contains the intermediate and final response files, including:
  - `aqi_by_year.json`: JSON file with AQI data organized by year.
  - `mcminnville_wildfire.json`: JSON file with wildfire data for McMinnville.
  - `normalized_smoke_estimate.json`: JSON file with normalized smoke estimate data.
  - `wildfire.json`: JSON file containing general wildfire data.

- **libraries**: Contains external libraries and custom modules.
- **src**: Contains the main project file, 'wildfire_analysis.ipynb'.




- `aqi_by_year.json`: This JSON file contains the Air Quality Index (AQI) data organized by year. It  includes information about corresponding AQI values for each year. 

- `mcminnville_wildfire.json`: This JSON file includes wildfire data specific to McMinnville City. It contains information about the fire perimeters, locations, durations, and other relevant attributes of wildfires that have occurred in the vicinity of McMinnville City. The data can help analyze the impact of wildfires on the city and its surroundings.

- `normalized_smoke_estimate.json`: This JSON file contains the normalized smoke estimate data. It  includes smoke estimations related to the smoke impact of each fire event, adjusted and normalized based on min-max process. The normalized values provide a standardized representation of the smoke impact, facilitating comparison and analysis across different fire events.

- `wildfire.json`: This JSON file contains general wildfire data. It  includes comprehensive information about various wildfires, including their locations, sizes, durations, and other relevant attributes. 


## Contributing
Contributions to this project are welcome. To contribute, follow these steps:

Fork the repository
Create a new branch
Make your modifications
Commit your changes
Push to the branch
Open a pull request

## License
This project is licensed under the MIT License - see the LICENSE file for details.
