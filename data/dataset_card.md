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

- **Format:** Parquet (.parquet)
- **Number of records:** 1,000
- **Number of columns:** 19
- **Data type:** Structured tabular data

## 5. Date Collected

The dataset was downloaded during the preparation of Phase 0 and Phase II of the project.

## 6. What One Record Represents

Each record represents one taxi trip in New York City during January 2023. The record contains information about the trip, including pickup and drop-off times, passenger count, trip distance, location IDs, fare amount and payment-related details.

## 7. Data Quality Report

The dataset was examined to identify missing values, duplicate records and unusual values.

- **Missing values:** No missing values were found in the 19 columns.
- **Duplicate records:** No duplicate records were identified.
- **Negative fare amounts:** 6 records.
- **Zero trip distances:** 8 records.
- **Zero passenger counts:** 13 records.

These unusual values were identified during the preliminary data quality assessment. They have not yet been corrected because data cleaning will be performed during the implementation phase.

