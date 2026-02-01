# Online Order Backend Service

OnlineOrder is the backend service for a food ordering platform similar to Uber Eats or DoorDash.  
The backend is built with Spring Boot and exposes RESTful APIs to support restaurant browsing, menu management, shopping cart operations, and order processing.

---

## Tech Stack

- Java
- Spring Boot
- Spring MVC
- Spring Data JPA
- RESTful APIs
- MySQL / H2
- Gradle
- Docker (optional)

---

## Directory Structure
```
onlineorder/
│
├── src/
│ ├── main/
│ │ ├── java/com/laioffer/onlineorder/
│ │ │
│ │ ├── controller/ # REST API layer
│ │ ├── service/ # Business logic layer
│ │ ├── repository/ # Database access (JPA repositories)
│ │ ├── entity/ # Database entities
│ │ ├── model/ # DTOs / request & response objects
│ │ ├── config/ # Spring configuration
│ │ ├── OnlineOrderApplication.java # Application entry point
│ │ └── DevRunner.java # Test data initialization
│ │
│ └── test/
│
├── build.gradle # Gradle build configuration
└── docker-compose.yml # Docker deployment
```

---

## Architecture

The system follows a classic layered backend architecture.
```
Client
→ Controller
→ Service
→ Repository
→ Database
```

## Layer responsibilities:

Controller
- Handle HTTP requests
- Validate input
- Return JSON responses

Service
- Core business logic
- Order processing
- Cart operations
- Transaction handling

Repository
- Database CRUD operations
- Implemented using Spring Data JPA

Entity
- Maps Java objects to database tables

DTO / Model
- Transfer data between frontend and backend
- Prevent direct exposure of entities

---

## Core Features

### Restaurant
- List restaurants
- Browse menus
- Retrieve menu items

### Cart
- Add item to cart
- Remove item
- Update quantity
- Calculate total price

### Order
- Checkout cart
- Create order
- Persist order items

### Customer
- Register customer
- Manage customer profile

---

## API Overview

| Method | Endpoint | Description |
|--------|-----------|-------------|
| GET | /restaurants | Get all restaurants |
| GET | /menu | Get menu items |
| POST | /cart/add | Add item to cart |
| POST | /cart/remove | Remove item from cart |
| GET | /cart | Get current cart |
| POST | /order | Place order |
| POST | /customer/register | Register customer |

All endpoints return JSON-formatted responses.

---

## Data Persistence

MySQL (or H2 for local testing) is used as the relational database.

Stores:
- Customers
- Restaurants
- Menu items
- Cart
- Orders
- Order items

Data access is handled via Spring Data JPA repositories.

---

## Running the Backend Locally

### Prerequisites
- Java 17 or above
- Gradle
- MySQL (optional)

### Run with Gradle
./gradlew bootRun

### Run with IDE

Run:
OnlineOrderApplication.java

Server starts at:
http://localhost:8080

---

## Docker Deployment

Build and start: 
docker-compose up --build





