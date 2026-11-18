# Tourist Transport and Trip Management System

## Student Information
- Name: Ishimwe Florence
- ID: 20251SEN040

## Project Description

This project is about developing a database system for Rwanda Explorer Travel Ltd, a proposed transport company that serves individuals and groups. The company uses cars, SUVs, vans and buses to transport customers to different destinations.

The system will help the company organize customer information, drivers, vehicles, bookings, destinations and payments in one database.

## Problem Statement

Many transport companies have difficulties managing customer bookings, drivers, vehicles, trip schedules and payments manually. This can lead to booking conflicts, delays and poor record keeping.

This project proposes a database system for Rwanda Explorer Travel Ltd to make transport operations easier to manage and organize.

## Objectives

### Main Objective

To develop a centralized database system for managing the transport operations of Rwanda Explorer Travel Ltd, including customers, drivers, vehicles, bookings, destinations and payments.

### Specific Objectives

1. To manage customer information by storing and organizing customer details in one database.
2. To manage drivers and vehicles by keeping their records and supporting proper assignments.
3. To manage bookings and destinations by recording trip details and reducing booking conflicts.
4. To manage payments by recording customer payments and tracking payment status.
5. To use SQL and PL/SQL to improve data management, accuracy and consistency.

## Data Source

The project uses the NYC Taxi and Limousine Commission (TLC) Trip Record Data, specifically the January 2023 Yellow Taxi dataset.

The dataset is used for studying trip information and carrying out preliminary data analysis. The original dataset contains 3,066,766 records. A sample of 1,000 records with 19 columns was used for analysis.

The dataset is a reference for transport information. It is not the actual customer, driver or vehicle data of Rwanda Explorer Travel Ltd. Company records will be entered separately.

**Dataset link:**  
https://www.nyc.gov/site/tlc/about/tlc-trip-record-data.page

## Innovation

The project plans to use **Oracle APEX** to build an interactive web interface connected to the Oracle database.

Company staff will use forms to enter and update customer, driver, vehicle, booking and payment information. They will also use reports to view bookings, vehicle assignments and payments.

PL/SQL will help check and manage database operations.

**Innovation option:** User Interface  
**Innovation tool:** Oracle APEX

## Planned Tables

The database will contain six main tables:

1. **CUSTOMER** – Stores customer information.
2. **DRIVER** – Stores driver information.
3. **VEHICLE** – Stores vehicle information and availability.
4. **DESTINATION** – Stores destination details.
5. **BOOKING** – Stores trip bookings, dates, assigned drivers, vehicles and booking status.
6. **PAYMENT** – Stores payment details linked to bookings.

## Planned PL/SQL Features

The project plans to use the following PL/SQL features:

- **Procedures:** To create and update bookings, assign drivers and vehicles, and record payments.
- **Functions:** To calculate booking totals and outstanding balances.
- **Cursors:** To display and process customer bookings and scheduled trips.
- **Triggers:** To validate booking operations and update related records when necessary.
- **Packages:** To group related booking and payment procedures and functions.
- **Exception Handling:** To handle errors such as invalid booking IDs, unavailable vehicles and invalid payment amounts.

## References

Al-Hawari, F., Al-Sammarraie, M., & Al-Khaffaf, H. (2020). Design, validation, and comparative analysis of a private bus location tracking information system. *Journal of Advanced Transportation*. https://doi.org/10.1155/2020/8895927

Distinctive Systems. (n.d.). *Coach Manager*. https://www.distinctive-systems.com/

Hartleb, P., Friedrich, M., & Richter, B. (2022). Vehicle scheduling for on-demand vehicle fleets in macroscopic travel demand models. *Transportation*. https://doi.org/10.1007/s11116-021-10205-4

National Institute of Statistics of Rwanda. (2024). *Rwanda Statistical Yearbook 2024*.

New York City Taxi and Limousine Commission. (2023). *TLC Trip Record Data: Yellow Taxi Trip Records (January 2023)*. https://www.nyc.gov/site/tlc/about/tlc-trip-record-data.page

Oracle. (n.d.). *Oracle Database SQL Language Reference: Constraints*. https://docs.oracle.com/en/database/




