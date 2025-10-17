🎓 UniLink - Student Affairs Management System (Backend)

📋 Overview

UniLink is a comprehensive backend service built with Java Spring Boot to streamline communication and service management between students and university administration.
The system provides a secure, scalable, and efficient digital platform for handling student affairs such as service requests, appointment scheduling, and document management.

🎯 Key Features

🔐 Dual-Role Authentication System – Secure login for both students and staff.

📨 Service Request Management – Submit, track, and update request statuses.

📅 Appointment Scheduling System – Book and manage appointments with conflict prevention.

🔔 Real-Time Notifications – Instant updates on request and appointment changes.

📂 Document Upload & Management – Secure storage and retrieval of digital files.

🧩 Role-Based Access Control (RBAC) – Access restrictions based on user roles.

🌐 RESTful API Architecture – Clean and well-documented endpoints.

🛠 Tech Stack
Category	Technologies
Backend Framework	Java 17, Spring Boot 3.0
Security	Spring Security, JWT Authentication
Database	MySQL 8.0, Spring Data JPA, Hibernate
API Documentation	Swagger / OpenAPI
Testing	JUnit, Mockito, Postman
Build Tool	Maven
🏗 System Architecture
Controller Layer  (REST APIs)
        ↓
Service Layer     (Business Logic)
        ↓
Repository Layer  (Data Access)
        ↓
Database          (MySQL)

📁 Project Structure
src/
├── main/
│   ├── java/com/unilink/
│   │   ├── controller/     # REST API endpoints
│   │   ├── service/        # Business logic layer
│   │   ├── repository/     # Data access layer
│   │   ├── entity/         # JPA entities
│   │   ├── dto/            # Data transfer objects
│   │   ├── security/       # Authentication & authorization
│   │   └── config/         # Application configuration
│   └── resources/
│       ├── application.properties
│       └── data.sql        # Initial data

🚀 Installation & Setup
✅ Prerequisites

Java 17 or higher

MySQL 8.0+

Maven 3.6+

⚙️ Steps to Run Locally

Clone the repository

git clone https://github.com/MahmoudEhab3/Student-Affairs-Backend.git
cd Student-Affairs-Backend


Create MySQL database

CREATE DATABASE unilink_db;


Update application properties

# src/main/resources/application.properties
spring.datasource.url=jdbc:mysql://localhost:3306/unilink_db
spring.datasource.username=your_username
spring.datasource.password=your_password


Run the application

mvn spring-boot:run


Access API documentation

http://localhost:8080/swagger-ui.html

📚 API Endpoints
🔑 Authentication
Method	Endpoint	Description
POST	/api/auth/login	User authentication
POST	/api/auth/register	User registration
POST	/api/auth/refresh	Refresh JWT token
📨 Requests Management
Method	Endpoint	Description
GET	/api/requests	Get all requests (Staff only)
POST	/api/requests	Create a new request (Student)
PUT	/api/requests/{id}	Update request status (Staff)
GET	/api/requests/student/{studentId}	Get student’s requests
📅 Appointments
Method	Endpoint	Description
GET	/api/appointments	Get available slots
POST	/api/appointments	Book appointment
PUT	/api/appointments/{id}	Reschedule appointment
DELETE	/api/appointments/{id}	Cancel appointment

💡 For full API documentation, visit /swagger-ui.html after running the project.

🧪 Testing
🧱 Run Unit Tests
mvn test

🧰 API Testing with Postman

Import the Postman collection from /docs/postman-collection.json

Set up environment variables

Run automated test scenarios

👥 Team Structure

Backend Development Team (2 Members)

Mahmoud Ehab – Lead Backend Developer (Sprint 2)

Ahmed Hegazy – Backend Developer (API Development & Testing)
