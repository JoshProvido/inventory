# Small Business Inventory Management System
Native PHP 8 + MySQL (PDO) + Bootstrap 5 + Chart.js

## Install (XAMPP)
1. Copy this folder to `C:\xampp\htdocs\inventory`.
2. Start **Apache** and **MySQL** in the XAMPP Control Panel.
3. Open phpMyAdmin → **Import** → choose `database.sql` → Go.
4. Open http://localhost/inventory/setup.php once (creates the users), then **delete setup.php**.
5. Log in at http://localhost/inventory/ — `admin / admin123` or `staff / staff123`. Change these passwords in Users.

If your MySQL has a root password, edit `config.php`.

## Roles
- **Admin**: everything, including Users, Categories and Suppliers (add/edit/delete).
- **Staff**: products, stock transactions, reports; can view (not change) categories and suppliers.

## Notes
- Bootstrap, Bootstrap Icons and Chart.js load from a CDN, so an internet connection is needed for styling and charts.
- Quantities change only through Stock Management so every change is logged.
- A category or supplier that still has products cannot be deleted. Deleting a product also deletes its movement history.
