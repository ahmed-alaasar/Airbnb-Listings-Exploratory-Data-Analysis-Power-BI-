# Price Cleaning and Imputation

The raw CSV contains 14 blank prices and 37 zero prices. These are separate conditions.

## City-level median imputation

1. Group listings by city.
2. Calculate the median price for each city.
3. Use the corresponding city median to replace blank prices.

The median is less sensitive to extreme prices than the mean.

## Validation note

The after-cleaning screenshot shows `--` for the blank-price and $0-price cards, but the minimum-price KPI still displays `$0.00`. The screenshots alone do not prove that zero-priced records were removed or replaced. The DAX measures and Power Query steps should be checked before claiming that.