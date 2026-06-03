# Simplified E-Commerce Platform
**Stack:** Java 17 / Spring Boot 3.2 | ReactJS 18 | H2 In-Memory Database | JPA

---

## Project Structure
```
ecommerce/
├── store/                  ← Spring Boot Backend (port 8080)
│   ├── pom.xml
│   └── src/main/
│       ├── java/com/ecommerce/store/
│       │   ├── StoreApplication.java
│       │   ├── model/Product.java
│       │   ├── repository/ProductRepository.java
│       │   ├── controller/ProductController.java
│       │   └── config/
│       │       ├── DataSeeder.java
│       │       └── CorsConfig.java
│       └── resources/application.properties
│
└── store-frontend/         ← React Frontend (port 3000)
    ├── package.json
    └── src/
        ├── App.js
        ├── index.js
        ├── components/Navbar.jsx
        └── pages/
            ├── PLP.jsx
            └── PDP.jsx
```

---

## Running the App

### 1. Start the Backend
```bash
cd store
mvn spring-boot:run
```
Backend runs at: http://localhost:8080

Test endpoints:
- http://localhost:8080/api/products
- http://localhost:8080/api/products/1
- http://localhost:8080/h2-console  (JDBC URL: jdbc:h2:mem:storedb)

### 2. Start the Frontend
```bash
cd store-frontend
npm install
npm start
```
Frontend runs at: http://localhost:3000

---

## Features
- Product Listing Page (PLP) with category filter tabs
- Product Detail Page (PDP) with full product info
- Add to Cart with live navbar badge counter
- H2 in-memory database auto-seeded with 5 products on startup
- CORS configured for frontend ↔ backend communication
