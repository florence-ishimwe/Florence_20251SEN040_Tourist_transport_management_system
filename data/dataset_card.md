# Dataset Card

## 1. Dataset Name
NYC Yellow Taxi Trip Records – January 2023

## 2. Data Source

- **Source:** NYC Taxi and Limousine Commission (TLC)
- **Dataset:** January 2023 Yellow Taxi Trip Records
- **Source link:** https://www.nyc.gov/site/tlc/about/tlc-trip-record-data.page

## 3. Licence

The dataset is publicly available from the New York City Taxi and Limousine Commission. Its use is subject to the terms and conditions provided by the TLC.

## 4. Dataset Format and Size

- **Format:** Excel Workbook (.xlsx)
- **Number of records:** 1,000
- **Number of columns:** 19
- **Data type:** Structured tabular data

## 5. Date Collected

The dataset was downloaded during the preparation of Phase 0 and Phase II of the project.

## 6. What One Record Represents

Each record represents one taxi trip in New York City during January 2023. The record contains information about the trip, including pickup and drop-off times, passenger count, trip distance, location IDs, fare amount and payment-related details.

## 7. Data Quality Report

The dataset was examined using Excel and data analysis
to identify missing values, duplicate records,
inconsistent text values and unusual numeric values.

The following results were obtained:

| Quality Check | Result |
|---|---:|
| Total records | 1,000 |
| Total columns | 19 |
| Missing values | 0 |
| Duplicate records | 0 |
| Negative fare amounts | 6 |
| Zero trip distances | 8 |
| Zero passenger counts | 13 |
| Non-numeric values in numeric columns | 0 |

The categorical column store_and_fwd_flag contains
two values: N (996 records) and Y (4 records).
No spelling variations were identified.

The unusual values have not been corrected.
They will be considered during the data cleaning
stage in Phase IV.
