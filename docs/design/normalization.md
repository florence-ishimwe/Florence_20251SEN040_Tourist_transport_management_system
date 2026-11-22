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

