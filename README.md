# 🍽️ Restaurant Management System – SQL Project

## 📌 Overview

This project demonstrates a **Restaurant Management System** built using SQL. It is designed to handle and automate key daily operations in a restaurant, such as managing reservations, orders, menu items, employees, and payments.

The system uses a structured relational database with multiple interconnected tables and leverages SQL features like **joins**, **subqueries** and **views**, to improve operational efficiency.

---

## 🎯 Objectives

- Manage customers, orders, tables, and employees efficiently
- Track menu item popularity and sales
- Automate status updates and payments using triggers
- Generate useful business insights with SQL queries

---

## 🧱 Database Tables

- `Customers` – Stores customer information
- `Tables` – Manages seating and reservation status
- `MenuItems` – Menu details with pricing
- `Employees` – Staff names, roles, and shifts
- `Orders` – Tracks order details
- `OrderItems` – Connects orders to specific menu items
- `Reservations` – Booking information
- `Payments` – Transaction records

---

## 🔍 Key SQL Features

### 🔁 Subqueries

- **Customers who ordered the most expensive item**
- **Menu items ordered more than once**
- **Customers with high-value orders**

### 🔗 Joins

- **INNER JOIN:** Orders with customer and table details  
- **JOIN with filter:** Reservations on reserved tables  
- **LEFT JOIN:** Menu items that have been ordered  

### 👓 Views

- **CustomerOrderSummary:** Summarizes order details per customer
- **PopularItems:** Menu items ordered more than once
- **EmployeeShiftView:** Overview of employees sorted by shift

---

## 📊 Sample Queries

```sql
-- Find customers who ordered the most expensive item
SELECT Customers.name, Orders.order_id, Orders.total_price
FROM Customers, Orders, OrderItems
WHERE Customers.customer_id = Orders.customer_id
  AND Orders.order_id = OrderItems.order_id
  AND OrderItems.item_id = (
    SELECT item_id FROM MenuItems WHERE price = (SELECT MAX(price) FROM MenuItems)
)
ORDER BY Orders.total_price DESC;
Here is a complete `README.md` documentation file for your **Restaurant Management System SQL Project**, based on the PDF you provided:

---

````markdown
# 🍽️ Restaurant Management System – SQL Project

## 📌 Overview

This project demonstrates a **Restaurant Management System** built using SQL. It is designed to handle and automate key daily operations in a restaurant, such as managing reservations, orders, menu items, employees, and payments.

The system uses a structured relational database with multiple interconnected tables and leverages SQL features like **joins**, **subqueries**, **views**, **stored procedures**, and **triggers** to improve operational efficiency.

---

## 🎯 Objectives

- Manage customers, orders, tables, and employees efficiently
- Track menu item popularity and sales
- Automate status updates and payments using triggers
- Generate useful business insights with SQL queries

---

## 🧱 Database Tables

- `Customers` – Stores customer information
- `Tables` – Manages seating and reservation status
- `MenuItems` – Menu details with pricing
- `Employees` – Staff names, roles, and shifts
- `Orders` – Tracks order details
- `OrderItems` – Connects orders to specific menu items
- `Reservations` – Booking information
- `Payments` – Transaction records

---

## 🔍 Key SQL Features

### 🔁 Subqueries

- **Customers who ordered the most expensive item**
- **Menu items ordered more than once**
- **Customers with high-value orders**

### 🔗 Joins

- **INNER JOIN:** Orders with customer and table details  
- **JOIN with filter:** Reservations on reserved tables  
- **LEFT JOIN:** Menu items that have been ordered  

### 👓 Views

- **CustomerOrderSummary:** Summarizes order details per customer
- **PopularItems:** Menu items ordered more than once
- **EmployeeShiftView:** Overview of employees sorted by shift

---

## 📊 Sample Queries

```sql
-- Find customers who ordered the most expensive item
SELECT Customers.name, Orders.order_id, Orders.total_price
FROM Customers, Orders, OrderItems
WHERE Customers.customer_id = Orders.customer_id
  AND Orders.order_id = OrderItems.order_id
  AND OrderItems.item_id = (
    SELECT item_id FROM MenuItems WHERE price = (SELECT MAX(price) FROM MenuItems)
)
ORDER BY Orders.total_price DESC;


```sql
-- Create view: Popular Menu Items
CREATE OR REPLACE VIEW PopularItems AS
SELECT MenuItems.name, COUNT(OrderItems.item_id) AS times_ordered
FROM MenuItems
JOIN OrderItems ON MenuItems.item_id = OrderItems.item_id
GROUP BY MenuItems.name
HAVING COUNT(OrderItems.item_id) > 1;
```



## ✅ Project Highlights

* 📌 Tracks most and least popular dishes
* 🧾 Summarizes high-spending customers
* 💳 Automates payment and table status updates
* 👨‍🍳 Organizes employee roles and schedules

---

## 📘 Conclusion

This project showcases how SQL can be used to:

* Structure and manage restaurant data effectively
* Derive actionable business insights using queries
* Automate operational workflows using views and triggers


