# StartUpTrack: MySQL Business Management System

## 📌 Overview
StartUpTrack is a **MySQL-powered business management system** designed to help small entrepreneurs track **sales, inventory, expenses, and customers**.  
It empowers business owners to make **data-driven decisions** and supports entrepreneurial growth.

---

## 🚀 Features
- Manage products, customers, sales, and expenses.
- Automatic stock updates after sales.
- Daily/weekly sales reports.
- Track profit vs expenses.
- Scalable foundation for web or mobile apps.

---

## 🗄 Database Schema
**Tables:**
- `Users` – entrepreneur login
- `Products` – product details
- `Customers` – customer information
- `Sales` – sales records
- `Expenses` – expenses tracking

---

## 💻 Sample SQL Queries
- Insert a new product:
```sql
INSERT INTO Products (name, category, price, stock_quantity) 
VALUES ('Laptop', 'Electronics', 800, 10);
Daily sales report:

SELECT DATE(date) AS SaleDate, SUM(total_amount) AS DailyRevenue 
FROM Sales 
GROUP BY DATE(date);


Profit vs Expenses:

SELECT 
   (SELECT SUM(total_amount) FROM Sales) - 
   (SELECT SUM(amount) FROM Expenses) AS NetProfit;

👨‍💻 Author

Tesfahun Tewodros
🎓 PLP Software Development Scholarship Learner
🌍 Ethiopia | 💡 Passionate about AI, Data Science & Entrepreneurship
