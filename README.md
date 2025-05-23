
# 🛠️ User Management API

This project is a robust **RESTful API** for user management, developed using **Node.js** with the **Express** framework and **MongoDB** as the database. It offers complete CRUD operations along with authentication functionalities.

---

## 🚀 Features

- Create a user
- Authenticate (login) a user
- List all users
- Update user information
- Delete a user
- Token-based authentication

---

## 📦 Technologies Used

- **MongoDB** + **Mongoose** for data persistence and schema modeling
- **Nodemon** for automatic server restart during development
- **Dotenv** for secure environment variable management
- **Bcrypt** for password hashing and enhanced security
- **JsonWebToken (JWT)** for authentication and authorization
- **Visual Studio Code** as the development environment

---

## 🧪 How to Use

### 📍 Register a User

**Endpoint:** `POST http://localhost:3000/register`  
**Request Body (JSON):**
```json
{
  "name": "Thiago",
  "email": "test@gmail.com",
  "password": "4002",
  "confirmpassword": "4002",
  "birthdate": "2004-03-01"
}
```

---

### 🔐 Authenticate a User

**Endpoint:** `POST http://localhost:3000/authenticate`  
**Request Body (JSON):**
```json
{
  "email": "test@gmail.com",
  "password": "4002"
}
```

---

### 👥 List Users

**Endpoint:** `GET http://localhost:3000/users`  
Optional pagination:  
`GET http://localhost:3000/users?limit=2&offset=0`

---

### ✏️ Update a User

**Endpoint:** `PUT http://localhost:3000/user/{id}`  
Replace `{id}` with the actual user ID.

**Request Body (JSON):**
```json
{
  "name": "Thiago",
  "email": "newemail@gmail.com",
  "oldpassword": "4002",
  "password": "1234",
  "birthdate": "2004-03-01"
}
```

---

### ❌ Delete a User

**Endpoint:** `DELETE http://localhost:3000/user/{id}`  
Replace `{id}` with the user ID to be deleted.

---

## 🔐 Security Notes

Each user receives a **JWT token** upon authentication to secure their session and prevent unauthorized access to update or delete actions.

---

## 📄 License

This project is licensed under the **MIT License**. You are free to use, modify, and distribute it.

---
