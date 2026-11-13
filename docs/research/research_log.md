
# Research Log
## Project: Tourist Transport and Trip Management System

| # | Source (APA) | Type | Link | Key Finding | Gap It Shows |
|---|---|---|---|---|---|
| 1 | Zheng, W., Zhuang, X., Liao, Z., Li, M., & Lin, Z. (2021). All roads lead to the places of your interest: An on-demand, ride-sharing visitor transport service. *International Journal of Tourism Research, 23*(5), 871–880. | Research Paper | https://doi.org/10.1002/jtr.2449 | The study proposes an intelligent visitor transport service that improves vehicle scheduling, reduces visitor waiting time, and improves energy efficiency. | The study focuses on visitor transport scheduling rather than integrated management of customers, drivers, vehicles, bookings, and payments. |
| 2 | Hong, Y., Xu, M., Jin, Y., & Wang, S. (2025). Data-driven modular vehicle scheduling in scenic areas. *Applied Sciences, 15*(1), Article 205. | Research Paper | https://doi.org/10.3390/app15010205 | The study proposes a data-driven vehicle scheduling method to improve vehicle utilization and reduce operating costs in tourist areas. | The study focuses on vehicle scheduling rather than complete transport company management, including customer bookings and payment tracking. |
| 3 | Rwanda Development Board. (2025). *Annual Report 2024*. https://rdb.rw/ar/Annual-report-2024.pdf | Report/Statistic | Rwanda generated USD 647 million in tourism revenue and welcomed 1.36 million visitors in 2024. Tourism revenue increased by 4.3% compared with 2023. | The report demonstrates the importance and growth of Rwanda's tourism sector, supporting the need for efficient tourism transport management systems. |
| 4 | Permalink Business Ltd. (n.d.). *Tour Operator System (TOS).* https://permalinkbusiness.com/products/tour-operator-system/ | Existing System | TOS provides booking management, itinerary creation, vehicle and driver allocation, payment tracking, invoicing, and financial reporting for tour operators. | Our project will develop a smaller Oracle-based system focused on six main tables, using PL/SQL to enforce booking, vehicle availability, driver assignment, and payment rules. |
| 5 | New York City Taxi and Limousine Commission. (n.d.). *TLC Trip Record Data*. https://www.nyc.gov/site/tlc/about/tlc-trip-record-data.page | Dataset | The dataset contains taxi trip records, including pickup and drop-off dates, times, locations, trip distances, passenger counts, fares, and payment types. | The dataset does not contain individual customer or driver identities and is not specific to tourist transport in Rwanda. It can provide a reference for designing trip and payment records. |
| 6 | Oracle. (n.d.). *Oracle Database PL/SQL Language Reference*. https://docs.oracle.com/en/database/oracle/oracle-database/23/lnpls/ | Technical Source | The documentation explains PL/SQL programming concepts, including procedures, functions, cursors, packages, triggers, variables, and exception handling in Oracle Database. | Provides the technical knowledge needed to implement database operations, automate business rules, handle errors, and maintain the Tourist Transport and Trip Management System. |

## 1. Research Paper 1

### Paper Information

- **Title:** Vehicle Scheduling for On-Demand Vehicle Fleets in Macroscopic Travel Demand Models
- **Authors:** Johann Hartleb, Markus Friedrich, and Emely Richter
- **Year:** 2022 (published online in 2021)
- **Journal:** Transportation
- **Publisher:** Springer Nature
- **DOI:** https://doi.org/10.1007/s11116-021-10205-4

### Research Problem

Transport operators need to organize vehicle schedules and determine how many vehicles are required to serve customer travel demands efficiently.

### Purpose of the Study

The study aimed to develop an algorithm that helps transport planners create vehicle schedules and estimate the number of vehicles needed to serve different travel demands.

### Method Used

The researchers developed a vehicle scheduling algorithm and tested it through two case studies involving regional carsharing in Germany and an electric scooter service at a university.

### Main Findings

The study showed that vehicle scheduling and relocation can help estimate fleet requirements and improve the use of available vehicles.

### Relevance to Our Research

This paper is relevant to our Tourist Transport and Trip Management System because it explains the importance of vehicle scheduling and fleet management.

It supports the need to manage vehicle availability and organize trips efficiently when assigning vehicles to customer bookings.

### Reference

Hartleb, J., Friedrich, M., & Richter, E. (2022). Vehicle scheduling for on-demand vehicle fleets in macroscopic travel demand models. *Transportation, 49*, 1133–1155. https://doi.org/10.1007/s11116-021-10205-4

### Source Link

https://link.springer.com/article/10.1007/s11116-021-10205-4


## 2. Research Paper 2

### Paper Information

- **Title:** Design, Validation, and Comparative Analysis of a Private Bus Location Tracking Information System
- **Authors:** Feras Al-Hawari, Mohammed Al-Sammarraie, and Taha Al-Khaffaf
- **Year:** 2020
- **Journal:** Journal of Advanced Transportation
- **Publisher:** Wiley
- **DOI:** https://doi.org/10.1155/2020/8895927

### Research Problem

Managing bus transportation services involves organizing buses, drivers, routes, schedules and trips. Without an organized computerized system, these activities can be difficult to coordinate.

### Purpose of the Study

The study aimed to design and develop a web-based information system to manage bus transportation services and allow passengers to track bus trips.

### Method Used

The researchers designed and developed a web-based system. They worked on the user interface, database design, system architecture and system testing.

### Main Findings

The developed system supported bus management, driver assignment, route scheduling and trip monitoring.

The evaluation showed that the system was helpful, easy to use, fast and responsive.

### Relevance to Our Research

This paper is relevant to our Tourist Transport and Trip Management System because it demonstrates how technology and database systems can help organize transport operations.

It supports the need to manage drivers, vehicles and schedules, which are important parts of our proposed system.

### Reference

Al-Hawari, F., Al-Sammarraie, M., & Al-Khaffaf, T. (2020). Design, validation, and comparative analysis of a private bus location tracking information system. *Journal of Advanced Transportation, 2020*, Article 8895927. https://doi.org/10.1155/2020/8895927

### Source Link

https://onlinelibrary.wiley.com/doi/10.1155/2020/8895927

## 3. Report or Statistic Research

### Report Information

- **Organization:** National Institute of Statistics of Rwanda (NISR)
- **Report Title:** Rwanda Statistical Yearbook 2024
- **Year:** 2024
- **Country:** Rwanda
- **Source Type:** Official government statistical report
- **Topic:** Road Transport and Tourism
- **Source Link:** https://www.statistics.gov.rw/sites/default/files/documents/2025-02/Statistical_Year_Book_2024.pdf

### Purpose of the Report

The report provides official statistical information about different sectors in Rwanda, including road transport services and tourism.

### Important Statistics

According to the report:

- Rwanda had 47 licensed public transport companies and cooperatives in 2023.
- There were 64 licensed rental car hire companies and cooperatives in 2023.
- Rwanda recorded 135,869 visits to its three major national parks in 2023.

### Relevance to Our Research

This report is relevant to our Tourist Transport and Trip Management System because it provides information about Rwanda's transport and tourism sectors.

The statistics show that transport services and tourism activities are present in Rwanda. This supports the importance of developing organized systems for managing customers, drivers, vehicles, destinations, bookings and payments.

### Reference

National Institute of Statistics of Rwanda. (2024). *Rwanda Statistical Yearbook 2024*. https://www.statistics.gov.rw/sites/default/files/documents/2025-02/Statistical_Year_Book_2024.pdf


## 4. Existing System Research

### System Information

- **System Name:** Coach Manager
- **Developer:** Distinctive Systems
- **Country:** United Kingdom
- **System Type:** Transport Management Software
- **Target Users:** Coach, minibus, chauffeur and community transport operators
- **Official Website:** https://distinctive-systems.com/products/coach-manager/

### Description of the Existing System

Coach Manager is a transport management software developed by Distinctive Systems. It helps transport companies manage bookings, vehicles, drivers, schedules, invoices and payments.

The system is designed to support the daily operations of transport businesses and organize their transport services.

### Main Features

- Booking management: Records customer bookings and transport requirements.
- Vehicle management: Helps allocate vehicles to bookings.
- Driver management: Organizes driver assignments.
- Scheduling: Helps plan vehicle and driver schedules.
- Invoicing: Generates invoices for bookings.
- Payment management: Records and allocates customer payments.
- Reporting: Provides financial and operational reports.

### Advantages of the Existing System

- Helps organize transport bookings.
- Makes it easier to allocate drivers and vehicles.
- Supports scheduling and trip coordination.
- Helps manage invoices and payments.
- Provides reports for transport operations.

### Limitations

- It is a commercial software product that requires a paid subscription.
- It includes many advanced features beyond the requirements of our proposed academic project.
- Its suitability for the specific needs of a Rwandan tourism transport company has not been established.

### Relevance to Our Research

Coach Manager is relevant to our Tourist Transport and Trip Management System because it demonstrates how software can organize transport bookings, vehicle allocation, driver assignments and payments.

Studying this existing system helps us identify useful features that can guide the development of our proposed system.

Our proposed system will focus on six main database tables: CUSTOMER, DRIVER, VEHICLE, DESTINATION, BOOKING and PAYMENT.

### Reference

Distinctive Systems. (n.d.). *Coach Manager*. https://distinctive-systems.com/products/coach-manager/


## 5.Dataset Research

### NYC Yellow Taxi Trip Data (January 2023)

- **Source:** NYC Taxi and Limousine Commission (TLC).
- **Dataset:** yellow_tripdata_2023-01.parquet
- **Format:** Parquet
- **Original records:** 3,066,766
- **Columns:** 19
- **Sample records:** 1,000
- **Sample format:** CSV

### Information Available

The dataset contains:
- Vendor identification
- Pickup and drop-off dates and times
- Passenger count
- Trip distance
- Pickup and drop-off location IDs
- Payment type
- Fare and additional charges

### Initial Findings

From the 1,000 sampled records:

- Average passenger count: 1.517
- Average trip distance: 2.96 miles
- Average fare amount: $16.95
- Average total amount: $25.19
- Maximum trip distance: 30.15 miles

### Limitations

- The dataset represents New York City taxi trips.
- It does not identify individual drivers.
- It does not contain vehicle registration numbers.
- Some records contain unusual values that require further investigation.

### Relevance to the Research

The dataset can help us understand transportation patterns, trip distances, passenger numbers and trip schedules. However, it cannot directly provide all the information required for a fleet management system.

### Data Quality Check

A missing-value check was performed on the
1,000 sampled records.

Results:
- Total sampled records: 1,000
- Total columns checked: 19
- Missing values: 0

All 19 columns contained complete values in the
sample. Therefore, no missing values were detected.

#### Duplicate Records Check

A duplicate-record check was performed on the
1,000 sampled records.

Results:
- Total sampled records: 1,000
- Duplicate records: 0

No duplicate records were detected in the sample.

#### Unusual Values Check

The sample was also checked for unusual values.

Results:
- Negative fare amounts: 6 records.
- Zero trip distances: 8 records.
- Zero passenger counts: 13 records.

These values may indicate unusual trips, adjustments, or incomplete records. Further investigation is required before deciding whether they should be removed during data cleaning.

## 6. Technical Source Research

### Source Information

- **Organization:** Oracle
- **Document Title:** Oracle Database SQL Language Reference – Constraints
- **Year:** Oracle Database 21c documentation
- **Source Type:** Official technical documentation
- **Topic:** Database integrity constraints
- **Source Link:** https://docs.oracle.com/en/database/oracle/oracle-database/21/sqlrf/constraint.html

### Purpose of the Source

This documentation explains how database constraints are used to maintain data accuracy, consistency and relationships between database tables.

### Important Technical Concepts

- **Primary Key:** Uniquely identifies each record in a table.
- **Foreign Key:** Establishes a relationship between two tables.
- **NOT NULL:** Prevents a column from containing NULL values.
- **UNIQUE:** Ensures that values in a column or combination of columns are not duplicated.
- **CHECK:** Ensures that stored values satisfy specified conditions.

### Relevance to Our Research

This technical source is relevant to our Tourist Transport and Trip Management System because the proposed database contains six related tables: CUSTOMER, DRIVER, VEHICLE, DESTINATION, BOOKING and PAYMENT.

The documentation will help guide the design of primary keys, foreign keys and other constraints to maintain accurate and consistent database records.

### Reference

Oracle. (n.d.). *Oracle Database SQL Language Reference: Constraints*. https://docs.oracle.com/en/database/oracle/oracle-database/21/sqlrf/constraint.html

No records were deleted during this initial analysis.

