
# Wildfire Impact Analysis in McMinnville City
This project aims to analyze the impact of wildfires in McMinnville City, focusing on estimating smoke impacts over the last 60 years. The analysis involves data extraction, filtering, smoke estimation, and correlation with Air Quality Index (AQI) data. Additionally, a predictive model has been developed for future smoke estimates.

## Table of Contents
- [Wildfire Impact Analysis in McMinnville City](#wildfire-impact-analysis-in-mcminnville-city)
  * [Table of Contents](#table-of-contents)
  * [Introduction](#introduction)
  * [Common Analysis:](#common-analysis-)
  * [Data Sources](#data-sources)
  * [Project parts:](#project-parts-)
    + [Data Extraction](#data-extraction)
    + [Data Filtering and Preprocessing](#data-filtering-and-preprocessing)
    + [Smoke Estimation Process](#smoke-estimation-process)
    + [Correlation Analysis](#correlation-analysis)
    + [Predictive Model](#predictive-model)
    + [Data Visualization](#data-visualization)
    + [Challanges faced:](#challanges-faced-)
  * [Project Structure](#project-structure)
  * [Installation](#installation)
  * [Folder Structure](#folder-structure)
    + [Data Files](#data-files)
  * [Reproducing the Analysis](#reproducing-the-analysis)
  * [Contributing](#contributing)
  * [License](#license)

## Introduction

More and more frequently, summers in the western US have been characterized by wildfires, leading to extensive smoke impacting various aspects of society. This project focuses on McMinnville City's wildfire impact analysis and aims to provide insights into the city's historical and predicted smoke exposure.

## Common Analysis:

The course project involves a comprehensive analysis of the impact of wildfires on a specific city in the US. The goal is to inform policymakers and civic institutions, aiding them in making well-informed plans to mitigate potential future impacts from wildfires. The project consists of four parts, with Part 1 focusing on the common analysis, forming the foundation for subsequent assignments. Part 1 begins with data acquisition, where the Combined wildland fire datasets for the United States and certain territories, 1800s-Present, are utilized for the analysis. The assignment involves creating annual estimates of wildfire smoke impacts on the assigned city over the last 60 years (1963-2023). Additionally, the analysis includes the comparison of the created smoke estimates with the Air Quality Index (AQI) data from the US Environmental Protection Agency (EPA) to ascertain the accuracy of the estimations. Furthermore, a predictive model is developed to forecast smoke estimates for the city for the next 25 years, emphasizing the necessity of conveying appropriate levels of uncertainty in the predictions. Step 2 of the project involves the visualization of the analysis through various time series graphs. The visualizations include a histogram depicting the number of fires occurring at 50-mile intervals from the city, a time series graph illustrating the total acres burned per year for fires within a specific distance from the city, and a time series graph showcasing the fire smoke estimate for the city alongside the corresponding AQI estimate.


## Data Sources

USGS_Wildland_Fire_Combined_Dataset.json: The common analysis research question is based on one specific dataset which can be found at Combined wildland fire datasets for the United States and certain territories, 1800s-Present (combined wildland fire polygons). This dataset was collected and aggregated by the US Geological Survey. The dataset is relatively well documented. Fire polygons are available in ArcGIS and GeoJSON formats. We have been assigned one US city that will form the basis for our individual analysis. We can find our individual US city assignment from this Google spreadsheet.

The below sample codes were referenced for the following tasks and have been provided under the Creative Commons CC-BY license:

1. Sample notebook for Geodetic Distance Computation
2. Sample code for accessing the US EPA Air Quality System API
3. Sample code for GeoJSON reader

Link: https://drive.google.com/drive/folders/1OJktGAx86hvMtirCUkGnS292r-FpPvLo


## Project parts:

### Data Extraction

The dataset used for this analysis is the Combined Wildland Fire Datasets for the United States and certain territories, 1800s-Present (combined wildland fire polygons) collected and aggregated by the US Geological Survey. The project extracts and processes data using Python modules and various data processing techniques.

### Data Filtering and Preprocessing

Data filtering and preprocessing involve selecting fire perimeters within 1250 miles of McMinnville City, enabling the extraction of relevant fire data for analysis.

### Smoke Estimation Process

The smoke estimation process calculates and normalizes the smoke impact of each fire event based on defined parameters. The estimated smoke impacts are further processed and correlated with the available AQI data.

### Correlation Analysis

Correlation analysis involves exploring the relationship between the estimated smoke impacts and the Air Quality Index data, providing insights into the correlation between fire smoke and air quality in McMinnville City.

### Predictive Model

The project employs the Prophet library to develop a predictive model for future smoke estimates in McMinnville City, enabling the projection of potential smoke impacts over the next 25 years.

### Data Visualization

The data analysis results are visually represented through various time series graphs and histograms, providing a comprehensive view of the wildfire impact on McMinnville City.

### Challanges faced:
You can expect these to come if you're replicating steps. :)

1. Unavailability of Gaseous AQI Data: One of the prominent challenges was the unavailability of Gaseous AQI data for the assigned location. This absence hindered the optimization process, ultimately resulting in the removal of its calculation from the project.

2. Data Processing Interruption: While processing the data, the program encountered an unhandled exception, leading to an interruption. Consequently, the program stopped, and the need to rerun the process emerged, causing delays and potential data loss.

3. Data Unavailability for Specific Years: Another challenge was the absence of data for the years 1963-1983. This led to the modification of the program to start the loop from 1983, minimizing the risk of processing data for the unavailable time frame.

4. Handling Large Datasets: Processing and analyzing extensive wildfire datasets posed a significant challenge, requiring efficient handling and management of large volumes of data. Implementing strategies to optimize data processing and analysis became crucial to ensure the smooth execution of the project.

5. Data Extraction and Preprocessing: Extracting and preprocessing the wildfire dataset to extract relevant information required careful handling and processing. Managing the complexities associated with data extraction and ensuring the data was in a suitable format for analysis demanded meticulous attention to detail and expertise in data manipulation techniques.





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

### Data Files

- `aqi_by_year.json`: This JSON file contains the Air Quality Index (AQI) data organized by year. It includes information about corresponding AQI values for each year.

- `mcminnville_wildfire.json`: This JSON file includes wildfire data specific to McMinnville City. It contains information about the fire perimeters, locations, durations, and other relevant attributes of wildfires that have occurred in the vicinity of McMinnville City. The data can help analyze the impact of wildfires on the city and its surroundings.

- `normalized_smoke_estimate.json`: This JSON file contains the normalized smoke estimate data. It includes smoke estimations related to the smoke impact of each fire event, adjusted and normalized based on the min-max process. The normalized values provide a standardized representation of the smoke impact, facilitating comparison and analysis across different fire events.

- `wildfire.json`: This JSON file contains general wildfire data. It includes comprehensive information about various wildfires, including their locations, sizes, durations, and other relevant attributes.

## Reproducing the Analysis

To reproduce this analysis, follow these steps:

1. Clone this repository to the local machine.
2. Ensure that Python is installed with the required libraries.
3. Create a `data` folder in the project directory.
4. Download the GeoJSON Files.zip from this link and extract the "USGS_Wildland_Fire_Combined_Dataset.json" file and place it under the `data` folder.
5. Run 'wildfire_analysis.ipynb' to generate smoke analysis, AQI analysis, comparison between them, etc.
6. Analyze the results and interpret the findings accordingly.

Note: Due to the large size of the data, the 'data' folder has been included in the .gitignore file. Therefore, users need to create the 'data' folder themselves and manually download the necessary JSON files. Make sure to follow the steps mentioned above for proper reproduction of the analysis.

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
