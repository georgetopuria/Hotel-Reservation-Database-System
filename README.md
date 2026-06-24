# Hotel Reservation Database System

# Overview

This is a project for the B103 Databases & BigData course. The aim of the project is to build and design a relational database system for a hotel reservation system using SQL.

Database is used to manage hotel functions such as guest management, room management, bookings, payments etc. The project illustrates the concepts of relational database design, normalization, SQL queries, joins, stored procedures, triggers and transactions.

---

# Features

* Guest management
* Room type management
* Hotel room management
* Booking management
* Payment processing
* Additional hotel services
*  Relational database design Retrieving and analyzing SQL data
* Stored procedures
* Triggers
* Transactions

---

# Database Structure

There are 7 tables in the system:

## Guests

Records information on visitors including name, contact information, and date of registration.

## Room_Types

Document room types, room descriptions, room rates and room capacities.

## Hotel_Rooms

Records information about each room in the hotel and its availability.

## Bookings

Records reservation information such as booking dates and guest information.

## Payments

Records payment information for bookings.

## Services

Offers extra amenities at the hotel like breakfast, spa and bike hire.

## Booking_Services

Relates hotel services to particular bookings.

---

# Entity Relationships

The main relationships in the database are:

Many Bookings may be associated with One Guest.
* One Room Type can be associated with many Hotel Rooms.
A One Hotel Room may be seen in numerous Bookings throughout the years.
A Payments can be attached to One Booking.
Multiple Services can be used within One Booking.
* One Service can be associated with multiple Bookings.

---

# Technologies Used

* SQL
* MySQL
* DBDiagram.io
* GitHub

---

# Files Included

## schema.sql

Includes all CREATE TABLE statements, constraints, primary keys, and foreign keys.

### insert_data.sql

Includes sample data in the database.

## queries.sql

Includes SQL queries for retrieval, filtering, sorting, aggregation, grouping and joins.

## advanced_sql.sql

Includes stored procedures, triggers, and examples of transactions.

## erd.png

Entity Relationship Diagram (ERD) for the database.

## report.pdf

Final project report.

---

## Example Queries

## Show all guests

```sql
SELECT * FROM Guests;
```

## Show available rooms

```sql
SELECT *
FROM Hotel_Rooms
WHERE Status = 'Available';
```

## Calculate total revenue

```sql
SELECT SUM(Amount) AS Revenue
FROM Payments;
```

Show guests' booking details.Present guests' booking details.

```sql
SELECT
    Guests.First_Name,
    Guests.Last_Name,
    Bookings.Booking_Id
FROM Guests
JOIN Bookings
ON Guests.Guest_Id = Bookings.Guest_Id;
```

---

## Advanced SQL Features

## Stored Procedure

A stored procedure was created to get the booking information for a particular guest.

## Trigger

When a successful payment is recorded, booking information will automatically be updated.

## Transaction

A transaction is an example of multiple SQL operations that can be performed safely as a single unit.

---

# Future Improvements

Possible future enhancements include:

* Staff management system
* Customer loyalty program
* Online reservation integration
* Automated room availability tracking
The cancellation and refund process is managed.The process of cancellation and refund is managed.
Reporting dashboard and analytics

---

# Author
George Topuria

Module: B103 Databases & Big Data

Institution: Gisma University of Applied Sciences
