## Overview

This project aims to develop a user-friendly car park management system for universities using Spring technologies. It facilitates parking space booking, real-time availability checks, online payments, and reporting functionalities.

## Functional Requirements

User Management:
User registration (students, faculty, staff) with basic information (name, email, license plate).
Admin creation and management of user accounts (permits, parking violations).
Parking Management:
Booking parking spaces in advance for users with valid permits (specify date and time).
Real-time display of parking space availability.
User check-in/out upon entering/leaving (optional: license plate recognition).
Admin assignment of parking spaces for special events (optional).
Payment System:
Online parking fee payment through integrated payment gateway.
Generation and delivery of parking violation notices with associated fines.
Reporting:
User access to past parking history (bookings, payments).
Generation of reports on parking usage, revenue, and violations (for admins).
Additional Features:
Waitlist system for unavailable parking spaces.
Integration with university ID card system for seamless access (optional).
Car park location map with available spaces (optional).
## Mockups (Wireframes)

Create mockups for:
User registration/login.
User dashboard (parking permits, booking options, parking history).
Real-time car park map (optional: color-coded availability).
Parking booking interface (calendar selection, available spaces).
Payment gateway integration for online fee payment.
Admin panel (user/permit management, parking assignments, report generation) (optional).
## System Behavior and REST API Endpoints

User Management:
POST /users: Registers a new user with basic information and license plate.
GET /users/{id} (Admin only): Retrieves user details by ID.
PUT /users/{id} (Admin only): Updates user information and permits.
Parking Management:
GET /parking/availability: Retrieves real-time availability data.
POST /parking/reservations: Creates a parking reservation for a user.
PUT /parking/reservations/{id}: Updates or cancels an existing reservation.
POST /parking/checkin (optional with license plate recognition): User checks in upon entering.
POST /parking/checkout (optional with license plate recognition): User checks out upon leaving.
PUT /parking/assignments/{id} (Admin only): Assigns a parking space to a user manually.
Payment System:
POST /payments: Processes an online payment for parking fees.
GET /violations/{id}: Retrieves details of a parking violation notice.
Reporting:
GET /parking/history: Retrieves user's past parking history (bookings, payments).
GET /reports/usage (Admin only): Generates reports on parking usage.
GET /reports/revenue (Admin only): Generates reports on parking revenue.
GET /reports/violations (Admin only): Generates reports on parking violations.
Note: This is a foundational design. You can expand on functionalities based on specific needs. Security aspects (authentication, authorization) and external system integrations (payment gateways, ID card systems) are crucial considerations for real-world applications.

## Technologies Used

Java
Spring Boot
Spring Security
Spring Data JPA
MySQL or PostgreSQL (database)
## Getting Started

Clone this repository.
Ensure necessary tools are installed (Java, Maven or Gradle).
Configure a database connection in application.properties.
Run the application using Maven or Gradle commands.
