
# Tourist Transport and Trip Management System

## Slide 1: Title

**Tourist Transport and Trip Management System**

- Name: Ishimwe Florence
- Student ID: 20251SEN040
- Course: Database Development with PL/SQL
- Instructor: Eric Maniraguha
- GitHub: https://github.com/florence-ishimwe/Florence_20251SEN040_Tourist_transport_management_system

---

## Slide 2: Background and Problem

### Project context

Rwanda Explorer Travel Ltd is a proposed transport company scenario serving individual customers and groups. It manages trips to different destinations using cars, SUVs and passenger vans.

### Who is affected?

- Customers
- Booking staff
- Drivers
- Company managers

### Problem statement

Many transport companies face challenges managing customer bookings, vehicle availability, driver assignments, trip schedules and payments using manual methods. This can lead to booking conflicts, assigning multiple trips to the same driver or vehicle, scheduling difficulties, delays and poor record management.

---

## Slide 3: Motivation

### Why this project was chosen

This project was chosen because transport management plays an important role in serving individuals and groups who need reliable transportation. Managing customers, drivers, vehicles, bookings and payments efficiently is essential for smooth daily operations.

We are motivated to develop a database system that can organize transport information, reduce manual work and make it easier for company staff to coordinate trips.

### Project focus

The project focuses on developing a centralized database system for managing customer information, driver assignments, vehicle availability, trip bookings, destinations and payments.

---

## Slide 4: Project Objectives

### Main objective

To develop a centralized database system for managing the transport operations of Rwanda Explorer Travel Ltd, including customers, drivers, vehicles, bookings, destinations and payments.

### Specific objectives

1. To manage customer information by storing and organizing customer details in a centralized database.
2. To manage drivers and vehicles by maintaining their records and supporting appropriate driver and vehicle assignments.
3. To manage bookings and destinations by recording trip details, scheduling transportation and reducing booking conflicts.
4. To manage payments by recording customer payments and tracking booking payment status.
5. To apply SQL and PL/SQL features to improve data management, accuracy and consistency.

---

## Slide 5: Research — Existing Solutions and Gaps

| Research source | What it contributes | Gap / relevance to our project |
|---|---|---|
| Hartleb et al. (2022) | Studies vehicle scheduling for on-demand transport fleets. | Focuses on fleet scheduling models rather than a small company's integrated booking database. |
| Al-Hawari et al. (2020) | Examines a bus location tracking information system. | Focuses on bus tracking, while our project focuses on bookings, driver and vehicle assignments, and payments. |
| Distinctive Systems – Coach Manager | Provides commercial coach booking, scheduling and administrative features. | A commercial solution; our project will develop a smaller, learning-focused database system for Rwanda Explorer Travel Ltd. |
| NISR Rwanda (2024) | Provides statistical information about Rwanda's transport and tourism sectors. | Provides background evidence rather than operational booking records for our proposed system. |

**Research gap:** There is an opportunity to develop a focused database system that integrates customer, driver, vehicle, destination, booking and payment management for a transport company.

---

## Slide 6: Data Source

### Dataset

**New York City Taxi and Limousine Commission (TLC)**

January 2023 Yellow Taxi Trip Records.

### Dataset size and sample

The January 2023 file contained 3,066,766 original records. A 1,000-record sample with 19 columns was used for preliminary analysis.

### Example fields

| Field | Example meaning |
|---|---|
| `tpep_pickup_datetime` | Date and time trip began |
| `tpep_dropoff_datetime` | Date and time trip ended |
| `passenger_count` | Number of passengers |
| `trip_distance` | Trip distance in miles |
| `fare_amount` / `total_amount` | Fare and total charged |

### Sample Dataset Records

| Pickup datetime | Drop-off datetime | Passengers | Distance (miles) |
|---|---|---|---|
| 1/1/2023 0:32 | 1/1/2023 0:40 | 1 | 0.97 |
| 1/1/2023 0:55 | 1/1/2023 1:01 | 1 | 1.10 |
| 1/1/2023 0:25 | 1/1/2023 0:37 | 1 | 2.51 |

Source: https://www.nyc.gov/site/tlc/about/tlc-trip-record-data.page

---

## Slide 7: Proposed Solution and Innovation

### Proposed database solution

An Oracle relational database will centralize customer details, bookings, driver assignments, vehicle information, destinations and payments.

### Planned innovation: User interface

Oracle APEX is the planned tool for building an interactive web interface connected to the Oracle database.

### How it will work

- Staff use APEX forms to enter and update records.
- Reports allow staff to view bookings, vehicle assignments and payments.
- APEX pages call PL/SQL procedures where appropriate; database rules remain in PL/SQL.
- The working application will be demonstrated live during the final presentation.

---

## Slide 8: Planned Database Design

The system will use six main tables:

1. CUSTOMER
2. DRIVER
3. VEHICLE
4. DESTINATION
5. BOOKING
6. PAYMENT

These tables will be connected through relationships to organize customer bookings, driver and vehicle assignments, destinations and payments.

---

## Slide 9: PL/SQL Approach

| PL/SQL feature | Planned use in this system |
|---|---|
| **Procedures** | Create or update bookings; record a payment; assign a driver and vehicle. |
| **Functions** | Calculate the booking total or return the outstanding balance. |
| **Cursors** | Process and display a customer's bookings or a list of scheduled trips. |
| **Triggers** | Validate changes and automatically update a related status when a payment is recorded. |
| **Packages** | Group related booking and payment procedures/functions into reusable modules. |
| **Exception handling** | Handle invalid booking IDs, unavailable vehicles and invalid payment amounts. |

---

## Slide 10: Expected Results

By the end of the project, we expect to demonstrate:

- An Oracle database containing the six planned tables and their relationships.
- Working SQL constraints and PL/SQL program units.
- A booking workflow that records a customer, destination, assigned vehicle and driver.
- Payment recording and retrieval of booking/payment information.
- An Oracle APEX interface connected to the real database, with forms and reports.
- Test cases showing valid operations and handling of invalid data.

### Demonstration goal

Show a staff member creating a booking, viewing it in a report and recording its payment.

---

## Slide 11: Future Improvements and Limitations

### Limitations

- The TLC dataset comes from New York taxi trips, not a Rwandan tourism company.
- It is useful as a transport-data reference, but it does not supply our actual customer, driver or vehicle records.
- The first version will focus on core booking and payment management rather than live GPS tracking.

### Future improvements

- Add GPS tracking and live vehicle location.
- Add customer notifications by SMS or email.
- Integrate online payment services.
- Develop a mobile application.
- Add analytics for demand, vehicle utilization and revenue trends.

---

## Slide 12: References (APA)

Al-Hawari, F., Al-Sammarraie, M., & Al-Khaffaf, H. (2020). Design, validation, and comparative analysis of a private bus location tracking information system. *Journal of Advanced Transportation*. https://doi.org/10.1155/2020/8895927

Distinctive Systems. (n.d.). *Coach Manager*. https://www.distinctive-systems.com/

Hartleb, P., Friedrich, M., & Richter, B. (2022). Vehicle scheduling for on-demand vehicle fleets in macroscopic travel demand models. *Transportation*. https://doi.org/10.1007/s11116-021-10205-4

National Institute of Statistics of Rwanda. (2024). *Rwanda statistical yearbook 2024*.

New York City Taxi and Limousine Commission. (2023). *TLC trip record data*. https://www.nyc.gov/site/tlc/about/tlc-trip-record-data.page

Oracle. (n.d.). *Oracle Database SQL language reference: Constraints*. https://docs.oracle.com/en/database/

---

## Thank You

