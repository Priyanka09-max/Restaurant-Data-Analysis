# 🍽️ Restaurant Data Analysis – SQL Project

This project focuses on analyzing restaurant operations using **SQL**. It explores various aspects such as customer behavior, order trends, popular menu items, and employee shift patterns through efficient data queries and database design.

---

## 📌 Project Objective

To build and analyze a restaurant database using SQL that supports:

- Customer management  
- Table reservations and status tracking  
- Menu item management  
- Order processing  
- Employee scheduling  
- Payment tracking  
- Generating meaningful insights through SQL queries and views

---

## 🗂️ Database Structure

The database consists of the following core tables:

- `Customers` – Stores customer details
- `Tables` – Tracks seating and table status
- `MenuItems` – Menu items with pricing
- `Employees` – Employee names, roles, and shifts
- `Orders` – Order summary (total price, customer, table)
- `OrderItems` – Line-level order details
- `Reservations` – Booking information
- `Payments` – Payment history per order

An **ER Diagram** was created to visualize the relationships between these entities.

---

## 🔍 SQL Features Used

### 📄 Subqueries

- **Most expensive item ordered**
- **Popular menu items** (ordered more than once)
- **High-value customers** (orders greater than average)

### 🔗 Joins

- **INNER JOIN** to show orders with customer names and tables
- **Reservations with customer names** and table status
- **LEFT JOIN** to list ordered menu items only

### 👁️ Views

- `CustomerOrderSummary` – Orders by each customer with totals
- `PopularItems` – Menu items ordered more than once
- `EmployeeShiftView` – Employee names sorted by shift time

---

## 📊 Sample Insights

- Identify **top-spending customers**
- Find **frequently ordered dishes**
- Analyze **employee shift scheduling**
- Track **reserved tables and occupancy**
- Monitor **order values and trends**

---

## ⚙️ Technologies Used

- **MySQL 
- ER diagram




