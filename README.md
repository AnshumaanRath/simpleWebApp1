 Simple Product Management API – Spring Boot
tags:

Spring Boot
REST API
H2 Database
CRUD
Java
🛒 Simple Product Management API – Spring Boot
This is a basic Spring Boot REST API for managing products. It supports full CRUD operations (Create, Read, Update, Delete) and uses an in-memory H2 database. The API is tested using Postman and runs locally on http://localhost:8080.

📦 Features
Add new products
Retrieve all products
Retrieve a product by ID
Update product details
Delete a product

🧩 Technologies Used
Java 17+
Spring Boot
Spring Web
H2 Database (In-memory)
Postman (for testing)


📁 API Endpoints
Method	Endpoint	Description
GET	/get products	Retrieve all products
GET	/get products/{prodid}	Retrieve product by ID
POST	/get products	Add a new product (JSON body)
PUT	/update products	Update existing product
DELETE	/get products/delete/{prodid}	Delete product by ID

Export to Sheets

🚀 How to Run the Project
Step 1: Clone the Repository
Bash

git clone https://github.com/your-username/simple-product-api.git
cd simple-product-api
Step 2: Run the Application
You have two options to run the application:

Option 1: Using Maven Wrapper (No need to install Maven separately)
Bash

./mvnw spring-boot:run
Option 2: Run from IDE
Open SimpleWebAppApplication.java in your IDE and run the main method directly.

Step 3: Access the Application
API Base URL: http://localhost:8080
H2 Console: http://localhost:8080/h2-console
🧪 Testing the API with Postman
You can use Postman to test each API endpoint manually.

Open Postman and choose the appropriate HTTP method (GET, POST, PUT, DELETE).
Use an endpoint like: http://localhost:8080/get products
For POST / PUT Requests:
When sending POST or PUT requests, you'll need to configure the request body:

Go to the Body tab.
Select raw.
Choose JSON from the dropdown.
Paste a sample JSON like the one below:

JSON

{
  "prodid": 101,
  "prodname": "Wireless Mouse",
  "price": 499.99
}

Set the following Headers:

Key	Value
Content-Type	application/json

Export to Sheets
🗃️ H2 Database Console
The project uses an H2 in-memory database, which resets every time the server restarts.

🔗 Access Console:
Visit: http://localhost:8080/h2-console

🔐 Default Credentials:
JDBC URL: jdbc:h2:mem:testdb
Username: sa
Password: (leave blank)
✅ Ensure this is present in application.properties:
Properties

spring.h2.console.enabled=true
spring.h2.console.path=/h2-console
spring.datasource.url=jdbc:h2:mem:testdb


