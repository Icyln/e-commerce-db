# 🛒 E-Commerce Database Project

## 1. Project Overview
This project contains the database structure (schema) for a basic **E-Commerce System**. It is designed to manage the core functions of an online store, ensuring high data integrity and relationship management between entities.

### Core Modules:
* **Users:** Customer profiles, authentication, and login credentials.
* **Products:** Catalog management, pricing, and real-time stock levels.
* **Orders:** Historical records of all purchases.
* **Payments:** Detailed transaction tracking for every order.

> **Goal:** To maintain strict data integrity (e.g., ensuring an order cannot exist without a valid user).

---

## 2. Database Requirements
To run this project, ensure your environment meets the following specifications:

* **Database System:** MySQL 8.0+ or MariaDB.
* **Tools:** [MySQL Workbench](https://www.mysql.com/products/workbench/) (recommended), DBeaver, or phpMyAdmin.
* **Operating System:** Windows, macOS, or Linux.

---

## 3. Setup Steps
Follow these steps to deploy the database on your local machine:

1.  **Download the Project:** Clone this repository or download the ZIP file.
2.  **Launch Your SQL Tool:** Open MySQL Workbench and connect to your local server.
3.  **Open the Script:** Navigate to `File > Open SQL Script` and select `e-commerce.sql`.
4.  **Execute:** Click the **Lightning Bolt icon** to run the script. This will create the database and all tables.

---

## 4. SQL Script Execution Order
If you choose to run scripts manually, they **must** be executed in this order to avoid "Foreign Key" errors:

1.  **Users & Products:** (Parent tables)
2.  **Orders:** (Depends on Users)
3.  **OrderItems & Payments:** (Depend on Orders and Products)

---

## 5. Folder Structure
```plaintext
📂 e-commerce-db-project
 ├── 📄 e-commerce.sql        # Main script to build the database
 ├── 📂 documentation
 │    ├── 📄 data_dictionary.md  # Detailed info on columns
 │    └── 🖼️ er_diagram.png      # Visual map of relationships
 ├── 📜 CHANGELOG.md          # Diary of updates
 └── 📘 README.md             # This file
