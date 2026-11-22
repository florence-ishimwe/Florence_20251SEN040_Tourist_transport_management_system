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

## 4. First Normal Form (1NF)

The dataset satisfies the main requirements of
First Normal Form because each column contains
individual values and each row represents one
taxi trip.

There are no repeating groups or multiple values
stored in a single cell.

A new column called TripID is introduced to
uniquely identify each trip record. TripID will
serve as the primary key.

### 4.1 Sample Records in 1NF

| TripID | VendorID | Passenger Count | Trip Distance | PULocationID | DOLocationID | Payment Type |
|---|---:|---:|---:|---:|---:|---:|
| 1 | 2 | 1 | 0.97 | 161 | 141 | 2 |
| 2 | 2 | 1 | 1.10 | 43 | 237 | 1 |
| 3 | 2 | 1 | 2.51 | 48 | 238 | 1 |

The sample records above show the new TripID
column. The other original columns remain in the
TRIP table.

### 4.2 Changes Made

- Added TripID as a unique identifier.
- Kept each value in its own column.
- Maintained one record per taxi trip.
- No repeating groups were identified.

### 4.3 Dependency Removed

No repeating group or partial dependency was
removed at this stage. The main change was
introducing a unique primary key for each trip.

## 5. Second Normal Form (2NF)

The dataset already satisfies First Normal Form
because each column contains individual values and
each record represents one taxi trip.

To achieve Second Normal Form, we examined the
functional dependencies between the primary key
and the non-key attributes.

The TRIP table uses TripID as its primary key.
Since TripID is a single-column primary key, there
are no partial dependencies.

All non-key attributes depend on the complete
TripID.

### 5.1 Sample Records in 2NF

| TripID | VendorID | Passenger Count | Trip Distance | PULocationID | DOLocationID | Payment Type |
|---|---:|---:|---:|---:|---:|---:|
| 1 | 2 | 1 | 0.97 | 161 | 141 | 2 |
| 2 | 2 | 1 | 1.10 | 43 | 237 | 1 |
| 3 | 2 | 1 | 2.51 | 48 | 238 | 1 |

### 5.2 Changes Made

- Maintained TripID as the primary key.
- Kept all original trip attributes.
- Confirmed that non-key attributes depend on
  the complete primary key.
- No table decomposition was required at this stage.

### 5.3 Dependency Removed

No partial dependency was identified or removed
because the primary key contains only one column.

## 6. Third Normal Form (3NF)

The dataset was examined to identify transitive
dependencies.

The proposed design separates repeated reference
information from the main trip records.

The final logical design will contain five related
tables:

1. VENDOR
2. LOCATION
3. RATE_CODE
4. PAYMENT_TYPE
5. TRIP

### 6.1 Proposed 3NF Tables

**VENDOR**
- VendorID (Primary Key)
- VendorName

**LOCATION**
- LocationID (Primary Key)
- Borough
- Zone
- ServiceZone

**RATE_CODE**
- RatecodeID (Primary Key)
- RateDescription

**PAYMENT_TYPE**
- PaymentTypeID (Primary Key)
- PaymentDescription

**TRIP**
- TripID (Primary Key)
- VendorID (Foreign Key)
- PickupDateTime
- DropoffDateTime
- PassengerCount
- TripDistance
- RatecodeID (Foreign Key)
- StoreAndFwdFlag
- PickupLocationID (Foreign Key)
- DropoffLocationID (Foreign Key)
- PaymentTypeID (Foreign Key)
- FareAmount
- Extra
- MTATax
- TipAmount
- TollsAmount
- ImprovementSurcharge
- TotalAmount
- CongestionSurcharge
- AirportFee

### 6.2 Sample Trip Records in 3NF

The following records are from the original
1,000-record dataset.

| TripID | VendorID | PickupLocationID | DropoffLocationID | RatecodeID | PaymentTypeID | TripDistance | TotalAmount |
|---|---:|---:|---:|---:|---:|---:|---:|
| 1 | 2 | 161 | 141 | 1 | 2 | 0.97 | 14.30 |
| 2 | 2 | 43 | 237 | 1 | 1 | 1.10 | 16.90 |
| 3 | 2 | 48 | 238 | 1 | 1 | 2.51 | 34.90 |

The descriptive information for the lookup tables
will be obtained from official TLC reference data.

### 6.3 Changes Made

- Separated vendor information into VENDOR.
- Separated location information into LOCATION.
- Separated rate descriptions into RATE_CODE.
- Separated payment descriptions into PAYMENT_TYPE.
- Kept individual trip information in TRIP.
- Used foreign keys to connect the tables.

### 6.4 Dependency Removed

The proposed separation prevents descriptive
reference information from being repeated in
multiple trip records.

The lookup descriptions and their functional
dependencies must be verified using official
reference data before the final design is approved.

## 7. Mapping Raw Fields to 3NF Tables

The original dataset contains 19 columns.
Each column has been assigned to a target table
in the proposed 3NF database design.

| Raw Field | Target Table | Target Column | Explanation |
|---|---|---|---|
| VendorID | VENDOR / TRIP | VendorID | Identifies the taxi service vendor |
| tpep_pickup_datetime | TRIP | PickupDateTime | Records the pickup date and time |
| tpep_dropoff_datetime | TRIP | DropoffDateTime | Records the drop-off date and time |
| passenger_count | TRIP | PassengerCount | Number of passengers |
| trip_distance | TRIP | TripDistance | Distance travelled |
| RatecodeID | RATE_CODE / TRIP | RatecodeID | Identifies the trip rate code |
| store_and_fwd_flag | TRIP | StoreAndFwdFlag | Indicates whether the trip record was stored and forwarded |
| PULocationID | LOCATION / TRIP | PickupLocationID | Identifies the pickup location |
| DOLocationID | LOCATION / TRIP | DropoffLocationID | Identifies the drop-off location |
| payment_type | PAYMENT_TYPE / TRIP | PaymentTypeID | Identifies the payment method |
| fare_amount | TRIP | FareAmount | Base trip fare |
| extra | TRIP | Extra | Additional charges |
| mta_tax | TRIP | MTATax | MTA tax amount |
| tip_amount | TRIP | TipAmount | Tip amount |
| tolls_amount | TRIP | TollsAmount | Toll charges |
| improvement_surcharge | TRIP | ImprovementSurcharge | Improvement surcharge |
| total_amount | TRIP | TotalAmount | Total trip charge |
| congestion_surcharge | TRIP | CongestionSurcharge | Congestion surcharge |
| airport_fee | TRIP | AirportFee | Airport fee |

A new TripID column will be introduced as the
primary key of the TRIP table. It does not come
from the original dataset.

## 8. Type Conversions and Cleaning Checklist

The following conversions and checks will be
considered during database implementation.

### 8.1 Type Conversions

| Raw Field | Required Data Representation |
|---|---|
| tpep_pickup_datetime | DATE and time |
| tpep_dropoff_datetime | DATE and time |
| passenger_count | NUMBER |
| trip_distance | NUMBER |
| fare_amount | NUMBER |
| extra | NUMBER |
| mta_tax | NUMBER |
| tip_amount | NUMBER |
| tolls_amount | NUMBER |
| improvement_surcharge | NUMBER |
| total_amount | NUMBER |
| congestion_surcharge | NUMBER |
| airport_fee | NUMBER |
| store_and_fwd_flag | Text |
| VendorID | Numeric identifier |
| RatecodeID | Numeric identifier |
| PULocationID | Numeric identifier |
| DOLocationID | Numeric identifier |
| payment_type | Numeric identifier |

### 8.2 Cleaning Checklist

The following items will be considered during
the data cleaning stage:

- Check records with negative fare amounts.
- Investigate records with zero trip distances.
- Investigate records with zero passenger counts.
- Check date and time values for consistency.
- Verify that vendor IDs exist in the VENDOR table.
- Verify that location IDs exist in the LOCATION table.
- Verify rate code and payment type identifiers.
- Check that numeric columns contain valid numbers.

Data cleaning will be performed during the
implementation phase. The original raw dataset
will remain unchanged.
