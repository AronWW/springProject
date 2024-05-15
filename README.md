
University Car Park Management System (UCPMS)
This project implements a University Car Park Management System using Java Spring framework.

Project Overview
The UCPMS allows university staff and students to manage parking activities. Users can register, view real-time parking availability, initiate entry/exit, and pay fees. The system also offers functionalities for administrators (optional).

Technologies
Java Spring Framework
(Optional) Database (e.g., MySQL)
(Optional) Payment Gateway Integration
Features
User Registration (Students & Staff)
Vehicle Registration
Real-time Parking Availability
Parking Entry/Exit with Payment Processing
Parking History
(Optional) Permit Management
(Optional) Admin Dashboard & Reports
Getting Started
Prerequisites

Java Development Kit (JDK)
Maven
Installation

Clone this repository.
Install dependencies using mvn install.
Running the Application

(Optional) Configure database connection details.
Run the Spring application using your preferred IDE or mvn spring-boot:run.
API Endpoints (RESTful)
User Management:

POST /users - Register a new user
GET /users/{id} - Get user details by ID
Vehicle Management:

POST /vehicles - Register a new vehicle
GET /vehicles/{id} - Get vehicle details by ID
Parking Management:

GET /parking/availability - Get real-time parking availability
POST /parking/entry - Initiate parking entry for a user
POST /parking/exit - Initiate parking exit for a user
GET /parking/history/{userId} - Get user's parking history
Payment Processing:

POST /payments - Process parking fee payment
Additional Endpoints (Optional):

GET /permits - Get information on permit programs (if applicable)
GET /reports - Generate reports on parking activity (if applicable)
Note: Refer to the code for detailed implementation of these endpoints.
