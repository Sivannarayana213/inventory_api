# 🧩 Inventory Management API

A backend REST API built using **Java (Spring Boot)** and **MySQL** to manage products, customers, and orders for a small inventory system.

---

## 🚀 Tech Stack
- **Java 21**
- **Spring Boot 3.5**
- **Spring Data JPA + Hibernate**
- **MySQL**
- **Lombok**
- **Maven**
- **Postman (for API testing)**

---

## 🏗️ Architecture Overview

- Controllers: handle REST endpoints.  
- Services: core business logic (stock updates, order totals).  
- Repositories: JPA interfaces for DB.  
- DTOs: request/response mapping layer.  
- Exception Handler: clean API error responses.

---

## 📦 Features
✅ Add / view / delete products  
✅ Add / view customers  
✅ Place orders with live stock validation  
✅ Auto-update inventory levels  
✅ Centralized exception handling (400 / 404 / 409)  
✅ Validation on request inputs  

---

## ⚙️ API Endpoints

### 🧱 Product
`POST /api/products` – Add product  
`GET /api/products` – List all  
`GET /api/products/{id}` – Get by ID  
`DELETE /api/products/{id}` – Delete product  

### 👥 Customer
`POST /api/customers` – Add customer  
`GET /api/customers` – List all  
`GET /api/customers/{id}` – Get by ID  

### 🛒 Orders
`POST /api/orders/place` – Place new order  

Example request:
```json
{
  "customerId": 1,
  "items": [
    {"productId": 2, "quantity": 3},
    {"productId": 4, "quantity": 1}
  ]
}

