Product Inventory Management System (MERN + MySQL)

A full-stack web application for managing products, categories, stock, and users with role-based access (Admin & Manager).
This system supports creating, updating, deleting, filtering, and searching products, along with image uploads and audit logs.

🚀 Tech Stack

Frontend: React.js, Axios, Bootstrap

Backend: Node.js, Express.js

Database: MySQL (Sequelize ORM)

Auth: JWT (stored in httpOnly cookies)

Uploads: Multer

Roles: Admin & Manager

📌 Features
🔐 Authentication & Roles

Login with email + password

JWT-based secure sessions

Admin: Manage users + products

Manager: Manage only products

📦 Product Management

Add / Edit / Delete products

Product image upload

Search by name/SKU

Filter by category, stock, price

Pagination (10 per page)

Soft delete support

Real-time stock adjustments

🧑‍💻 Admin Features

View all users

Add new manager

Block/unblock users

View audit logs

🗂 Category Management

Add / Edit / Delete categories

🛠 Project Setup Instructions
1️⃣ Backend Setup
1. Open the Backend folder and install dependencies
cd Backend
npm install

2. Configure environment variables

Create .env in Backend:

DB_HOST=127.0.0.1
DB_USER=root
DB_PASS=your_mysql_password
DB_NAME=inventory_db
DB_PORT=3306
JWT_SECRET=mysecretkey
PORT=3001

3. Seed default users (Admin & Manager)
node seed.js


This creates:

Role	Email	Password
Admin	admin@inventory.com
	admin123
Manager	manager@inventory.com
	manager123
4. Start Backend Server
npm run server


Backend will run at:
👉 http://localhost:3001/api/

2️⃣ Frontend Setup
1. Install frontend dependencies
cd Frontend
cd inventory_management_system
npm install

2. Start React App
npm start


Frontend runs at:
👉 http://localhost:3000

📡 API Base URL (Frontend → Backend)

Your Axios instance should use:

const api = axios.create({
  baseURL: "http://localhost:3001/api",
  withCredentials: true
});
