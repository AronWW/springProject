# University Car Park Management System (Spring Project)

## Overview

This project implements a car park management system for a university using Spring technologies. It facilitates user registration, parking availability display, entry/exit recording, and optional functionalities like reservations and payments.

## Functional Requirements

### User Management:
- User registration (students, faculty, staff) with basic information (name, email, license plate).
- Assigning user roles with varying permissions.

### Car Park Management:
- Define total parking slots and maintain real-time availability.
- Display available parking spaces in real-time.
- Implement optional parking slot reservation (based on user role).

### Entry/Exit Management:
- License plate scanning upon entry and exit.
- System validation of license plate and user permissions.
- Automatic update of available parking slots after entry/exit.

### Payment System:
- Integration of various payment methods for parking duration.
- Track parking fees and generate reports (admin only).

### Notifications:
- Alert users nearing parking session expiry.
- Inform users of full car park status.

### Additional Features:
- Search for available parking by location (multi-level parking).
- Access historical parking data (user and admin).
- Manage season parking permits (optional, admin only).

## System Behavior and REST API Endpoints

### User Management:
- POST /users: Registers a new user with basic information.
- GET /users/{id} (Admin only): Retrieves user details by ID.
- PUT /users/{id} (User can update own profile): Updates user information.

### Car Park Management:
- GET /carpark/status: Retrieves current total and available parking slots.

### Entry/Exit Management:
- POST /entry (with license plate): Validates license plate and user permission, updates available slots (increment -1).
- POST /exit (with license plate): Validates license plate, updates available slots (increment +1).

### Payment System:
- POST /payments: Processes parking fee payment for a specific user and duration.
- GET /reports/parking (Admin only): Retrieves parking fee reports.

### Notifications:
- Implement push notifications or SMS alerts triggered by server-side logic.

### Additional Endpoints:
- GET /carpark/search?location={location} (optional): Search for available parking spaces based on location.
- GET /history/parking (User can access own history): Retrieves historical parking data for a user.
- POST /permits (Admin only): Manages season parking permits.

## Technologies Used

- Java
- Spring Boot
- Spring Security
- Spring Data JPA
- MySQL or PostgreSQL (database)
- License plate recognition system integration (optional)
