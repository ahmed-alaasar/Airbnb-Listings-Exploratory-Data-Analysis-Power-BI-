# Airbnb Listings – Dataset Dictionary

The dataset contains snapshot information about Airbnb listings, including property characteristics, geographical locations, pricing, and host details.

| Column | Inferred Data Type | Description |
|---|---|---|
| listing_size | Numeric (Float) | Physical size of the property, likely measured in square meters or square feet. |
| instant_book | Boolean | Indicates whether a guest can book immediately without waiting for host approval (t/f). |
| review_score | Numeric (Integer) | Aggregated score based on guest reviews. |
| price | Numeric | Nightly rental price for the listing. |
| bedrooms | Numeric (Integer) | Total number of bedrooms available in the listing. |
| accommodates | Numeric (Integer) | Maximum number of guests the property can host. |
| property_type | Categorical (String) | Classification of the listing, such as a room in a boutique hotel or hotel. |
| longitude | Numeric (Float) | Geographic longitude coordinate of the property. |
| latitude | Numeric (Float) | Geographic latitude coordinate of the property. |
| city | Categorical (String) | City in which the listing is located. |
| neighbourhood | Categorical (String) | Local district, borough, or neighborhood of the listing. |
| host_total_listings | Numeric (Integer) | Total number of properties managed by the host. |
| host_is_superhost | Boolean | Indicates whether the host holds Superhost status (t/f). |
| host_acceptance_rate | Numeric (Float) | Percentage of guest booking requests accepted by the host. |
| host_response_rate | Numeric (Float) | Percentage of guest messages answered by the host. |
| host_since | Date (Integer) | Host registration date, formatted as YYYYMMDD. |
| host_id | String / ID | Unique identifier assigned to the host. |
| listing_id | String / ID | Unique identifier assigned to the listing. |

## Data Quality Notes

- **Zero values:** The price, bedrooms, and accommodates columns may contain zero values. A zero bedroom count may represent a studio, while zero price or accommodates values may indicate missing or unrecorded data.
- **Missing values:** Columns such as host_acceptance_rate may contain blank or null values.
- **ID formatting:** host_id and listing_id should be treated as text to avoid scientific notation or precision loss.
- **Date parsing:** host_since is stored as an integer in YYYYMMDD format and should be parsed as a date when needed.
