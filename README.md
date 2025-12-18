🛒 E-Commerce Database Project
1. Project Overview
This project contains the database structure (schema) for a basic E-Commerce System. It is designed to manage the core parts of an online store, including:

Users: Managing customer profiles and login info.

Products: Tracking the catalog, prices, and stock levels.

Orders: Recording purchases made by users.

Payments: Tracking transaction details for every order.

The goal of this database is to ensure data integrity—for example, making sure an order cannot exist without a valid user.

2. Database Requirements
To run this project, you will need the following installed on your computer:

Database System: MySQL 8.0+ or MariaDB.

Tool: MySQL Workbench (recommended) or any SQL editor (like phpMyAdmin or DBeaver).

Operating System: Windows, macOS, or Linux.

3. Setup Steps
Follow these steps to get the database running on your local machine:

Download the Project: Clone or download this repository to your computer.

Open your SQL Tool: Launch MySQL Workbench and connect to your local server.

Open the Script: Go to File > Open SQL Script and select e-commerce.sql.

Execute: Click the "Lightning Bolt" icon to run the script. This will create the database and all necessary tables.

4. SQL Script Execution Order
If you choose to run scripts manually or break them into smaller files, they must be run in this order to avoid "Foreign Key" errors:

Users & Products: These are "Parent" tables and must be created first.

Orders: This depends on the Users table.

OrderItems & Payments: These are "Child" tables that depend on Orders and Products.

5. Folder Structure
The project is organized simply so you can find what you need quickly:

Plaintext

📂 e-commerce-db-project
 ├── 📄 e-commerce.sql        # The main script to build the database
 ├── 📂 documentation
 │    ├── 📄 data_dictionary.md  # Detailed info on every column and rule
 │    └── 🖼️ er_diagram.png      # Visual map of table relationships
 ├── 📜 CHANGELOG.md          # A diary of updates made to the project
 └── 📘 README.md             # This file (Project instructions)

 
6. Project Assumptions
To keep this example beginner-friendly, we made a few design choices:
Currency: All prices are stored in DECIMAL format to ensure accuracy (e.g., $10.99).
Security: The password column is set to 255 characters to allow for "hashed" (encrypted) passwords.
Deletion: We use ON DELETE CASCADE. This means if a user is deleted, all of their order history is automatically removed to keep the database clean.
