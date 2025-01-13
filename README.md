# ReactJS + Spring Boot CRUD Full Stack Application

This project is a Full Stack Application that demonstrates CRUD (Create, Read, Update, Delete) operations using **ReactJS** for the frontend and **Spring Boot** for the backend. The application manages employee data.

## Table of Contents
- [Features](#features)
- [Technologies Used](#technologies-used)
- [Prerequisites](#prerequisites)
- [Setup Instructions](#setup-instructions)
  - [Backend Setup](#backend-setup)
  - [Frontend Setup](#frontend-setup)
- [Run the Application](#run-the-application)
- [Screenshots](#screenshots)
- [License](#license)

---

## Features
- Add a new employee
- View all employees
- Update employee details
- Delete an employee
- Fully responsive frontend design

---

## Technologies Used
### Frontend:
- ReactJS
- Axios for API calls
- React Router DOM for navigation
- Bootstrap for styling

### Backend:
- Spring Boot
- Spring Data JPA
- MySQL database
- Maven for dependency management

---

## Prerequisites
Before you begin, ensure you have the following installed:
1. **Java Development Kit (JDK 8 or above)**  
   [Download JDK](https://www.oracle.com/java/technologies/javase-downloads.html)
2. **Node.js and npm**  
   [Download Node.js](https://nodejs.org/)
3. **MySQL**  
   [Download MySQL](https://www.mysql.com/)
4. **Git**  
   [Download Git](https://git-scm.com/)

---

## Setup Instructions

### Backend Setup
1. **Clone the Repository**
   ```bash
   git clone https://github.com/rohittbhoi/Full-Stack-Application.git
Setup Instructions
Backend Setup
Clone the Repository
Clone the repository to your local machine:

bash
Copy code
git clone https://github.com/rohittbhoi/Full-Stack-Application.git
Navigate to the Backend Folder
Switch to the backend directory:

bash
Copy code
cd Full-Stack-Application/springboot-backend
Set Up the MySQL Database

Create a new database in MySQL:
sql
Copy code
CREATE DATABASE fullstack_crud;
Update the database connection details in the application.properties file located in src/main/resources/:
properties
Copy code
spring.datasource.url=jdbc:mysql://localhost:3306/fullstack_crud
spring.datasource.username=your_mysql_username
spring.datasource.password=your_mysql_password
spring.jpa.hibernate.ddl-auto=update
Install Maven Dependencies
Run Maven to install the required dependencies:

bash
Copy code
mvn clean install
Run the Backend Application
Start the Spring Boot application:

bash
Copy code
mvn spring-boot:run
The backend will run on http://localhost:8080.

Frontend Setup
Navigate to the Frontend Folder
Switch to the frontend directory:

bash
Copy code
cd Full-Stack-Application/react-frontend
Install Dependencies
Use npm to install all required packages:

bash
Copy code
npm install
Configure the API Endpoint
Update the API endpoint in src/services/EmployeeService.js to match your backend URL:

javascript
Copy code
const EMPLOYEE_API_BASE_URL = "http://localhost:8080/api/v1/employees";
export default EMPLOYEE_API_BASE_URL;
Run the Frontend Application
Start the React application:

bash
Copy code
npm start
The frontend will be available at http://localhost:3000.

Testing the Application
Open a browser and visit http://localhost:3000.
Use the UI to perform CRUD operations:
Add Employee: Click on "Add Employee" and fill in the form.
View Employees: View the list of employees on the home page.
Edit Employee: Click on the "Edit" button next to an employee's name.
Delete Employee: Click on the "Delete" button to remove an employee.
Deployment
Backend Deployment
Package the Spring Boot Application
Generate a .jar file using Maven:
bash
Copy code
mvn clean package
Deploy on a Server
Deploy the .jar file on a server like AWS, Azure, or Heroku.
