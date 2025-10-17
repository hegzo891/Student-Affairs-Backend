UniLink - Student Affairs Management System (Backend)
https://img.shields.io/badge/Java-17-orange
https://img.shields.io/badge/Spring%2520Boot-3.0-green
https://img.shields.io/badge/Spring%2520Security-JWT-blue
https://img.shields.io/badge/MySQL-8.0-lightblue

📋 Project Overview
UniLink is a comprehensive digital platform designed to streamline communication and service delivery between students and university administration. This repository contains the backend service built with Java Spring Boot that powers the UniLink application.


🎯 Key Features
Dual-Role Authentication System (Student & Staff)

Service Request Management (Submit, Track, Update Status)

Appointment Scheduling System with Conflict Prevention

Real-time Notification System

Document Upload & Management

Role-Based Access Control

RESTful API Architecture

🛠 Tech Stack
Backend Framework: Java 17, Spring Boot 3.0

Security: Spring Security, JWT Authentication

Database: MySQL with Spring Data JPA & Hibernate

API Documentation: Swagger/OpenAPI

Testing: JUnit, Mockito, Postman

Build Tool: Maven

🏗 System Architecture
Controller Layer (REST APIs)
    ↓
Service Layer (Business Logic)
    ↓
Repository Layer (Data Access)
    ↓
Database (MySQL)

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

Prerequisites
Java 17 or higher

MySQL 8.0

Maven 3.6+

Steps to Run Locally
Clone the repository

bash
git clone https://github.com/MahmoudEhab3/Student-Affairs-Backend.git
cd Student-Affairs-Backend
Configure Database

bash
# Create MySQL database
CREATE DATABASE unilink_db;
Update application properties

properties
# src/main/resources/application.properties
spring.datasource.url=jdbc:mysql://localhost:3306/unilink_db
spring.datasource.username=your_username
spring.datasource.password=your_password
Run the application

bash
mvn spring-boot:run
Access API Documentation

text
http://localhost:8080/swagger-ui.html
📚 API Endpoints
Authentication
Method	Endpoint	Description
POST	/api/auth/login	User authentication
POST	/api/auth/register	User registration
POST	/api/auth/refresh	Refresh JWT token
Requests Management
Method	Endpoint	Description
GET	/api/requests	Get all requests (Staff)
POST	/api/requests	Create new request (Student)
PUT	/api/requests/{id}	Update request status (Staff)
GET	/api/requests/student/{studentId}	Get student's requests
Appointments
Method	Endpoint	Description
GET	/api/appointments	Get available slots
POST	/api/appointments	Book appointment
PUT	/api/appointments/{id}	Reschedule appointment
DELETE	/api/appointments/{id}	Cancel appointment
For complete API documentation, run the application and visit /swagger-ui.html

🧪 Testing
Run Unit Tests
bash
mvn test
API Testing with Postman
Import the Postman collection from /docs/postman-collection.json

Update environment variables

Execute test scenarios

👥 Team Structure
Backend Team (2 Developers):

Mahmoud Ehab - Primary Backend Developer (Sprint 2)

Ahmed hegazy - Backend Developer




You can customize the contact details and add any specific technical details about your implementation.

