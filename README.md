# Hibernate1 Project

This project is a simple Java application that demonstrates the usage of Hibernate for ORM (Object-Relational Mapping) with a MySQL database. It includes DAO, service, and utility layers to manage entities and database transactions effectively.

## Table of Contents
- [Technologies Used](#technologies-used)
- [Project Structure](#project-structure)
- [Configuration](#configuration)
- [Setup](#setup)
- [Usage](#usage)
- [Testing](#testing)

## Technologies Used
- Java 21
- Hibernate 5.6.9
- MySQL Connector/J 8.0.29
- JPA 2.2 API
- JUnit 4.13.2 for testing

## Project Structure
The project is structured as follows:
src ├── main │ ├── java │ │ ├── dao │ │ │ └── IDao.java # DAO Interface │ │ ├── entities │ │ │ ├── Machine.java # Entity for Machine │ │ │ └── Salle.java # Entity for Salle │ │ ├── services │ │ │ ├── MachineService.java # Service for Machine operations │ │ │ └── SalleService.java # Service for Salle operations │ │ ├── test │ │ │ └── Test.java # JUnit test class │ │ └── util │ │ └── HibernateUtile.java # Utility class for Hibernate configuration │ └── resources │ └── hibernate.cfg.xml # Hibernate configuration file


## Configuration

### `pom.xml`
The `pom.xml` file specifies dependencies for Hibernate, MySQL, JPA API, and JUnit. Key dependencies include:
- **Hibernate Core** for ORM mapping.
- **MySQL Connector/J** for database connectivity.
- **JPA API** for standard entity management.
- **JUnit** for testing.

### `hibernate.cfg.xml`
This file contains Hibernate configurations, including:
- Database connection settings (URL, username, password)
- JDBC connection pool settings
- Hibernate SQL dialect for MySQL 8
- SQL logging settings
- Schema management settings (auto-update mode)
- Entity class mappings

### Database Configuration
The database connection is configured in `hibernate.cfg.xml`. Update the following properties based on your environment:
```xml
<property name="hibernate.connection.url">jdbc:mysql://localhost:3306/base</property>
<property name="hibernate.connection.username">your_username</property>
<property name="hibernate.connection.password">your_password</property>
```
## `Setup`
1- Clone the repository
git clone https://github.com/Elansari-Jaafar/Hibernate1.git
2- Open the project in your preferred Java IDE (e.g., IntelliJ IDEA).
3- Ensure your MySQL database is running and the schema is created.
4- Update hibernate.cfg.xml with the correct database credentials.

## `Usage`
To run the project, ensure that your database configuration is correct. The main business logic is implemented in the services package:

MachineService for managing Machine entities.
SalleService for managing Salle entities.
Execute your business logic through these services, and observe SQL statements in the logs (due to hibernate.show_sql set to true).

## `Testing`
JUnit is used for testing. To run tests, execute:
mvn test
Tests are located in the test package and are designed to validate the functionality of Hibernate mappings and service methods.
