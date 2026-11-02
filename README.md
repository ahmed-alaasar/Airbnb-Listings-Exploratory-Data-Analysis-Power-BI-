# Airbnb Listings – Exploratory Data Analysis | Power BI

An Exploratory Data Analysis project on **7,210 Airbnb listings** across Sydney, New York, Paris, and Rome. The project investigates missing and zero-priced records, calculates descriptive price statistics, applies city-level median imputation to blank prices, and presents the before/after report views in Power BI.

## Project at a glance

| Item | Details |
|---|---|
| Dataset | 7,210 rows × 18 columns |
| Cities | Sydney, New York, Paris, Rome |
| Main data issue | Missing and zero-valued listing prices |
| Cleaning approach | City-level median imputation for blank prices |
| BI tool | Microsoft Power BI |
| Transformation / modeling | Power Query and DAX |

## Dashboard preview

### Before cleaning

![Airbnb report before cleaning](ReportShots/Before%20Cleaning.png)

The raw-data view shows **7.21K listings**, **14 blank-priced listings**, and **37 listings priced at $0**. The visible price KPIs are average **149.76**, minimum **0.00**, median **87.00**, and maximum **10.57K**.

### After cleaning

![Airbnb report after cleaning](ReportShots/After%20Cleaning.png)

The total listing KPI remains **7.21K**. The blank-price and $0-price cards display `--`. The lower price-distribution visual uses `New_price (bins)`.

[Open the full screenshot comparison and report observations](ReportShots/EDA_Comparison.md).

## Dataset

The raw dataset is stored at [`Dataset/airbnb.csv`](Dataset/airbnb.csv). It contains listing identifiers, host information, property details, price, review score, location, booking information, and listing size.

The complete column descriptions and data quality notes are in the [Dataset Dictionary](Dataset/dataset_dictionary.md).

### Initial data quality findings

The counts below were calculated directly from the raw CSV in this repository.

| Field | Missing / blank | Zero values |
|---|---:|---:|
| `price` | 14 | 37 |
| `host_response_rate` | 3,057 | 344 |
| `bedrooms` | 797 | 0 |
| `accommodates` | 0 | 14 |
| `host_total_listings_count` | 8 | 2,383 |
| `property_type` | 14 | — |
| `listing_size_sqft` | 14 | — |
| `review_scores_rating` | 0 | 6 |

The city distribution is Sydney **2,110**, New York **2,100**, Paris **1,500**, and Rome **1,500** listings. See [Data Quality Findings](Analysis/Data_Quality_Findings.md) for the complete summary.

## Analysis and cleaning workflow

1. **Missing-value investigation:** identify blank fields and count blank-priced listings.
2. **Zero-value investigation:** distinguish actual zero values from blanks, particularly for price.
3. **Descriptive analysis:** calculate mean, median, minimum, maximum, and counts of zero-priced and blank-priced listings.
4. **City price analysis:** calculate city-level mean and median prices.
5. **Price imputation:** replace blank prices using the median price of the corresponding city.
6. **Power BI reporting:** compare the before-cleaning and after-cleaning report views.

The imputation method and its validation note are documented in [Price Cleaning and Imputation](Data_Cleaning/Price_Imputation.md).

## Power BI measures and calculated fields

The model screenshot shows a dedicated `_measures` table with measures for total listings, blank-priced listings, $0 listings, and average host acceptance rate, including after-cleaning variants.

It also shows price-related calculated fields and supporting columns, including `New_price`, `updated_price`, price bins, percentile fields, and IQR boundary fields. See the [Model Inventory](PowerBI_Model/Model_Inventory.md) and the [model screenshot](ReportShots/Measures%20NAd%20calculated%20columns.png).

The screenshot confirms the visible field names, but does not expose their formulas. Exact DAX expressions and Power Query steps should be added only from the actual PBIX definitions.

## Repository structure

```text
.
├── README.md
├── Dataset/
│   ├── airbnb.csv
│   └── dataset_dictionary.md
├── Analysis/
│   ├── Data_Quality_Findings.md
│   └── Descriptive_Analysis.md
├── Data_Cleaning/
│   └── Price_Imputation.md
├── PowerBI_Model/
│   └── Model_Inventory.md
├── Report/
│   └── Airbnb EDA.pbix
└── ReportShots/
    ├── Before Cleaning.png
    ├── After Cleaning.png
    ├── Measures NAd calculated columns.png
    └── EDA_Comparison.md
```

## Tools

- Microsoft Power BI
- Power Query
- DAX

## Important interpretation note

In the after-cleaning screenshot, the blank-price and $0-price cards show `--`, but the minimum-price KPI still shows **0.00**. The screenshots alone do not establish whether zero-priced rows were removed, replaced, or excluded only from specific measures. The corresponding DAX definitions and Power Query steps are needed to confirm that behavior.
