# Spring Boot Web Application with H2 Database, JDBC, and CRUD Functionality

This Spring Boot web application serves as a base-level project to demonstrate the compatibility and ease of use of Spring Boot with an H2 in-memory database, JDBC API, and built-in validators. Maven is used for managing the project's dependencies.

## Features

- **CRUD Functionality:** Create, Read, Update, and Delete operations for a simple entity.
- **H2 In-Memory Database:** Leverages the H2 database for easy setup and development.
- **JDBC API:** Utilizes JDBC for database interaction.
- **Validators:** Includes validation for the entity fields to ensure data integrity.

## Requirements

- Java 8 or higher
- Maven 3.6.0 or higher

## H2 Console

The H2 database console can be accessed at [http://localhost:8080/h2-console](http://localhost:8080/h2-console) with the following credentials:
- **JDBC URL:** `jdbc:h2:mem:testdb`
- **Username:** sa
- **Password:** password

## Validation

Validation is implemented using the `javax.validation.constraints` package. The entity fields are annotated to ensure data integrity, such as:
- `@NotEmpty`: Ensures the field is not empty.
- `@Positive`: Ensures the field's value is positive.
- `@Size(min = x, max = y)`: Ensures the field's length is within the specified range.
- Custom validation annotations for specific business rules.

## Project Structure

The project follows a typical Spring Boot structure with the following main components:
- **Controller:** Handles incoming HTTP requests and returns responses.
- **Service:** Contains business logic and calls methods in the repository.
- **Repository:** Interfaces with the database using JDBC.
- **Model:** Represents the data structure of the application.

This setup allows for a clean separation of concerns and makes the application easy to maintain and extend.
