
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
#### Dataset Analysis and Findings

A sample of 1,000 records was extracted from the original
NYC Yellow Taxi Trip Data for January 2023.

The descriptive statistics showed:

- Average passenger count: 1.517
- Average trip distance: 2.96 miles
- Average fare amount: $16.95
- Average total amount: $25.19
- Maximum trip distance: 30.15 miles

The dataset contains useful information about trip
timing, passenger numbers, travel distances, pickup
and drop-off locations, and payment information.

Some records contain unusual values, such as zero
trip distances and negative fare amounts. These
require further investigation during data cleaning.

#### Limitations

- The dataset represents New York City taxi trips.
- It does not identify individual drivers.
- It does not provide vehicle registration numbers.
- It cannot directly represent Rwanda's transport system.
