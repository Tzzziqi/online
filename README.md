# Online Order Backend Service

OnlineOrder is a Spring Boot backend for a food ordering platform similar to Uber Eats or DoorDash.  
It provides RESTful APIs for restaurant browsing, menu management, shopping cart operations, and order processing.

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

## Features
- Browse restaurants and menus
- Add/remove items from cart
- Checkout and place orders
- Customer registration

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

## Run Locally

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





