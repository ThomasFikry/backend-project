# Gym Supplements Store Backend

## 📌 Overview
This is the backend for a Gym Supplements Store project.  
It includes:
- **Authentication Module** (User Signup/Login + JWT Tokens + Role-based Access)
- **Products Module** (CRUD operations for supplements)

Built with:
- **Node.js**
- **Express.js**
- **MongoDB + Mongoose**
- **bcryptjs** (Password Hashing)
- **jsonwebtoken** (JWT Authentication)

---

## 👥 User Roles
- **Admin** → Can create, update, delete products
- **Customer** → Can view products, but cannot create/update/delete

---

## 📦 Routes

### 1️⃣ Authentication
| Method | Endpoint       | Description |
|--------|---------------|-------------|
| POST   | `/api/auth/signup` | Register a new user & get a token |
| POST   | `/api/auth/login`  | Login & get a token |

---

### 2️⃣ Products
| Method | Endpoint                | Description |
|--------|-------------------------|-------------|
| POST   | `/api/products`         | Create a new product (**Admin only**) |
| GET    | `/api/products`         | Get all products |
| GET    | `/api/products/:id`     | Get product by ID |
| PATCH  | `/api/products/:id`     | Update product (**Admin only**) |
| DELETE | `/api/products/:id`     | Delete product (**Admin only**) |

---

## 🔐 Protected Routes
- Admin-only routes require:
  1. A valid JWT token in the `Authorization` header:  
     ```
     Authorization: Bearer <your_token>
     ```
  2. User role must be `"admin"`.

---

## 🗄️ Project Structure
