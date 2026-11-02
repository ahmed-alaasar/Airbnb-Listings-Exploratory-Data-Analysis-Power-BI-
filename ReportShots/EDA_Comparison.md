# Airbnb EDA – Before and After Cleaning

The Power BI report provides two views through its **Before Cleaning** and **After Cleaning** navigation buttons.

## Before Cleaning

![Airbnb report before cleaning](Before%20Cleaning.png)

The raw-data view shows **7.21K total listings**, **14 blank-priced listings**, and **37 listings priced at $0**. The displayed price KPIs are average **149.76**, minimum **0.00**, median **87.00**, and maximum **10.57K**.

The city chart shows Sydney **2,110**, New York **2,100**, Paris **1,500**, and Rome **1,500** listings. The average host acceptance-rate line displays approximately **64.33%**, **65.31%**, **49.06%**, and **48.92%**, respectively.

## After Cleaning

![Airbnb report after cleaning](After%20Cleaning.png)

The total listing KPI remains **7.21K**. The blank-price and $0-price cards display `--`. The visible price KPIs remain average **149.76**, minimum **0.00**, median **87.00**, and maximum **10.57K**.

The lower chart now uses `New_price (bins)` and displays the distribution across the shown price range. The neighborhood table displays average price and review score; its visible total row is **116.28** and **75**, respectively.

## What the screenshots show

- The report contains separate before-cleaning and after-cleaning states.
- The after-cleaning view uses a different price-bin field for the distribution visual.
- The blank-price and zero-price cards display `--` in the after-cleaning view.
- The minimum-price KPI still displays **0.00** in both screenshots. Therefore, these screenshots alone do not prove that all zero-priced records were removed or replaced. The underlying DAX measures and Power Query steps are needed to explain the exact treatment.

## Model Fields

![Power BI measures and calculated columns](Measures%20NAd%20calculated%20columns.png)

The Fields screenshot shows a dedicated `_measures` table and supporting price fields, bins, percentile fields, and IQR boundary fields. Their visible names and documentation are listed in [Model Inventory](../PowerBI_Model/Model_Inventory.md).