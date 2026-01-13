<div align="center">
   
  [![English](https://img.shields.io/badge/English-blue)](README.md)
  [![Português](https://img.shields.io/badge/Português-green)](README-pt-br.md)
  
</div>

# Cash Card Service API

A robust and secure RESTful API designed for managing digital debit cards and family allowances.

This project was developed as part of my **Spring Boot** specialization portfolio, focusing on API design best practices, security, and automated testing.

## Tech Stack

* **Java 21** (Core Language)
* **Spring Boot 3.5** (Main Framework)
* **Spring Data JDBC/JPA** (Data Persistence)
* **Spring Security** (Authentication & Authorization)
* **H2 Database** (In-Memory Database for Dev)
* **JUnit 5** (Unit & Integration Testing)
* **Gradle (Groovy)** (Dependency Management)
* **Docker** (Containerization)

## Key Features

* **Full CRUD:** Create, Read, Update, and Delete operations for Cash Cards.
* **Security (AuthN/AuthZ):**
    * Authentication via Basic Auth.
    * Authorization based on **Ownership** (Users can only view/edit their own cards).
    * Protected routes and sensitive endpoints.
* **Pagination & Sorting:** Optimized endpoints for handling large datasets.
* **Error Handling:** User-friendly and compliant HTTP error responses (404, 403, 401).

## Methodology: TDD (Test-Driven Development)

This project strictly followed the **Red-Green-Refactor** cycle:
* **Red:** Every feature started with a failing test.
* **Green:** Code was written specifically to pass the test.
* **Refactor:** Code was cleaned and optimized while keeping tests green.
* **Coverage:** Comprehensive testing for Controllers (Integration) and Domain Layer (Unit).

## How to Run
### Steps

## Como rodar o projeto
1. Clone the repository:
```bash
git clone https://github.com/cgmarquess/cash-card-service.git
```
2. Open the folder
```bash
cd cash-card-service
```
3. Run with Gradle
-To run the tests (TDD):
```bash
./gradlew test
```
-To upload the application (API):
```bash
./gradlew bootRun
```
### How to run with Docker
1. Generate the Docker image:
```bash
docker build -t cash-card-api . 
```
2. Run the container:
```bash
docker run -p 8080:8080 cash-card-api
```
Developed by [Gabriel Marques] - [[LinkedIn](https://www.linkedin.com/in/cgmarquess/?locale=en_US)]
