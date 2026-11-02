# Airbnb EDA – Power BI

## Project Overview

This project focuses on Exploratory Data Analysis (EDA) of Airbnb listings using Microsoft Power BI.

The project investigates missing values, performs descriptive statistical analysis, and addresses missing listing prices through city-level median imputation.

## Dataset Description

The dataset contains snapshot information about Airbnb listings, including property characteristics, geographical locations, pricing, and host details.

For the complete dataset description and data dictionary, refer to:

[Dataset Dictionary](Dataset/dataset_dictionary.md)

## Project Tasks

### 1. Missing Values Investigation

- Investigate missing values in the dataset.
- Identify columns containing blank values.
- Calculate the number of blank-priced listings.

### 2. Descriptive Analysis

**Price Analysis**
- Mean price.
- Median price.
- Maximum price.
- Minimum price.
- Total listings with a $0 price.
- Total listings with a blank price.

**City Price Analysis**
- Calculate the mean price for each city.
- Calculate the median price for each city.
- Create a table containing city-level mean and median prices for missing-price imputation.

### 3. Data Cleaning – Price Imputation

- Investigate blank listing prices.
- Calculate city-level median prices.
- Replace blank listing prices using the corresponding city median.

## Power BI Report

The Power BI report presents the analysis before and after cleaning.

The report includes:

- Blank-priced listings.
- Zero-priced listings.
- Total listings.
- Average price.
- Minimum price.
- Median price.
- Maximum price.
- Listing count by city.
- Average host acceptance rate by city.
- Neighborhood average price and review score.

[View the Before & After EDA Comparison](ReportShots/EDA_Comparison.md)

## Repository Structure

```text
Airbnb-Listings-Exploratory-Data-Analysis-Power-BI-/
│
├── README.md
│
├── Dataset/
│   ├── airbnb.csv
│   └── dataset_dictionary.md
│
├── Missing_Values/
│
├── Descriptive_Analysis/
│   ├── Price_Analysis/
│   └── City_Price_Analysis/
│
├── Data_Cleaning/
│   └── Price_Imputation/
│
├── Report/
│   └── Airbnb EDA.pbix
│
└── ReportShots/
    ├── Before Cleaning.png
    ├── After Cleaning.png
    ├── Measures NAd calculated columns.png
    └── EDA_Comparison.md
```

## Tools Used

- Microsoft Power BI
- Power Query
- DAX

## Project Status

Done
