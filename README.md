# Spring Boot 3 Security

## Overview
This project demonstrates a basic security implementation using Spring Boot 3, Spring Security, and JWT (JSON Web Token). It is designed to secure REST APIs and includes user authentication using JWT tokens.

## Prerequisites
- **Java 17**
- **Maven 3.6+**
- **MySQL Database**

## Setup

### 1. Clone the Repository

- git clone https://github.com/kokonaing-dev/spring-security-jwt.git


### 2. Test the Application
You can test the API endpoints using [Postman](https://www.postman.com/).

To decode and verify JWT tokens, use [jwt.io](https://jwt.io).

#### Example Commands
You can also use the following commands to test specific endpoints:

```bash
# Testing the Add User endpoint
curl -X POST http://localhost:8080/auth/addNewUser \
-H "Content-Type: application/json" \
-d '{"id": 2, "name": "John Admin", "email": "john.admin@example.com", "password": "password123", "roles": "ROLE_ADMIN"}'

# Testing the Generate Token endpoint
curl -X POST http://localhost:8080/auth/generateToken \
-H "Content-Type: application/json" \
-d '{"username": "John Doe", "password": "password123"}'

# Testing the User Profile endpoint with Bearer Token
curl -X GET http://localhost:8080/auth/user/userProfile \
-H "Content-Type: application/json" \
-H "Authorization: Bearer <your-jwt-token>"
