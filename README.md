# 📝 Simple Blog Web Application (PHP + MySQL)

This is a basic PHP web application that performs **CRUD operations** (Create, Read, Update, Delete) on blog posts with **user authentication** (register, login, logout). The application uses **MySQL** as the database and **sessions** for managing user login states.

---

## 📦 Features

- User Registration and Login with Password Hashing
- Session-based Authentication
- Add, View, Edit, Delete Blog Posts
- Clean, simple codebase for learning purposes

---

## 🛠 Requirements

- PHP 7.4 or higher
- MySQL Server
- Apache or any web server (XAMPP recommended for Windows)
- Web browser

---

## 🗄️ Database Setup

1. Open your MySQL client or phpMyAdmin.
2. Run the following SQL script (in `db.sql`) to create the database and tables:

```sql
CREATE DATABASE blog;

USE blog;

CREATE TABLE users (
    id INT AUTO_INCREMENT PRIMARY KEY,
    username VARCHAR(50) NOT NULL UNIQUE,
    password VARCHAR(255) NOT NULL
);

CREATE TABLE posts (
    id INT AUTO_INCREMENT PRIMARY KEY,
    title VARCHAR(255) NOT NULL,
    content TEXT NOT NULL,
    created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);
