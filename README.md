🛒 E-Commerce Database Project
1. Project Overview
This project contains the database structure (schema) for a basic E-Commerce System. It is designed to manage the core functions of an online store, ensuring high data integrity and relationship management between entities.

Core Modules:

Users: Customer profiles, authentication, and login credentials.

Products: Catalog management, pricing, and real-time stock levels.

Orders: Historical records of all purchases.

Payments: Detailed transaction tracking for every order.

Goal: To maintain strict data integrity (e.g., ensuring an order cannot exist without a valid user).

2. Database Requirements
To run this project, ensure your environment meets the following specifications:

Database System: MySQL 8.0+ or MariaDB.

Tools: MySQL Workbench (recommended), DBeaver, or phpMyAdmin.

Operating System: Windows, macOS, or Linux.

3. Setup Steps
Follow these steps to deploy the database on your local machine:

Download the Project: Clone this repository or download the ZIP file.

Launch Your SQL Tool: Open MySQL Workbench and connect to your local server.

Open the Script: Navigate to File > Open SQL Script and select e-commerce.sql.

Execute: Click the Lightning Bolt icon to run the script. This will automatically generate the database and all associated tables.

4. SQL Script Execution Order
If you choose to run scripts manually or modify the files, they must be executed in the following order to avoid "Foreign Key Constraint" errors:

Users & Products: These are "Parent" tables and must exist first.

Orders: This depends on the Users table.

OrderItems & Payments: These "Child" tables depend on both Orders and Products.

5. Folder Structure
The repository is organized to help you locate documentation and assets quickly:

Plaintext

📂 e-commerce-db-project
 ├── 📄 e-commerce.sql        # The main script to build the database
 ├── 📂 documentation
 │    ├── 📄 data_dictionary.md  # Detailed info on every column and rule
 │    └── 🖼️ er_diagram.png      # Visual map of table relationships
 ├── 📜 CHANGELOG.md          # A diary of updates made to the project
 └── 📘 README.md             # This file (Project instructions)
6. Project Assumptions
To keep the design clean and beginner-friendly, the following logic was applied:

Currency: All prices use the DECIMAL format (e.g., 10.99) rather than FLOAT to ensure mathematical accuracy for financial reports.

Security: The password column supports up to 255 characters to accommodate modern "hashed" (encrypted) strings.

Data Cleanup: We utilize ON DELETE CASCADE. If a user profile is deleted, their specific order history is automatically removed to prevent "orphan" records.
