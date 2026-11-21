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

## Phase I – Business Process Modeling

## Overview
This phase presents the business process model i  for the **trip scheduling and booking management system** process of the Tourist Transport and Trip Management System (Rwanda Explorer Travel Ltd). The process shows how a customer's trip request is checked, scheduled, paid for, confirmed and communicated to everyone involved.

## Business Process Description
A customer requests a trip. The booking officer collects the trip details (destination, date, number of passengers, trip type, pickup location) and checks whether a suitable **vehicle** and **driver** are available. If both are available, the system assigns them to the trip and records the booking as *Pending*. The customer then pays a deposit, the system confirms the booking, and a notification is sent to both the **customer** and the **driver**.

If a vehicle or a driver is not available, the customer is offered a new date or can cancel the booking. When a new date is chosen, the process starts again from the trip request.

## Actors (Swimlanes)
| Lane | Responsibility |
|------|----------------|
| Customer | Requests the trip, chooses a new date or cancels, pays the deposit, receives the confirmation |
| Booking officer | Collects trip details, checks vehicle and driver availability |
| System (Oracle DB) | Assigns driver and vehicle, records the booking, confirms it and sends notifications |
| Driver | Receives the trip details |

## Process Steps
1. The customer requests a trip.
2. The booking officer collects the trip details.
3. The booking officer checks vehicle availability.
4. The booking officer checks driver availability.
5. If a vehicle or driver is not available, the customer picks a new date or cancels.
6. The system assigns the driver and vehicle and records the booking as *Pending*.
7. The customer pays the deposit.
8. The system confirms the booking.
9. The system notifies the customer and the driver.
10. The customer receives the booking confirmation and the driver receives the trip details.

## Business Rules
- A vehicle or driver cannot be booked for two overlapping trips.
- The vehicle must have enough seats for the number of passengers.
- The driver must be active, not on leave, and licensed for the vehicle type.
- A booking is confirmed only after the deposit is paid.

## Modeling Tool
- **Tool:** [draw.io](https://www.drawio.com/) (diagrams.net)
- **Notation:** BPMN-style swimlane diagram (one pool with four lanes)

## Diagram
**Published diagram link:** [View the diagram]((https://viewer.diagrams.net/?tags=%7B%7D&lightbox=1&highlight=0000ff&edit=_blank&layers=1&nav=1&dark=auto#R%3Cmxfile%3E%3Cdiagram%20name%3D%22Page-1%22%20id%3D%222rDpGGewbzUh5HtBnUZ2%22%3E5Vxbk9o2FP41zLQPydiWL%2FC4sGmaJml3QqdNnjpaW4CywqK2WKC%2FvhKWML5gjNfyuu7usqCji%2B3vnO%2Fo6MYIzNb79xHcrD7TAJGRZQT7EbgfWfzHNfibkBwSiWlOJolkGeFAylLBHP%2BDpFBWXG5xgOJMQUYpYXiTFfo0DJHPMjIYRXSXLbagJHvVDVyigmDuQ1KU%2FokDtkqkY8tL5T8jvFypK5uufL41VIXlk8QrGNDdmQi8G4FZRClLPq33M0QEegqXpN5PF3JPNxahkNWpsPyIPu7nG%2BOv9x%2FMKbB%2B%2BT6bOm%2FsYiuy4ZgdFAbxDq8JDHlq6q8wCT7BA92K0jGD%2FpNKTSMUc%2FU9qKbMnOgzFFZhcCmvFjGpaksIVmxNZI0NxSE76syZ8j%2F%2BSDPxMuW7MXL4Hc1EzlvLqcisyvMuZ5qXq4lUcs1LmVV5XnmmWdWqWdGqWdWqeoKLqF3KrMrzLmeaFdUmY5P%2FHu%2FWsGwwORWRxfgfmCYm9wzJVprcyHIJO5pKRMMlTy1F6vcIb3i5ub9CwZZgkWHAMOD%2FP8OQM3EtLE%2FW5ETIVpbXQBFD%2BzNLl2R5j%2BgasejAi6wyfHacpOIuZb%2FjSEorNyeTh6zrgtL1LE9Np%2BzkHyRBbyCrUyRrFanLGVxFvoIaZtuY8ZuPGmIHitiZ4yxYli6wVMMoKDj4K%2FDJm47pNvJRRTlh1TmcxcXmMkkjtqJLGkLyLpVOI7oNAxRIT5iW%2BUTpRmrhO2LsIDUEt4xmdRSgBdwS9gk%2BIjLl7nd5bHFGCY14iaQ7mxKR%2BwCDQHBEXMoy7JN%2BuQEsURUA5qSEj2XajhCBDD9n8W1dkwrn2oo70wchPFAQiOxWmKH5Bh41uuPBShZV3jlv0Icw5sGGlMB4k8QTC7wX%2BiqSYy6Y1IgZyn%2Bc%2B5SsS3GtDEuANmwnjbFNLdm8jm8BvC%2Fo7y2KmXgm%2FkocewMk3SKSppXzzl7WO5uuJizBrQ4mxfIKelmoC1g%2BYP%2BJS0K0E5E2ZIi%2FcW%2FAg2IY%2BiIg7wRYYANd%2FZ7xWsBCAUuANjTGzZh%2BO4ye5ejiugV0d4kuGGqXaFm96hMV0J1TYkrpUxJ48xH3Akd8mItp2BE3Ju5YGzes1wgybgWbF20JaTcLtJPrJA1PlzN3a%2BLc3iAmRZEuFpjrpr3BzCSLYneDG7upJ3drevKSaaBheHLVCfbEkd%2BsuLYCcA4qEQMcDlkyqxIgBjGJdblyALIeRlsYbrnauTHUKEeFnn3hRt0gp3VurNBxRPWMVtgnYjgFnzk34CNp1nncTg8L6Oo6gH56lIRIg6AH6Bk96s4Hl9BjRdeP21hDyPoHaokz4yJnxrmYNUsZAHSFrKBklawm0PyJWRbRMsDFQsUTUrYa0mOMu8CE5ESQ4GXIkz6%2FDcTlU4Ep9iG5kxlrHAQldCpo6VfaSCfg6jjiTXYcYRuWLp1MdLsxMFg3Nu6VGwPN3djLpjJULx9E%2FBmjV%2Bjkbc%2FWhWndJZMuu4b7dnC%2BuWNwDV0zqsBrDHNPO4ZvqNkA8HrPkJsasa2JJqXYdWfy%2FjNK6aq3drXNVznNfXxPdaKPKGaul9Cnlbreq72p2PkhZmjNZT%2F8FsFklHA%2F%2FbERkNW7S1SH63U0IWs3DkelEq6Go3ZRC8MIR%2B1%2BhaN23cGeV9DHy8LRuzgWLug8Hj1ubTtNQmmKSc2stzF1BUt23Zi0COxLt5r4NBJIPp4WgvjD8RtB4dFiuwFW37q%2B2iukz%2Fc4xW55GL7HNXvle5y6i6Nt%2B55Zsrx8zpFOSDG2dS3ou7dyoC0of6UMLwQy%2FmnvrHTkyq93gqy%2BrRJWY3ejIpirG2snA3U3Vr%2FcDdCuyeEuBfVLk3bjnX11NQleZbM7v%2Ffo8FXUf2ubnhJ8E7lvDcdRgnt1sihJHc5TDyjCHGQx2D8KOzOOV7MFZ5i20MVQ1O4Vqx1TtybtoWpSbRnviSbdxvv16mpSxbuD06Tbr%2F16pqWdlMp2B6fKZHj7As0dq95F0fFYhiogTwynLT8IQTowGmcXOcaTcc4IkgZTkzjd2Qv4XrLeUXmu%2BqZZ9PvmA8la25id3Ky5tr1optU4VnHrHknxhuoYTatf0Yp3s%2BramnL5gnwkHq%2BrrcxOlh46T6XU3nnW5bEUeQw%2FTo7hazuTktsxYBqerhl0r85EiPIj%2F9tIzOvXnIdXJ6Yu0UUY3InvhRmd9gSUOpp2pgquQlV2KrwUvpKj4hcjpEIIlO%2FQ899Qkdi0rJSqpdCO51a3k5hQoZ22oiqvztb12jQt8ZjdmAbaY%2FZVtio%2Bf5Ntis%2FpTJZIqImsXhmTnTemfBOvbk08mX6tUlI8%2FXYq8O5f%3C%2Fdiagram%3E%3C%2Fmxfile%3E))


