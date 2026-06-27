
# 🛍️ Vendilo - Advanced Online Store Platform

[![Java](https://img.shields.io/badge/Java-17%2B-blue.svg)](https://www.java.com)
[![JUnit](https://img.shields.io/badge/JUnit-5.9.2-green.svg)](https://junit.org/junit5/)
[![SQLite](https://img.shields.io/badge/SQLite-3.42.0-lightblue.svg)](https://www.sqlite.org/)

## 📋 Overview

Vendilo is a comprehensive e-commerce platform developed as a university project, simulating a full-featured online marketplace. The system supports multiple user roles including customers, sellers, support agents, and administrators, with sophisticated business logic for order management, payments, and user interactions.

## 🎯 Key Features

### 👥 User Roles
- **Customers**: Browse products, manage cart, place orders, rate products
- **Sellers**: Manage inventory, list products, view sales history  
- **Support Agents**: Handle user requests and seller verifications
- **Administrators**: Manage users, monitor performance, send promotions

### 💰 Core Functionality
- **Product Catalog**: Categorized products (Digital, Books) with detailed attributes
- **Shopping Cart**: Dynamic cart management with address-based shipping
- **Wallet System**: Digital wallet for transactions and seller payouts
- **Discount Codes**: Percentage and fixed-amount discounts
- **Vendilo+ Subscription**: Premium membership with exclusive benefits

### 📱 Advanced Features
- **Notification System**: Real-time updates for orders, stock, and messages
- **Performance Analytics**: Sales reports and seller performance tracking
- **User Management**: Admin controls for user creation, blocking, and role assignment

## 🚀 Installation & Running

### Prerequisites
- Java 17 or higher
- SQLite JDBC driver (included)
- Git (optional)

### Setup Steps

1. **Clone the repository**
```bash
git clone https://github.com/your-username/vendilo.git
cd vendilo
```

2. **Compile all Java source files**
```bash
dir /s /b *.java > sources.txt
javac -cp lib\sqlite-jdbc-3.42.0.0.jar -d out @sources.txt
```

3. **Run the application**
```bash
java -cp "out;lib/sqlite-jdbc-3.42.0.0.jar" ir.ac.kntu.Vendilo
```

### Quick Test (Optional)
The system includes pre-loaded data for testing purposes. Default admin credentials:
```
Username: admin
Password: Admin@123
```


## 📖 Documentation

The system follows object-oriented principles with clear separation of concerns:
- **Data Layer**: SQLite database for persistent storage
- **Business Layer**: Service classes for business logic
- **Presentation Layer**: Console-based interactive menus

## 🤝 Contributing

This is an academic project. For contributions, please ensure:
- Clean code principles are followed
- Unit tests are included for new features
- Conventional commit messages are used

## 📝 License

This project is developed for educational purposes as part of the Advanced Programming course.
