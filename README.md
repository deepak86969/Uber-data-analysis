# Uber-data-analysis
Analysis Uber data 

Analysis of 2,000 Uber bookings (July 2024) using MySQL and Power BI.

## Files
- `data/booking.sql` — Database schema + all 2000 records
- `queries/analysis_queries.sql` — 10 SQL analysis queries & views
- `excel/booking.xlsx` — Source data in Excel format

## Setup
sql
CREATE DATABASE uber;
USE uber;

CREATE TABLE booking (
  `id` INT AUTO_INCREMENT PRIMARY KEY,
  `Date` DATE,
  `Time` VARCHAR(20),
  `Booking_ID` VARCHAR(50),
  `Booking_Status` VARCHAR(100),
  `Customer_ID` VARCHAR(50),
  `Vehicle_Type` VARCHAR(100),
  `Pickup_Location` VARCHAR(255),
  `Drop_Location` VARCHAR(255),
  `V_TAT` FLOAT,
  `C_TAT` FLOAT,
  `Canceled_Rides_by_Customer` VARCHAR(255),
  `Canceled_Rides_by_Driver` VARCHAR(255),
  `Incomplete_Rides` VARCHAR(50),
  `Incomplete_Rides_Reason` VARCHAR(255),
  `Booking_Value` INT,
  `Payment_Method` VARCHAR(100),
  `Ride_Distance` INT,
  `Driver_Ratings` FLOAT,
  `Customer_Rating` FLOAT
) ;



## Key Insights
- Booking statuses: Success, Canceled by Customer, Canceled by Driver, Driver Not Found
- Vehicle types: Bike, eBike, Auto, Mini, Prime Sedan, Prime SUV, Prime Plus
- Payment methods: Cash, UPI, Credit Card, Debit Card
