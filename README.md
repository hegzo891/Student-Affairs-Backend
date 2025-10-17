# 🎓 UniLink - Student Affairs Management System (Backend)

![Java](https://img.shields.io/badge/Java-17-orange)
![Spring Boot](https://img.shields.io/badge/Spring%20Boot-3.0-green)
![Spring Security](https://img.shields.io/badge/Spring%20Security-JWT-blue)
![MySQL](https://img.shields.io/badge/MySQL-8.0-lightblue)

---

## 📋 Overview

**UniLink** is a digital backend solution designed to streamline communication and service delivery between **students** and **university administration**.  
Built with **Java Spring Boot**, it offers secure authentication, request tracking, appointment management, and document handling through a robust RESTful API.

---

## 🎯 Key Features

- 🔐 Dual-role authentication (Student & Staff)
- 📨 Service request management (Submit, track, update)
- 📅 Appointment scheduling with conflict prevention
- 🔔 Real-time notifications
- 📂 Document upload & management
- 🧩 Role-based access control
- 🌐 RESTful API architecture

---

## 🛠 Tech Stack

| Category | Technologies |
|-----------|---------------|
| **Backend** | Java 17, Spring Boot 3.0 |
| **Security** | Spring Security, JWT |
| **Database** | MySQL 8.0, JPA, Hibernate |
| **Documentation** | Swagger / OpenAPI |
| **Testing** | JUnit, Mockito, Postman |
| **Build Tool** | Maven |

---

## 🏗 System Architecture

```text
Controller Layer  (REST APIs)
        ↓
Service Layer     (Business Logic)
        ↓
Repository Layer  (Data Access)
        ↓
Database          (MySQL)
📁 Project Structure
text
Copy code
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
Java 17+

MySQL 8.0+

Maven 3.6+

Steps
Clone the repository

bash
Copy code
git clone https://github.com/MahmoudEhab3/Student-Affairs-Backend.git
cd Student-Affairs-Backend
Create the MySQL database

sql
Copy code
CREATE DATABASE unilink_db;
Update application properties

properties
Copy code
spring.datasource.url=jdbc:mysql://localhost:3306/unilink_db
spring.datasource.username=your_username
spring.datasource.password=your_password
Run the application

bash
Copy code
mvn spring-boot:run
Access Swagger documentation

bash
Copy code
http://localhost:8080/swagger-ui.html
📚 API Endpoints
🔑 Authentication
Method	Endpoint	Description
POST	/api/auth/login	User authentication
POST	/api/auth/register	User registration
POST	/api/auth/refresh	Refresh JWT token

📨 Requests Management
Method	Endpoint	Description
GET	/api/requests	Get all requests (Staff)
POST	/api/requests	Create new request (Student)
PUT	/api/requests/{id}	Update
