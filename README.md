# Airbnb Listings – Exploratory Data Analysis (Power BI)

An end-to-end Exploratory Data Analysis (EDA) project using Microsoft Power BI to investigate Airbnb listing data, identify data quality issues, analyze pricing patterns, and explore the relationship between listing characteristics, host performance, and geographical location.

## Project Overview

This project focuses on understanding Airbnb listing data through data quality investigation, descriptive statistics, data cleaning, and interactive visualization.

The primary objective is to transform raw listing data into meaningful insights while addressing missing values, invalid price records, and other data inconsistencies.

## Project Objectives

- Investigate missing values and data quality issues.
- Identify zero-priced listings and other potentially invalid records.
- Calculate descriptive statistics for important numerical variables.
- Analyze listing distribution across different cities and neighborhoods.
- Investigate pricing patterns and geographical differences.
- Impute missing listing prices using city-level median prices.
- Develop an interactive Power BI dashboard to communicate findings.

## Dataset Description

The dataset contains snapshot information about Airbnb listings, including property characteristics, geographical information, pricing, and host details.

### Dataset Columns

| Column | Description |
|---|---|
| listing_id | Unique identifier for each listing |
| host_id | Unique identifier for each host |
| listing_size | Physical size of the property |
| instant_book | Whether instant booking is available |
| review_score | Aggregated guest review score |
| price | Nightly listing price |
| bedrooms | Number of bedrooms |
| accommodates | Maximum guest capacity |
| property_type | Classification of the property |
| longitude | Geographic longitude |
| latitude | Geographic latitude |
| city | Listing's city |
| neighbourhood | Listing's neighborhood |
| host_total_listings | Total listings managed by the host |
| host_is_superhost | Whether the host is a Superhost |
| host_acceptance_rate | Host booking acceptance rate |
| host_response_rate | Host response rate |
| host_since | Host registration date |

## Project Workflow

### 1. Data Quality Investigation

The initial investigation focuses on understanding the condition of the raw dataset.

Main activities:

- Identify missing values across all columns.
- Calculate the number and percentage of missing records.
- Identify zero-priced listings.
- Investigate potentially invalid values in bedrooms and accommodates.
- Examine data types and formatting inconsistencies.
- Identify duplicate records where applicable.

### 2. Descriptive Analysis

Descriptive analysis is organized into separate groups.

**A. Price Analysis**
- Mean price.
- Median price.
- Minimum price.
- Maximum price.
- Number of listings with a $0 price.
- Number of listings with blank prices.

**B. Listing Analysis**
- Total number of listings.
- Listing distribution across cities.
- Distribution of property types.
- Average bedrooms and guest capacity.

**C. Host Analysis**
- Total number of hosts.
- Host acceptance rate.
- Host response rate.
- Superhost distribution.
- Average listings per host.

**D. City Analysis**
- Average listing price by city.
- Median listing price by city.
- Number of listings per city.
- Price distribution across neighborhoods.

### 3. Data Cleaning and Price Imputation

One of the main challenges in this dataset is the presence of missing and potentially invalid price values.

The cleaning process includes:

- Investigating missing prices separately from zero-priced listings.
- Evaluating the distribution of prices across different cities.
- Calculating the mean and median price for each city.
- Using the city-level median to replace missing price values.
- Preserving valid existing price records.
- Validating the results after imputation.

**Imputation Strategy:**

Missing listing prices are replaced using the median price of listings within the same city.

The median is preferred over the mean because it is less sensitive to extreme rental prices and outliers.

### 4. Power BI Dashboard

The dashboard provides an interactive overview of the dataset before and after cleaning.

Key dashboard metrics include:

- Total listings.
- Blank-priced listings.
- Zero-priced listings.
- Average price.
- Minimum price.
- Median price.
- Maximum price.

Additional visualizations explore listing distribution, host acceptance rates, and average prices across neighborhoods.

## Dashboard Preview

### Before Cleaning

![Before Cleaning](06_Screenshots/before_cleaning.png)

### After Cleaning

![After Cleaning](06_Screenshots/after_cleaning.png)

### Dashboard Overview

![Dashboard Overview](06_Screenshots/dashboard_overview.png)

## Repository Structure

```text
Airbnb-EDA-PowerBI/
│
├── README.md
│
├── 01_Dataset/
│   ├── airbnb_raw.csv
│   ├── airbnb_cleaned.csv
│   └── dataset_dictionary.md
│
├── 02_Data_Quality_Investigation/
│   ├── 01_Missing_Values/
│   ├── 02_Zero_Values/
│   └── 03_Data_Validation/
│
├── 03_Descriptive_Analysis/
│   ├── 01_Price_Analysis/
│   ├── 02_Listing_Analysis/
│   ├── 03_Host_Analysis/
│   └── 04_City_Analysis/
│
├── 04_Data_Cleaning/
│   ├── 01_Price_Imputation/
│   ├── 02_Missing_Values_Handling/
│   └── 03_Data_Type_Formatting/
│
├── 05_PowerBI_Dashboard/
│   ├── Airbnb_EDA.pbix
│   └── DAX_Measures.md
│
├── 06_Screenshots/
│   ├── before_cleaning.png
│   ├── after_cleaning.png
│   └── dashboard_overview.png
│
└── 07_Documentation/
    ├── data_cleaning_process.md
    └── analysis_findings.md
```

## Tools & Technologies

- **Microsoft Power BI:** Data modeling, data transformation, DAX, and visualization.
- **Power Query:** Data cleaning, transformation, and missing-value handling.
- **DAX:** Calculated measures and analytical metrics.

## Key Analytical Focus

This project emphasizes the importance of data quality before drawing business conclusions.

Particular attention is given to the difference between missing values and zero values, the impact of outliers on descriptive statistics, and the use of city-level median imputation to preserve geographical pricing differences.

## Project Status

In Progress – Data investigation, descriptive analysis, cleaning, and dashboard development.

## Author

Ahmed Al-aasar

Aspiring Data Analyst | SQL Server | Power BI | Data Analytics
