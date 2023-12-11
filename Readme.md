# Wildfire Impact Analysis and Extension Plan in McMinnville City

This comprehensive project delves into the profound impact of wildfires on McMinnville City, specifically focusing on the estimation of smoke impacts over the past 60 years. The analysis involves intricate data extraction, meticulous filtering, robust smoke estimation processes, and a nuanced correlation with Air Quality Index (AQI) data. Additionally, a forward-thinking predictive model has been devised to anticipate smoke estimates for the forthcoming 25 years. This extension plan envisions incorporating the identified smoke impact insights into broader considerations, ranging from business implications to healthcare ramifications.

## Table of Contents
- [Wildfire Impact Analysis and Extension Plan in McMinnville City](#wildfire-impact-analysis-and-extension-plan-in-mcminnville-city)
  * [Table of Contents](#table-of-contents)
  * [Introduction](#introduction)
  * [Common Analysis:](#common-analysis-)
  * [Data Sources](#data-sources)
  * [Project parts:](#project-parts-)
    + [Part 1](#part-1)
      - [Data Extraction](#data-extraction)
      - [Data Filtering and Preprocessing](#data-filtering-and-preprocessing)
      - [Smoke Estimation Process](#smoke-estimation-process)
      - [Correlation Analysis](#correlation-analysis)
      - [Predictive Model](#predictive-model)
      - [Data Visualization](#data-visualization)
      - [Challenges Faced:](#challenges-faced-)
    + [Part 2](#part-2)
      - [Extension Plan - Part 1: Business Analysis](#extension-plan---part-1--business-analysis)
        * [Data Processing](#data-processing)
        * [Exploratory Data Analysis (EDA)](#exploratory-data-analysis--eda-)
        * [Visualization](#visualization)
        * [Conclusion](#conclusion)
      - [Extension Plan - Part 2: Healthcare Analysis](#extension-plan---part-2--healthcare-analysis)
        * [Data Processing](#data-processing-1)
        * [Exploratory Data Analysis (EDA)](#exploratory-data-analysis--eda--1)
        * [Visualization](#visualization-1)
        * [Conclusion](#conclusion-1)
    + [Extension Plan Results:](#extension-plan-results-)
  * [Project Structure](#project-structure)
  * [Installation](#installation)
  * [Folder Structure](#folder-structure)
    + [Data Files](#data-files)
  * [Reproducing the Analysis](#reproducing-the-analysis)
  * [Contributing](#contributing)
  * [License](#license)


## Introduction

With increasing frequency, wildfires in the western US have become synonymous with summers, unleashing extensive smoke that affects various facets of society. This project aims to illuminate the impact of wildfires on McMinnville City, unraveling insights into the city's historical and anticipated smoke exposure.

## Common Analysis:

The project encompasses a comprehensive analysis of wildfires' impact on a specific city in the US. The objective is to furnish policymakers and civic institutions with well-informed plans to mitigate potential future wildfire impacts. The analysis unfolds in four pivotal parts, with Part 1 setting the groundwork. It commences with data acquisition, utilizing the Combined Wildland Fire Datasets for the United States and certain territories from the US Geological Survey. The assignment spans the creation of annual estimates of wildfire smoke impacts on McMinnville City over the last six decades (1963-2023). The analysis also involves comparing these smoke estimates with the Air Quality Index (AQI) data from the US Environmental Protection Agency (EPA) to validate accuracy. Furthermore, the project entails developing a predictive model to forecast smoke estimates for the city over the next 25 years, emphasizing the importance of conveying appropriate levels of uncertainty in the predictions. Challenges faced during the analysis are also documented, shedding light on the intricacies involved in processing extensive wildfire datasets.

## Data Sources

**USGS_Wildland_Fire_Combined_Dataset.json:** This dataset serves as the bedrock for the common analysis, sourced from Combined Wildland Fire Datasets for the United States and certain territories, 1800s-Present (combined wildland fire polygons), collected and aggregated by the US Geological Survey. The dataset is well-documented and encompasses fire polygons available in ArcGIS and GeoJSON formats.

*Source:* [USGS Wildland Fire Combined Dataset](https://www.sciencebase.gov/catalog/item/61aa537dd34eb622f699df81)

*Sample codes referenced for tasks:*
1. Sample notebook for Geodetic Distance Computation
2. Sample code for accessing the US EPA Air Quality System API
3. Sample code for GeoJSON reader

*Link:* [Sample Codes](https://drive.google.com/drive/folders/1OJktGAx86hvMtirCUkGnS292r-FpPvLo)

**Health Care Data**

*Source:* Oregon Health Authority Hospital Reporting

*Link:* [Oregon Health Authority Hospital Reporting](https://www.oregon.gov/oha/hpa/analytics/pages/hospital-reporting.aspx)

*Databank Q1 2007 - Q2 2023.xlsx* The dataset from the Oregon Health Authority includes valuable health care information, such as hospitalizations, available beds, and hospital revenue. These metrics are essential for evaluating the potential impacts of wildfire smoke on the health care system in McMinnville.

*License/Terms of Use:* The dataset is hosted on the Oregon state government's data portal. The datasets are publicly available and can be used for research and analysis. [Terms of Use](https://www.tylertech.com/terms)

**Oregon Active Businesses**

*Source:* Oregon Active Businesses

*Link:* [Oregon Active Businesses](https://data.oregon.gov/business/Active-Businesses-ALL/tckn-sxa6)

*Active_Businesses_-_ALL.csv * This dataset contains information about active businesses in Oregon, including McMinnville. It includes details such as the name of the business, location, industry, and registration date. Analyzing this data provides insights into the economic landscape, business trends, and potential vulnerabilities of the local economy to external factors like wildfire events.

*License/Terms of Use:* The dataset is available on the Oregon Data website and follows the licensing terms provided, ensuring responsible and ethical use of the data. [Terms of Use](https://www.tylertech.com/terms)


## Project parts:

### Part 1
In this we will be caculating smoke estimate as this will set stage for our human-centered analysis.
#### Data Extraction

The project initiates with extracting and processing data from the Combined Wildland Fire Datasets for the United States and certain territories, 1800s-Present. Python modules and various data processing techniques are employed for this purpose.

#### Data Filtering and Preprocessing

Data filtering and preprocessing involve selecting fire perimeters within 1250 miles of McMinnville City, ensuring the extraction of relevant fire data for analysis.

#### Smoke Estimation Process

The smoke estimation process intricately calculates and normalizes the smoke impact of each fire event based on predefined parameters. The estimated smoke impacts are further processed and correlated with available AQI data.

#### Correlation Analysis

Correlation analysis explores the relationship between estimated smoke impacts and the Air Quality Index data. This provides valuable insights into the correlation between fire smoke and air quality in McMinnville City.

#### Predictive Model

The project utilizes

 the Prophet library to fashion a predictive model for future smoke estimates in McMinnville City. This facilitates the projection of potential smoke impacts over the next 25 years.

#### Data Visualization

The results of data analysis are visually represented through various time series graphs and histograms, offering a comprehensive view of the wildfire impact on McMinnville City.

#### Challenges Faced:

Expect these challenges if replicating steps:

1. **Unavailability of Gaseous AQI Data:** Prominently, the absence of Gaseous AQI data posed a challenge, impacting the optimization process and necessitating its removal from the project.

2. **Data Processing Interruption:** An unhandled exception during data processing led to an interruption, requiring a rerun of the process and potentially resulting in delays and data loss.

3. **Data Unavailability for Specific Years:** The absence of data for the years 1963-1983 led to a program modification, starting the loop from 1983 to minimize the risk of processing data for the unavailable timeframe.

4. **Handling Large Datasets:** Processing extensive wildfire datasets demanded efficient handling to ensure smooth execution. Strategies were implemented to optimize data processing and analysis.

5. **Data Extraction and Preprocessing:** Extracting and preprocessing the wildfire dataset required meticulous handling to ensure the data was in a suitable format for analysis.


### Part 2
In this we will be doing human-centered of analysis of smoke estimator caculated in project part 1.

#### Extension Plan - Part 1: Business Analysis
The primary goal of this extension plan is to perform a human-centered analysis of the smoke estimator's impact on various socio-economic factors, specifically within the business sector. The selected metric for evaluation is the number of registered businesses. This analysis aims to uncover how wildfires and associated smoke may influence business activities, investor decisions, and the overall economic well-being in McMinnville City.

##### Data Processing
1. **Data Acquisition:** Download the necessary CSV files from the provided link and store them in the 'data' folder with the exact names mentioned in the subsequent cells for reproducibility.
2. **Data Reading:** Utilize the Pandas library to read the CSV files and obtain the required business data for McMinnville City.
3. **Exploration:** Explore the dataset to verify its compatibility with the city and county where the smoke analysis was conducted.
4. **Preprocessing:** Clean and preprocess the data, extracting information relevant to the chosen socio-economic parameters.

##### Exploratory Data Analysis (EDA)
- **Unique Cities:** Investigate the dataset to ensure it contains data for McMinnville City and relevant surrounding areas.
- **Business Trends:** Analyze the trends in registered businesses over time, identifying any patterns or anomalies.

##### Visualization
Utilize visualizations such as line plots and bar charts to effectively communicate the business trends and their correlation with the smoke estimator. Visualization aids in presenting a comprehensive overview of the impact on the business sector in McMinnville City.

##### Conclusion
The insights gained from this analysis will contribute to understanding the dynamic relationship between wildfire smoke and the local business environment, providing valuable information for decision-makers. 
Although, there wasn't any trend noticed fo business, it was indeed an insightful study to do. The busines actvities weren't affcted by smoke.


#### Extension Plan - Part 2: Healthcare Analysis

Building on the human-centered approach, this phase of the extension plan focuses on evaluating the impact of the smoke estimator on healthcare metrics. Leveraging data from the Oregon Health Authority Hospital Reporting, the analysis includes hospitalizations, available beds, and hospital revenue. The objective is to discern the potential repercussions of wildfire smoke on the healthcare system in McMinnville. This entails evaluating aspects such as service demand, operational challenges, and financial considerations.

##### Data Processing
1. **Data Acquisition:** Access the healthcare dataset from the Oregon state government's data portal.
2. **Data Filtering:** Focus on extracting information related to hospitalizations, available beds, and hospital revenue.
3. **Preprocessing:** Clean and organize the healthcare data to prepare it for correlation analysis with the smoke estimator.

##### Exploratory Data Analysis (EDA)
- **Trends in Healthcare Metrics:** Explore trends in hospitalizations, available beds, and hospital revenue over the relevant timeframe.
- **Comparison with Smoke Estimator:** Correlate healthcare metrics with smoke impact data to identify potential relationships.

##### Visualization
Utilize visualizations, such as line plots and comparative charts, to present the impact of wildfire smoke on healthcare metrics. Visualization enhances the interpretability of complex healthcare data.

##### Conclusion
The findings from this analysis will contribute valuable insights into how the healthcare system in McMinnville responds to wildfire smoke events. This information is crucial for making informed decisions and implementing strategies to enhance healthcare resilience in the face of environmental challenges.

We found a positive relation between smoke estimate and hospitalizations, thus we can conclude that the healthcare of the system is affcted by smoke.


### Extension Plan Results:

**Business Impact Analysis:**
The extension plan envisions the integration of smoke impact insights into broader considerations. Specifically, analyzing the business impact of the estimated smoke on McMinnville City can provide valuable insights. Understanding how local businesses are affected, from disruptions to operations to economic implications, can guide business continuity planning and risk mitigation.

*Result*: No correlation between business and smoke estimation was discovered. With the smoke estimator, the number of registered businesses is rising. Cities' companies are impacted by a number of things, including regulations, admission rates, ease of doing business, etc. It was discovered that smoke had little effect on Yamhill County.

**Healthcare Ramifications:**
The extension plan also involves delving into the healthcare ramifications of smoke exposure. Analyzing the correlation between estimated smoke impacts and healthcare metrics, such as hospital admissions or respiratory health data, can offer insights into the public health consequences. This information is crucial for healthcare institutions and policymakers in devising strategies to address healthcare challenges arising from wildfire smoke.

*Result*: A positive correlation was seen between the healthcare data and the smoke estimator. Hospitalizations have been observed to increase in tandem with the smoke estimate. Therefore, it's critical to cut back on smoking because it has a harmful impact on health. Smoking can have a variety of negative health repercussions, such as respiratory conditions and psychological ones. 

## Project Structure

The project structure encompasses the main data processing and analysis scripts, alongside data visualization components. The repository includes additional documentation and resources relevant to the project.

## Installation

To install the required dependencies, use the following command:

```bash
pip install -r requirements.txt
```

## Folder Structure

The project folder comprises the following structure:

- **data:** Contains intermediate and final response files, including:
  - `aqi_by_year.json`: JSON file with AQI data organized by year.
  - `mcminnville_wildfire.json`: JSON file with wildfire data for McMinnville.
  - `normalized_smoke_estimate.json`: JSON file with normalized smoke estimate data.
  - `wildfire.json`: JSON file containing general wildfire data.
  - `Active_Businesses_-_ALL.csv`: CSV file for business data for Oregon state.
  - `Databank Q1 2007 - Q2 2023.xlsx`: EXCEL file for healthcare data for Oregon state.

- **libraries:** Contains external libraries and custom modules.
- **src:** Contains the main project file, 'wildfire_analysis.ipynb'.

### Data Files

- `aqi_by_year.json:` Air Quality Index (AQI) data organized by year.
- `mcminnville_wildfire.json:` Wildfire data specific to McMinnville City.
- `normalized_smoke_estimate.json:` Normalized smoke estimate data.
- `wildfire.json:` General wildfire data.

## Reproducing the Analysis

To reproduce this analysis:

1. Clone this repository to the local machine.
2. Ensure Python is installed with the required libraries.
3. Create a `data` folder in the project directory.
4. Download 'GeoJSON Files.zip' from [this link](#) and extract the "USGS_Wildland_Fire_Combined_Dataset.json" file, placing it under the `data` folder.
5. For extesion plan and human centered analysis, Download two files from the sources "Oregon Health Authority Hospital Reporting" [https://www.oregon.gov/oha/hpa/analytics/pages/hospital-reporting.aspx] and  "Oregon Active Businesses" [https://data.oregon.gov/business/Active-Businesses-ALL/tckn-sxa6]
6. Run 'wildfire_analysis.ipynb' to generate smoke analysis, AQI analysis, comparison, etc.
7. Run 'extension_data_exploration.ipynb' to generate the human-centered analysis.
6. Analyze the results and interpret the findings accordingly.

Note: Due to the large data size, the 'data' folder is included in the .gitignore file. Users need to create the 'data' folder and manually download the necessary JSON files, following the steps above for proper reproduction.

## Contributing

Contributions to this project are welcome. To contribute, follow these steps:

1. Fork the repository.
2. Create a new branch.
3. Make modifications.
4. Commit changes.
5. Push to the branch.
6. Open a pull request.

## License

This project is licensed under the MIT License - see the LICENSE file for details.