# Data Normalization

## 1. Entity Identification

The NYC Yellow Taxi Trip Records dataset contains
information about taxi trips, vendors, pickup and
drop-off locations, rate codes and payment types.

The following entities were identified:

1. TRIP
2. VENDOR
3. LOCATION
4. RATE_CODE
5. PAYMENT_TYPE

The TRIP entity stores the main trip information.
The other entities store identifiers that are
repeated across multiple trip records.

## 2. Entity Relationships and Keys

The identified entities are connected through
primary keys and foreign keys.

- VENDOR has a one-to-many relationship with TRIP.
- LOCATION has a one-to-many relationship with TRIP
  for pickup locations.
- LOCATION has a one-to-many relationship with TRIP
  for drop-off locations.
- RATE_CODE has a one-to-many relationship with TRIP.
- PAYMENT_TYPE has a one-to-many relationship with TRIP.

A new TripID will be introduced as the primary key
of the TRIP table because the original dataset does
not contain a dedicated trip identifier.

The TRIP table will contain foreign keys that
reference the other four entities.

## 3. Unnormalized Form (UNF)

The original NYC Yellow Taxi dataset is stored in
one wide table containing 19 columns.

Each row represents one taxi trip. The table contains
trip information, vendor identifiers, pickup and
drop-off location identifiers, rate codes and
payment information.

At this stage, all information remains together
in the original structure without being separated
into related tables.

### 3.1 Sample Records

The following three records were selected from the
original dataset to demonstrate the UNF structure.

| VendorID | Pickup DateTime | Drop-off DateTime | Passenger Count | Trip Distance | RatecodeID | Store Flag | PULocationID | DOLocationID | Payment Type | Fare Amount | Extra | MTA Tax | Tip Amount | Tolls Amount | Improvement Surcharge | Total Amount | Congestion Surcharge | Airport Fee |
|---|---|---|---:|---:|---:|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| 2 | 2023-01-01 00:32:10 | 2023-01-01 00:40:36 | 1 | 0.97 | 1 | N | 161 | 141 | 2 | 9.30 | 1.00 | 0.50 | 0.00 | 0.00 | 1.00 | 14.30 | 2.50 | 0.00 |
| 2 | 2023-01-01 00:55:08 | 2023-01-01 01:01:27 | 1 | 1.10 | 1 | N | 43 | 237 | 1 | 7.90 | 1.00 | 0.50 | 4.00 | 0.00 | 1.00 | 16.90 | 2.50 | 0.00 |
| 2 | 2023-01-01 00:25:04 | 2023-01-01 00:37:49 | 1 | 2.51 | 1 | N | 48 | 238 | 1 | 14.90 | 1.00 | 0.50 | 15.00 | 0.00 | 1.00 | 34.90 | 2.50 | 0.00 |

### 3.2 UNF Observation

The dataset stores all trip information in one wide
table. Vendor IDs, location IDs, rate codes and
payment types are repeated across different records.

The data has not yet been separated into related
tables. This structure will be used as the starting
point for the normalization process.
