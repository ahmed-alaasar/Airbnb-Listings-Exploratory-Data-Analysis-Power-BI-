# Airbnb EDA – Power BI

## Project Overview

This project focuses on Exploratory Data Analysis (EDA) of Airbnb listings using Microsoft Power BI.

The project investigates missing values, performs descriptive statistical analysis, and addresses missing listing prices through city-level median imputation.

## Dataset Description

The dataset contains snapshot information about Airbnb listings, including property characteristics, geographical locations, pricing, and host details.

For the complete dataset description and data dictionary, refer to:

`Dataset/dataset_dictionary.md`

## Project Tasks

### 1. Missing Values Investigation

- Investigate missing values in the dataset.
- Identify columns containing blank values.
- Calculate the number of blank-priced listings.

### 2. Descriptive Analysis

Perform descriptive statistical analysis, organized into separate groups.

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

### 4. Power BI Report

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

## Repository Structure

| Folder | Description |
|---|---|
| Dataset | Dataset description and data dictionary |
| Missing_Values | Missing values investigation |
| Descriptive_Analysis | Descriptive statistical analysis |
| Data_Cleaning | Price imputation |
| PowerBI_Report | Power BI report file |
| Screenshots | Before and after cleaning report screenshots |

## Tools Used

- Microsoft Power BI
- Power Query
- DAX

## Project Status

In Progress
