# 🛒 Newark Online Computer Store (NOCS)

## 📌 Project Overview
**Newark Online Computer Store (NOCS)** is an e-commerce platform designed to provide customers with a seamless shopping experience for computer-related products. Built as part of **CS631-007: Database Management Systems Design**, this project focuses on **database implementation, front-end and back-end development, security, and scalability**.

## 🚀 Features
### 🔹 User Features
- User registration and authentication 🔐
- Browse and search computer hardware and accessories 💻
- Add/remove items from the shopping cart 🛍️
- Secure payment processing 💳
- Order history and tracking 📦

### 🔹 Admin Features
- Product management (add, update, delete) 🏷️
- Order and transaction tracking 📊
- Customer data management 👥
- Sales analytics and reporting 📈

---

## 🏗️ Tech Stack
### 🔹 Front-End
- **HTML, CSS, JavaScript**
- **Responsive UI design** for multi-device support 📱💻

### 🔹 Back-End
- **PHP** for handling server-side logic
- **SQL (MySQL/PostgreSQL)** for database management
- **Node.js** (Optional for API integration)

### 🔹 Security & Optimization
- **SSL/TLS encryption** for secure transactions 🔒
- **SQL Injection Protection**
- **Scalable database architecture**

---

## 📊 Database Structure
- **Customers** (ID, Name, Email, Address, Phone, Credit Card Info)
- **Products** (ID, Name, Description, Price, Stock Quantity, Category)
- **Orders** (Order ID, Customer ID, Date, Total Amount, Payment Method)
- **Transactions** (Transaction ID, Order ID, Status, Payment Details)
- **Shopping Cart** (Customer ID, Product ID, Quantity)

---

## 🛠️ Setup Instructions
### 🔹 Prerequisites
Ensure you have the following installed:
- **PHP & MySQL** for backend processing
- **Apache/Nginx Server**
- **Browser (Chrome/Firefox)**

### 🔹 Installation Steps
1. **Clone the repository:**
   ```bash
   git clone https://github.com/ananya-jaikumar/DMSD_Project.git
   cd DMSD_Project
   ```
2. **Setup the Database:**
   - Import `database.sql` into MySQL
3. **Run the Server:**
   - Start Apache/Nginx and ensure PHP is running
4. **Access the Application:**
   - Open browser and navigate to `http://localhost/NOCS`

---

## 📌 SQL Queries for Analysis
- **Total amount charged per credit card**
  ```sql
  SELECT CCNumber, ROUND(SUM(Quantity * PriceSold),2) AS Total FROM transactions GROUP BY CCNumber ORDER BY Total DESC;
  ```
- **Top 10 customers by spending**
  ```sql
  SELECT CustomerID, SUM(TotalAmount) AS Spent FROM orders GROUP BY CustomerID ORDER BY Spent DESC LIMIT 10;
  ```
- **Most frequently sold products in a given time period**
  ```sql
  SELECT ProductID, COUNT(*) AS Sales FROM transactions WHERE Date BETWEEN '2023-01-01' AND '2023-12-31' GROUP BY ProductID ORDER BY Sales DESC;
  ```

---

## 📢 Future Enhancements
✅ Add AI-powered product recommendations 🧠
✅ Implement **REST API** for third-party integrations 🔗
✅ Enable **multi-currency and multilingual support** 🌍
✅ Deploy to cloud-based platforms like **AWS/GCP** ☁️

---

💡 Contributions are welcome! Feel free to fork and submit pull requests! 🚀

