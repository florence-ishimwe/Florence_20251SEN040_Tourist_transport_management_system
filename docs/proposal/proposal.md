
# TOURIST TRANSPORT AND TRIP MANAGEMENT SYSTEM

**Name:** Ishimwe Florence  
**ID:** 20251SEN040  
**Course Code:** INSY8311  
**Course Name:** Database Development with PL/SQL  
**Lecturer:** Eric Maniraguha

---

## 1. Problem Statement

Many transport companies have difficulties managing customer bookings, drivers, vehicles, trip schedules and payments manually. This can lead to booking conflicts, delays and poor record keeping. Rwanda Explorer Travel Ltd is the proposed transport company for this project.

## 2. Proposed Solution

The project proposes an Oracle database system to help Rwanda Explorer Travel Ltd manage its transport operations. Company staff will register customers, manage driver and vehicle information, record destinations, create bookings, assign drivers and vehicles, and record payments.

The system will use SQL and PL/SQL to organize information, check data and reduce booking conflicts.

## 3. Data Source

The project will use the January 2023 New York City Taxi and Limousine Commission (NYC TLC) Yellow Taxi Trip Record dataset for preliminary transport-data analysis. The original dataset contains 3,066,766 records, and a sample of 1,000 records was used for analysis.

The Rwanda Statistical Yearbook 2024 will provide information about Rwanda's transport and tourism sectors. Research papers and Oracle documentation will also support the project.

The NYC TLC dataset is only a reference for transport information. It does not contain the actual company records. Customer, driver, vehicle, booking, destination and payment records for the proposed system will be entered separately.

Dataset link: https://www.nyc.gov/site/tlc/about/tlc-trip-record-data.page

## 4. Planned Tables

The system will have six main tables:

- **CUSTOMER:** Stores customer information.
- **DRIVER:** Stores driver information.
- **VEHICLE:** Stores vehicle details and availability.
- **DESTINATION:** Stores destination details.
- **BOOKING:** Stores trip details, dates, assigned drivers and vehicles, and booking status.
- **PAYMENT:** Stores payment details linked to bookings.

## 5. Planned PL/SQL Features

The project plans to use:

- **Procedures:** To create and update bookings, assign drivers and vehicles, and record payments.
- **Functions:** To calculate booking totals and outstanding balances.
- **Cursors:** To process and display customer bookings and scheduled trips.
- **Triggers:** To validate booking operations and update related records when necessary.
- **Packages:** To group related booking and payment procedures and functions.
- **Exception Handling:** To handle errors such as invalid booking IDs, unavailable vehicles and invalid payment amounts.

Primary keys, foreign keys, NOT NULL, UNIQUE and CHECK constraints will help maintain correct and consistent data.

## 6. Innovation

The project will use **Oracle APEX** as its innovation tool. It will provide an interactive web interface connected to the Oracle database.

Company staff will use forms to enter and update information. They will also use reports to view bookings, driver and vehicle assignments, and payments. The application will use the database and PL/SQL rules to manage operations.

**Innovation option:** User Interface  
**Innovation tool:** Oracle APEX

## 7. References (APA)

Al-Hawari, F., Al-Sammarraie, M., & Al-Khaffaf, H. (2020). Design, validation, and comparative analysis of a private bus location tracking information system. *Journal of Advanced Transportation*. https://doi.org/10.1155/2020/8895927

Distinctive Systems. (n.d.). *Coach Manager*. https://www.distinctive-systems.com/

Hartleb, P., Friedrich, M., & Richter, B. (2022). Vehicle scheduling for on-demand vehicle fleets in macroscopic travel demand models. *Transportation*. https://doi.org/10.1007/s11116-021-10205-4

National Institute of Statistics of Rwanda. (2024). *Rwanda Statistical Yearbook 2024*.

New York City Taxi and Limousine Commission. (2023). *TLC Trip Record Data: Yellow Taxi Trip Records (January 2023)*. https://www.nyc.gov/site/tlc/about/tlc-trip-record-data.page

Oracle. (n.d.). *Oracle Database SQL Language Reference: Constraints*. https://docs.oracle.com/en/database/







