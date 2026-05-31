# Medicare Management System - Microservices

## Overview
A Healthcare Management System built using Spring Boot Microservices Architecture.
Features:
- Patient Management
- Doctor Management
- Appointment Management
- Service Discovery using Eureka
- API Gateway
- JWT Authentication
- Role Based Access Control (RBAC)
- OpenFeign Communication
- Docker Containerization

---

## Architecture
Client
→ API Gateway
→ Microservices
- Auth Service
- Patient Service
- Doctor Service
- Appointment Service

Service Discovery handled by Eureka Server.

---

## Technologies Used
- Java 21
- Spring Boot 3
- Spring Cloud
- Eureka Server
- API Gateway
- Spring Data JPA
- MySQL
- JWT
- OpenFeign
- Docker
- Maven

---

## Docker Deployment

```bash
docker compose up -d
```

---

## Screenshots

### Eureka Service Registry
screenshots/Screenshot 2026-06-01 002712.png
screenshots/Screenshot 2026-06-01 002811.png

### Docker Containers Running
screenshots/Screenshot 2026-06-01 003801.png

### Admin Login
screenshots/Screenshot 2026-06-01 011659.png

### Patient Service
screenshots/Screenshot 2026-06-01 003135.png

### Doctor Service
screenshots/Screenshot 2026-06-01 003211.png

### Appointment Service
screenshots/Screenshot 2026-06-01 003256.png

### Appointment Details (Feign Client)

### RBAC - USER Forbidden
screenshots/Screenshot 2026-06-01 003517.png

### RBAC - ADMIN Success
screenshots/Screenshot 2026-06-01 003541.png
screenshots/Screenshot 2026-06-01 003606.png

---

## Security
JWT Authentication

Roles:
- ADMIN
- USER

Authorization Rules:

| Endpoint |       ADMIN    |   USER |
|-----------|----------------|----------|
| GET Patients | ✅         | ✅ |
| GET Doctors | ✅          | ✅ |
| GET Appointments | ✅     | ✅ |
| POST Doctors | ✅         | ❌ |
| DELETE Doctors | ✅       | ❌ |
| POST Patients | ✅        | ❌ |
| DELETE Patients | ✅      | ❌ |

---

## Author
Sai Krishna Peddinti
