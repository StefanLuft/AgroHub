# AgroHub

A RESTful API service for an agro-platform connecting farmers and buyers.
Implemented a role model (Farmer, Client), category and product management, order processing, and farm store statistics.

## Tech Stack
* **Language:** Java 25
* **Framework:** Spring Boot 4.0.3 (Web, Data JPA)
* **Database:** PostgreSQL
* **Authentication:** JWT Tokens
* **Tools:** Maven
* **Documentation:** Swagger (Springdoc OpenAPI)

## Features
* **Authentication:** Registration and login (issuing a JWT token).
* **Public access:** View product lists, categories, and search by name.

* **FARMER Role:**
* Manage your categories (create, delete).
* Manage products (add, delete).
* View your store's orders.
* Get statistics (revenue, customers).
* **CLIENT Role:**
* Place an order.
* Cancel orders.

## Installation and Run

This project uses PostgreSQL. Before running, make sure you have the database installed and running, and the connection settings are specified in application.properties (or application.yml).

1. **Clone the repository:**
```bash
git clone https://github.com/theaprilthreatwind/aitu-mvp-project.git
cd aitu-mvp-project
```
2. **Configure the PostgreSQL database:**
   Create a database (e.g., agrohub) and update the configuration in src/main/resources/application.properties:
```bash
spring.datasource.url=jdbc:postgresql://localhost:5432/agrohub
spring.datasource.username=your_username
spring.datasource.password=your_password
spring.jpa.hibernate.ddl-auto=update
```
3. **Run the application:**
```bash
./mvnw spring-boot:run
```

4. **Enabling frontend access (the entire frontend bridge is built via ngrok):**
```bash
ngrok config add-authtoken <38DU12yBHRx4Jo34wRMlPxpFZP8_89xoDdkLsa2iec1G7PE2q>
ngrok http 8080
```
Copy the URL (for example: https://unnegotiated-apocalyptically-paulette.ngrok-free.dev) and share it with the frontend developers.

5. **Swagger API Documentation:**
   After successfully launching, navigate to:
   https://unnegotiated-apocalyptically-paulette.ngrok-free.dev/swagger-ui/index.html (you can test all endpoints here without third-party software).

**Author:** Miron Naidanov