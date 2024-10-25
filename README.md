# Uber Trip Analysis Pipeline with MAGE, BigQuery, and Looker

This project demonstrates a comprehensive ETL pipeline designed to process, analyze, and visualize Uber trip data. Leveraging the MAGE open-source ETL tool, Google BigQuery for data storage and analysis, and Looker Studio for insightful data visualizations, this repository outlines a complete workflow for turning raw data into valuable business insights.

## Table of Contents

- [Project Overview](#project-overview)
- [Data Source](#data-source)
- [Pipeline Architecture](#pipeline-architecture)
- [Technologies Used](#technologies-used)
- [Setup and Usage](#setup-and-usage)
- [Dashboard](#dashboard)
- [Future Improvements](#future-improvements)
- [License](#license)

## Project Overview

This project automates the process of extracting, transforming, and loading Uber trip data, available [here](https://www.nyc.gov/site/tlc/about/tlc-trip-record-data.page), to Google BigQuery for analysis. A Looker dashboard presents visualizations that uncover trends and patterns in taxi ridership, allowing stakeholders to make data-driven decisions.

## Data Source

The dataset used is the NYC Taxi and Limousine Commission (TLC) Trip Record Data. It contains detailed information about taxi trips in NYC, including pickup and drop-off locations, timestamps, passenger counts, trip distances, fare amounts, and more.

## Pipeline Architecture

The pipeline is composed of the following stages:

1. **Extract:** NYC Taxi trip data is downloaded and stored in cloud storage.
2. **Transform:** Data transformation is performed using MAGE on a virtual machine. This includes data cleaning, standardization, and other transformations to prepare the data for analysis.
3. **Load:** The transformed data is loaded into Google BigQuery for efficient querying.
4. **Visualization:** Data is visualized using Looker Studio, providing an interactive dashboard that presents key insights.

### Workflow Diagram

#### 1. ETL Pipeline Workflow

![Uber_ETL_pipeline](https://github.com/user-attachments/assets/43fe36f1-548a-4276-8a33-73b344d15725)

The diagram above illustrates the ETL pipeline used in this project. The raw data is stored in Google Cloud Storage, processed and transformed using the MAGE tool, and then loaded into BigQuery for analysis. Finally, the data is visualized using Looker Studio.

#### 2. Data Model (Fact and Dimension Tables)

![Uber_data_model drawio](https://github.com/user-attachments/assets/c3ab755f-9731-4a0c-8a7c-f31a0e498165)

The diagram above represents the data model used in the project. It showcases the relationships between the fact table and dimension tables, enabling efficient querying and analysis.

## Technologies Used

- **[MAGE](https://www.mage.ai/):** An open-source ETL tool used for transforming the data on a virtual machine.
- **Google Cloud Storage:** Stores raw and transformed data.
- **Google BigQuery:** A highly scalable data warehouse used to store and query large datasets.
- **Looker Studio:** A visualization tool to create interactive dashboards for data insights.

## Setup and Usage

### Prerequisites

- Google Cloud Platform account
- Access to BigQuery, Google Cloud Storage, and Looker Studio
- MAGE ETL tool installed on a VM


### VM Setup Instructions

To set up the virtual machine for the ETL pipeline, follow the steps below:

1. **Update Package Lists:**

   ```bash
   sudo apt-get update
   sudo apt-get update
   sudo apt-get install python3-distutils
   sudo apt-get install wget
   sudo apt install python3-pip
   python3 -m venv myenv
   sudo apt install python3-venv
   source myenv/bin/activate
   python3 -m venv myenv
   source myenv/bin/activate
   python3 -m pip install --upgrade pip
   python3
   quit()
   pip3 install pandas
   pip3 install mage-ai
   pip3 install google-cloud
   pip install google-cloud-bigquery
   pip install db-dtypes
   mage start project_name
   

### Steps

1. **Download Data:** Download NYC Taxi trip data from the [NYC TLC data source](https://www.nyc.gov/site/tlc/about/tlc-trip-record-data.page) and upload it to Google Cloud Storage.

2. **Setup Virtual Machine with MAGE:**
   - Install and configure MAGE on a VM.
   - Connect MAGE to your Google Cloud Storage bucket and Google BigQuery.

3. **Define ETL Pipeline:**
   - Create ETL tasks in MAGE to clean, transform, and load the data.
   - Configure data transformations as per project requirements (e.g., filtering out incomplete records, data type standardization).

4. **Run ETL Pipeline:**
   - Execute the ETL pipeline to process the data and load it into BigQuery.

5. **Build Looker Dashboard:**
   - Connect Looker Studio to BigQuery and create a dashboard with visualizations showing key metrics (e.g., trip counts, average fare, peak hours).

6. **View and Share Insights:**
   - Use the Looker dashboard to gain insights and share the results with stakeholders.

## Dashboard

The Looker dashboard offers visualizations for:

- **Trip Distribution**: Analysis of trip count by date, time, and location.
- **Fare Analysis**: Breakdown of average fare amount over time.
- **Passenger Trends**: Insights into peak hours and high-demand locations.
- **Trip Distance Analysis**: Average trip distances segmented by time of day and location.

![Dashboard](https://github.com/user-attachments/assets/cbe94a3e-ff47-4ee1-91a0-b38674701308)

## Future Improvements

- **Data Enrichment**: Incorporate weather and event data to analyze their impact on taxi usage.
- **Machine Learning**: Predictive modeling to forecast demand patterns.
- **Automated Updates**: Schedule ETL jobs for regular updates to the BigQuery dataset and Looker dashboard.

## License

This project is open-source and available under the [MIT License](LICENSE).

---

### Contact

For questions or suggestions, feel free to contact me at [shrishubhamwagh@gmail.com] or open an issue in this repository.
