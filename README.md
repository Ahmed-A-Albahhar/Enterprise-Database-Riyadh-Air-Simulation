# Enterprise-Database-Riyadh-Air-Simulation
A normalized relational database simulation for Riyadh Air, featuring SQL DDL/DML scripting and BI-focused querying.
# Enterprise Database Architecture: Riyadh Air Simulation

## 📌 Project Overview
This project involves the end-to-end design and implementation of a normalized relational database for Riyadh Air, a newly established airline scaling for global operations. The database architecture translates complex business operations—such as flight scheduling, pilot assignments, cabin class pricing, and passenger reservations—into a scalable, structured data environment.

## 💡 Business Impact & Key Takeaways
* **Scalable Operations:** Engineered a flexible database architecture designed to handle large-scale daily airline operations and future fleet expansions.
* **Automated Pricing Logic:** Integrated business rules directly into the relational design, deriving Economy, Business, and First-Class fares dynamically based on flight base fares (e.g., Base + 75% for Business).
* **Data Integrity & Normalization:** Applied strict primary and foreign key constraints across 8 distinct tables to ensure data consistency, preventing double-bookings and enforcing airplane capacity limits.

## 🗄️ Database Schema & Normalization
The database was designed with full normalization to eliminate redundancy and maintain structural integrity. The core entity relationships include:
* **AIRPLANE & CABIN_TYPE:** Tracks fleet capacity (e.g., Boeing 787-9) and links specific cabin configurations to each aircraft.
* **FLIGHT & PILOT:** Manages flight schedules, routes, and pilot assignments, ensuring no scheduling conflicts.
* **RESERVATION, PASSENGER, & TICKET:** Handles the booking lifecycle, linking individual passengers to active reservations, luggage allowances, and specific ticket details (e.g., meal preferences).

## ⚙️ Technical Implementation (SQL)
The project encompasses the complete Data Definition Language (DDL) and Data Manipulation Language (DML) lifecycle:
* **DDL Scripts:** Created 8 relational tables (`AIRPLANE`, `PILOT`, `FLIGHT`, `RESERVATION`, `TICKET`, `PASSENGER`, `CABIN_TYPE`, `SEAT`) with strict data types, `NOT NULL` constraints, and interconnecting foreign keys.
* **DML Scripts:** Seeded the database with comprehensive demo data to simulate a live operational environment.
* **Analytical Querying:** Developed highly structured SQL queries utilizing `INNER JOIN`, `GROUP BY`, and aggregate functions (`SUM`, `AVG`, `COUNT`) to extract business intelligence.

## 📊 Business Intelligence Query Examples
The database seamlessly supports operational reporting, including:
* **Capacity & Utilization:** Tracking total passengers per flight and identifying high-capacity aircraft (>200 seats).
* **Financial Reporting:** Calculating total revenue generated from specific flight routes using aggregated ticket fares.
* **Logistics Analysis:** Determining average luggage allowances for specific departure hubs to optimize cargo weight limits.
