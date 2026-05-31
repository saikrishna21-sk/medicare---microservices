# Medicare Management System - Microservices Architecture

## Overview
The Medicare Management System is a Spring Boot Microservices project designed to manage patients, doctors, and appointments in a healthcare environment.
The application follows a distributed microservices architecture using Spring Cloud components such as Eureka Service Registry, API Gateway, OpenFeign, and Resilience4j Circuit Breaker.
Authentication and Authorization are implemented using JWT (JSON Web Tokens) with Role-Based Access Control (RBAC).

## Architecture
Client → API Gateway → Microservices
* Auth Service
* Patient Service
* Doctor Service
* Appointment Service

Service Discovery is handled by Eureka Server.
Inter-service communication is implemented using OpenFeign.
Fault tolerance is implemented using Resilience4j Circuit Breaker.

## Microservices

### Service Registry
Responsible for service discovery using Netflix Eureka.

### API Gateway
Single entry point for all client requests.
Performs JWT validation and role-based authorization.

### Auth Service
Handles user registration, login, password encryption, and JWT token generation.

### Patient Service
Manages patient records.

### Doctor Service
Manages doctor records.

### Appointment Service
Manages appointments and communicates with Patient Service and Doctor Service to provide aggregated appointment details.

## Tech Stack
* Java 21
* Spring Boot
* Spring Cloud
* Eureka Server
* Spring Cloud Gateway
* OpenFeign
* Resilience4j
* Spring Security
* JWT
* MySQL
* Docker
* Docker Compose
* Swagger / OpenAPI

## Features
* Microservices Architecture
* Service Discovery using Eureka
* API Gateway Routing
* JWT Authentication
* Role-Based Authorization (ADMIN / PATIENT)
* OpenFeign Inter-Service Communication
* Circuit Breaker Pattern
* Dockerized Deployment
* Swagger API Documentation
* CRUD Operations for Patients, Doctors, and Appointments

## Running the Project
```bash
docker compose up -d
```

Verify running containers:
```bash
docker ps
```

Access Eureka Dashboard:
http://localhost:8761

Access API Gateway:
http://localhost:8080

## Future Enhancements

* Kafka Event Streaming
* Distributed Tracing
* Centralized Logging
* Kubernetes Deployment
* Monitoring using Prometheus and Grafana
