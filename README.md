# Spring-Boot-API-CRUD-DB
A Subscription Management application implemented using Spring Boot API and MySQL database.

# Subscription Management Implementation Spring Boot API CRUD with Database
This is a simple Spring Boot application implementing CRUD operations with a MySQL database. It provides an API to manage subscription data, such as adding, updating, retrieving, and deleting subscriber details.

# Features
- CRUD operations: Create, Read, Update, Delete subscription records.
- RESTful API: Exposes endpoints to interact with the subscription database.
- MySQL Database Integration: Uses MySQL to store subscriber information.

# Technologies Used
- Spring Boot: Backend framework for building Java applications.
- MySQL: Relational database for storing subscription data.
- Postman: For testing the REST API.

# Prerequisites
- Java: JDK 11 or higher.
- Maven: Build tool for the project.
- MySQL: A running MySQL instance.

# Setting Up the Project
1. Clone the Repository
   - Clone this repository to your local machine:
     ```
     git clone https://github.com/RaamTechLead-DSAI/Spring-Boot-API-CRUD-DB.git
     cd Spring-Boot-API-CRUD-DB

2. Set Up MySQL Database
   - Install MySQL and start the MySQL server.
   - Create a database for the application:
   `CREATE DATABASE subscription_management;`
   - Configure the application.properties file in src/main/resources/ with your MySQL connection details:
      ```
      spring.datasource.url=jdbc:mysql://localhost:3306/subscription_management
      spring.datasource.username=<your_username>
      spring.datasource.password=<your_password>
      spring.datasource.driver-class-name=com.mysql.cj.jdbc.Driver
   - Make sure to replace <your_username> and <your_password> with your actual MySQL credentials.

3. Build and Run the Application
   - Use Maven to build and run the application:
   - The application will start on http://localhost:8080.
      ```
      mvn clean install
      mvn spring-boot:run

# API Endpoints
| Method | Endpoint | Description |
|----------|----------|----------|
| GET | /api/subscribers | Get all subscribers |
| GET | /api/subscribers/{id} | Get a subscriber by ID |
| POST | /api/subscribers | Add a new subscriber |
| PUT | /api/subscribers | Update an existing subscriber |
| DELETE | /api/subscribers/{id} | Delete a subscriber by ID |

# Testing the API with Postman
1. Import Collection
You can import the provided Postman collection into Postman. This collection includes all the API requests that correspond to the CRUD operations.

2. Example Requests
- GET All Subscribers:
   - URL: http://localhost:8080/api/subscribers
   - Method: GET
- GET Subscriber by ID:
   - URL: http://localhost:8080/api/subscribers/{id}
   - Method: GET
   - Body (JSON)
- POST Create Subscriber:
   - URL: http://localhost:8080/api/subscribers
   - Method: POST
     ```json
      {
       "status": "Active",
       "firstName": "John",
       "lastName": "Doe",
       "email": "john.doe@example.com",
       "contactNum": "1234567890",
       "startDate": "2024-11-20"
      }
- PUT Update Subscriber:
   - URL: http://localhost:8080/api/subscribers
   - Method: PUT
   - Body (JSON)
     ```json 
     {
       "subscriberId": 1,
       "status": "Inactive",
       "firstName": "John",
       "lastName": "Doe",
       "email": "john.doe@example.com",
       "contactNum": "1234567890",
       "startDate": "2024-11-20"
      }

- DELETE Subscriber:
  - URL: http://localhost:8080/api/subscribers/{id}
  - Method: DELETE

# License
This project is licensed under the MIT License - see the LICENSE file for details.



