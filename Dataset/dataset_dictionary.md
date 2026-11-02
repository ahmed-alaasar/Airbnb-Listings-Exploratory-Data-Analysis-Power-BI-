# Airbnb Listings – Dataset Dictionary

The raw CSV contains 7,210 listing records and the following 18 columns.

| Column | Inferred data type | Description |
|---|---|---|
| `listing_id` | ID / Integer | Unique identifier assigned to the listing. Treat as an identifier, not a measure. |
| `host_id` | ID / Integer | Unique identifier assigned to the host. Treat as an identifier, not a measure. |
| `host_since_datekey` | Date key / Integer | Host registration date stored as YYYYMMDD. |
| `host_response_rate` | Numeric (Float) | Proportion of guest messages to which the host responds. |
| `host_acceptance_rate` | Numeric (Float) | Proportion of booking requests accepted by the host. |
| `host_is_superhost` | Boolean / Categorical | Indicates whether the host is a Superhost (`t` / `f`). |
| `host_total_listings_count` | Numeric (Integer) | Number of listings managed by the host. |
| `neighbourhood` | Categorical (String) | Neighborhood in which the listing is located. |
| `city` | Categorical (String) | City in which the listing is located. |
| `latitude` | Numeric (Float) | Geographic latitude of the listing. |
| `longitude` | Numeric (Float) | Geographic longitude of the listing. |
| `property_type` | Categorical (String) | Classification of the property. |
| `accommodates` | Numeric (Integer) | Maximum number of guests the listing accommodates. |
| `bedrooms` | Numeric (Integer) | Number of bedrooms in the listing. |
| `price` | Numeric | Nightly listing price. |
| `review_scores_rating` | Numeric | Aggregated guest review rating. |
| `instant_bookable` | Boolean / Categorical | Indicates whether instant booking is available (`t` / `f`). |
| `listing_size_sqft` | Numeric (Float) | Listing size in square feet. |

## Data Quality Notes

- `price` contains both blank values and zero values. These are investigated separately.
- `bedrooms`, `host_response_rate`, `host_total_listings_count`, `property_type`, and `listing_size_sqft` also contain missing values in the raw file.
- `host_id` and `listing_id` are identifiers and should be stored as text when numeric formatting could cause scientific notation or precision issues.
- `host_since_datekey` is stored as an integer in YYYYMMDD format and can be converted to a date for date-based analysis.
- A zero value is not automatically a missing value. Its meaning must be evaluated according to the relevant column.
