# Boutique-Application

A full-stack boutique (e-commerce) web application built using **React.js (Frontend)** and **Spring Boot (Backend)**.
The application allows customers to browse products, manage carts, place orders, and enables admin-level product management.

---

## 🚀 Features

### 👤 Customer Features

* Browse products by category
* Search products by name/description
* View featured and sale products
* Add to cart and manage quantities
* Place orders with shipping details
* View order history

---

### 🛒 Cart Management (React Context API)

* Add / Remove items
* Update quantity dynamically
* Auto calculation of total price
* Clear cart functionality

---

### 🔐 Admin Features

* Admin login (role-based UI control)
* Add / Update / Delete products
* Manage stock & sale status
* View analytics (best-selling products, revenue)

---

## 🏗️ Architecture

```
Frontend (React)
   ├── Components (Cart, Admin, Product UI)
   ├── Context API (Cart + Admin State)
   └── API Layer (Fetch)

          ↓ REST API

Backend (Spring Boot)
   ├── Controller Layer (REST APIs)
   ├── Service Layer (Business Logic)
   ├── Repository Layer (JPA)
   └── Exception Handling (Global)

          ↓

Database (MySQL)
```

---

## 🧩 Backend Design

### 📦 Entities

* Customer
* Product
* Order
* OrderItem

### 🔗 Relationships

* One Customer → Many Orders
* One Order → Many OrderItems
* One Product → Referenced in OrderItems

---

## ⚙️ Key Backend Features

* UUID-based primary keys
* DTO + Mapper pattern for clean API responses
* Global Exception Handling (`@RestControllerAdvice`)
* Validation using `jakarta.validation`
* Custom queries using JPQL
* Order total calculation using `BigDecimal`
* Analytics:

  * Total revenue calculation
  * Best-selling products
  * Order filtering (date range, status)

---

## 🔒 Security

* Spring Security configured
* CORS enabled for deployed frontend
* API endpoints currently public (can be extended with JWT)

---

## 📡 API Endpoints

### 🛍️ Product APIs

* `GET /api/products`
* `GET /api/products/{id}`
* `GET /api/products/category/{category}`
* `GET /api/products/search?q=`
* `GET /api/products/sale`
* `GET /api/products/featured`
* `PATCH /api/products/{id}/stock`
* `PATCH /api/products/{id}/sale`

---

### 👤 Customer APIs

* `GET /api/customers`
* `POST /api/customers`
* `PUT /api/customers/{id}`
* `DELETE /api/customers/{id}`

---

### 📦 Order APIs

* `GET /api/orders`
* `POST /api/orders`
* `GET /api/orders/date-range`
* Order item management APIs

---

## 🎨 Frontend Structure

```
src/
 ├── api/           # API calls
 ├── components/    # UI Components
 ├── pages/         # Page-level components
 ├── context/       # Cart & Admin Context
 └── App.js         # Main routing
```

---

## 🛠️ Tech Stack

### Frontend

* React.js
* Context API
* Fetch API
* CSS

### Backend

* Spring Boot
* Spring Data JPA
* Spring Security
* Hibernate

### Database

* MySQL

### Tools

* Git & GitHub
* Postman
* IntelliJ / VS Code

---

## ⚡ Highlights

* Clean layered architecture
* Real-world e-commerce flow
* State management using Context API
* Backend validations + exception handling
* Optimized queries and analytics
* Deployed full-stack application

---

## 🔮 Future Enhancements

* JWT Authentication
* Payment Gateway Integration
* Image Upload (Cloud Storage)
* Microservices Architecture
* Redis Caching

---

## 👨‍💻 Author

**Sushant Rokade**
B.Tech IT | Java Full Stack Developer

---

## ⭐ Conclusion

This project demonstrates strong understanding of:

* Full-stack development
* REST API design
* Backend architecture
* State management in React
* Real-world system design

---
