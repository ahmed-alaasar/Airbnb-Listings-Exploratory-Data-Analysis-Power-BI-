# Data Quality Investigation

## Dataset Profile

The raw CSV contains **7,210 rows and 18 columns** across Sydney, New York, Paris, and Rome.

## Missing Values

| Column | Missing values |
|---|---:|
| host_response_rate | 3,057 |
| bedrooms | 797 |
| host_total_listings_count | 8 |
| property_type | 14 |
| price | 14 |
| listing_size_sqft | 14 |

The raw dataset contains **14 listings with a blank price**.

## Zero Values

| Column | Zero values |
|---|---:|
| price | 37 |
| accommodates | 14 |
| host_total_listings_count | 2,383 |
| review_scores_rating | 6 |

A zero value is not automatically equivalent to a missing value. The raw dataset contains **37 listings with a price of $0**.

## City Distribution

| City | Listings |
|---|---:|
| Sydney | 2,110 |
| New York | 2,100 |
| Paris | 1,500 |
| Rome | 1,500 |
| **Total** | **7,210** |

These figures describe the raw CSV currently stored in the repository.
