
# TOURIST TRANSPORT AND TRIP MANAGEMENT SYSTEM

**Name:** Ishimwe Florence  
**ID:** 20251SEN040  
**Course Code:** INSY8311  
**Course Name:** Database Development with PL/SQL  
**Lecturer:** Eric Maniraguha

---

## 1. Problem Statement

Tourism and transport companies may face difficulties managing customer bookings, vehicle availability, driver assignments, destinations, and payments when these activities are handled manually or kept in separate records. This can lead to booking conflicts, delays in confirming trips, difficulty identifying available vehicles, and challenges retrieving accurate customer and payment information. Rwanda Explorer Travel Ltd is the proposed case company for addressing these challenges.

## 2. Proposed Solution

The project proposes a Tourist Transport and Trip Management System implemented using an Oracle relational database. Company staff will register customers, maintain driver and vehicle information, record destinations, create and manage bookings, assign available vehicles and drivers, and record payments. The database will organize related information and use constraints and PL/SQL program units to support accurate and efficient operations.

## 3. Data Source

The January 2023 New York City Taxi and Limousine Commission (NYC TLC) Yellow Taxi Trip Record dataset will be used for preliminary transport-data exploration and analysis. Rwanda Statistical Yearbook 2024 will provide contextual transport and tourism statistics. Academic studies on vehicle scheduling and transport tracking, together with Oracle Database documentation, will support the research and database design.

Company-specific customer, driver, vehicle, booking, destination, and payment records will be entered by authorized staff; the public taxi dataset will not be treated as the company's operational records.

## 4. Planned Tables

- **CUSTOMER** – stores customer details.
- **DRIVER** – stores driver details.
- **VEHICLE** – stores vehicle details and availability.
- **DESTINATION** – stores trip destination details.
- **BOOKING** – stores customer trip bookings, dates, assigned driver and vehicle, and booking status.
- **PAYMENT** – stores payment details linked to bookings.

## 5. Planned PL/SQL Features

The project plans to use:

- **Stored Procedures:** To manage bookings and record payments.
- **Functions:** To calculate payment totals.
- **Triggers:** To validate booking operations and help prevent conflicting vehicle assignments.
- **Cursors or Parameterized Queries:** To produce booking, vehicle, and payment reports.

Primary-key, foreign-key, NOT NULL, UNIQUE, and CHECK constraints will help maintain data integrity.

## 6. Innovation

The system will bring customer, trip, destination, vehicle, driver, and payment information together in one database. Its main value is the coordination of booking management with vehicle and driver assignment, supported by database validation to reduce scheduling conflicts and improve access to organized trip records.

## 7. References (APA)

Al-Hawari, F., Al-Sammarraie, M., & Al-Khaffaf, M. (2020). Design, validation, and comparative analysis of a private bus location tracking information system. *Journal of Advanced Transportation*. https://doi.org/10.1155/2020/8895927

Hartleb, J., Friedrich, M., & Richter, B. (2022). Vehicle scheduling for on-demand vehicle fleets in macroscopic travel demand models. *Transportation*. https://doi.org/10.1007/s11116-021-10205-4

National Institute of Statistics of Rwanda. (2024). *Rwanda statistical yearbook 2024*.

New York City Taxi and Limousine Commission. (2023). *TLC trip record data: Yellow taxi trip records (January 2023).*

Oracle. (n.d.). *Oracle Database SQL language reference: Constraints.*

