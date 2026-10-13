# 📦 Inventory Management System

A Python-based inventory management application built using **Object-Oriented Programming (OOP)**, custom exception handling, and CSV file storage.

![Python](https://img.shields.io/badge/Python-3.10%2B-blue?logo=python)
![Storage](https://img.shields.io/badge/Storage-CSV-orange)
![Project](https://img.shields.io/badge/Project-Internship-success)

## 🌟 Project Overview

The **Inventory Management System** helps users manage product records, track stock quantities, update prices, and calculate inventory value.

The application supports standard products and perishable products with expiry dates. It saves inventory records in a CSV file and loads saved records when the application starts.

This project demonstrates practical Python programming skills and fundamental software development concepts.

## ✨ Features

- ➕ Add standard products.
- 🥫 Add perishable products with expiry dates.
- 🔎 Search products using their unique IDs.
- 📦 Increase or decrease stock quantities.
- 💰 Update product prices.
- 🗑️ Delete products from inventory.
- 📊 Generate a complete inventory report.
- 🚨 Identify products with 10 or fewer units.
- 🧮 Calculate the value of each product and displayed inventory.
- 💾 Save and load records using CSV files.
- 🛡️ Handle duplicate IDs, missing products, invalid prices, and insufficient stock.

## 🧰 Technologies Used

| Technology | Purpose |
|---|---|
| Python | Main programming language |
| `csv` | Read and write inventory records |
| `os` | Handle file paths and check file existence |
| `abc` | Create an abstract base class |
| OOP | Organize classes and product operations |
| CSV | Store inventory data persistently |

**Requirements:** Python 3.10 or later is recommended. No external packages are required.

## 🗂️ Project Structure

```text
Inventory-Management-System/
├── inventory_management.py
├── inventory.csv
└── README.md
```

- `inventory_management.py` — main Python application.
- `inventory.csv` — inventory records created when data is saved.
- `README.md` — project documentation.

*Replace `inventory_management.py` with your actual Python script filename if it differs.*

## ⚙️ Installation and Setup

### Step 1: Install Python

Install Python 3.10 or later from [python.org](https://www.python.org/downloads/).

### Step 2: Open the project folder

Open the folder containing your Python script in VS Code or a terminal.

### Step 3: Run the program

```bash
python inventory_management.py
```

If your system uses the `python3` command, run:

```bash
python3 inventory_management.py
```

## 🖥️ Menu Options

The application provides the following menu:

| Option | Function |
|---|---|
| 1 | Add Standard Product |
| 2 | Add Perishable Product |
| 3 | Search Product |
| 4 | Adjust Stock Quantity |
| 5 | Update Product Price |
| 6 | Delete Product |
| 7 | Display Inventory Report |
| 8 | Display Low Stock Alert |
| 9 | Save Records |
| 10 | Save and Exit |

Follow the prompts to enter product details and manage your inventory.

## 🧮 Inventory Valuation

The system calculates product value using this formula:

**Product Value = Unit Price × Stock Quantity**

For example, if a product costs ₹50 per unit and 20 units are available:

```text
Product Value = ₹50 × 20
              = ₹1,000
```

The inventory report displays product details and calculates the combined value of the products included in that report.

## 🧱 Object-Oriented Programming Concepts

### 1. Abstraction
The abstract `Item` class defines the common structure for inventory items through `calculate_value()` and `get_details()`.

### 2. Inheritance
- `Product` inherits from `Item`.
- `PerishableProduct` inherits from `Product`.

This allows perishable products to reuse standard product functionality.

### 3. Encapsulation
Properties and methods control access to product details, prices, quantities, and expiry dates.

### 4. Polymorphism
The `get_details()` method is implemented differently by `Product` and `PerishableProduct`.

### 5. Custom Exception Handling
The program defines specific exceptions:

- `ProductNotFoundError`
- `DuplicateProductError`
- `InvalidStockError`

These exceptions help handle common inventory errors.

## 💾 CSV Data Storage

The application stores records in `inventory.csv` using these columns:

```text
type,item_id,name,category,price,quantity,expiry_date
```

| Column | Description |
|---|---|
| `type` | Standard or perishable product |
| `item_id` | Unique product identifier |
| `name` | Product name |
| `category` | Product category |
| `price` | Unit price |
| `quantity` | Current stock quantity |
| `expiry_date` | Expiry date for perishable products |

The program loads records at startup. Select **Save Records** or **Save & Exit** to save your latest changes.

**Important:** Changes are not automatically saved after every operation. Save your records before closing the application.

## 🧪 Suggested Test Cases

| Test case | Expected result |
|---|---|
| Add a product with a new ID | Product is added |
| Add a duplicate product ID | Duplicate-product error |
| Search for an unknown ID | Product-not-found error |
| Enter a price of zero or less | Invalid-price error |
| Reduce stock below zero | Stock adjustment is rejected |
| Display the full inventory | Product details and valuation appear |
| Save and restart the application | Saved records are loaded |
| Add a perishable product | Expiry date appears in product details |

## 🚀 Future Enhancements

The project could be improved by adding:

- 📅 Expiry-date validation and expiry alerts.
- 🔐 Login and user authentication.
- 📈 Charts for inventory value and stock levels.
- 🔍 Search by product name or category.
- 📤 Excel or PDF report export.
- 🧾 Stock transaction history.
- 🖥️ A graphical user interface.
- 🧪 Automated unit tests.
- 🗃️ Database integration using SQLite or MySQL.

## 🎓 Learning Outcomes

This project provides practice in:

- Python classes and objects.
- Abstract classes and inheritance.
- Encapsulation and polymorphism.
- Custom exceptions and error handling.
- CSV file operations.
- Input validation.
- Menu-driven application development.
- Basic inventory calculations and reporting.

## 👨‍💻 Author

**Your Name**  
Python / Machine Learning Intern

Update this section with your name, internship organization if appropriate, and GitHub profile before publishing.

## 📄 License

This project is intended for educational and internship-learning purposes. Add a suitable license if you plan to distribute it publicly.

---

⭐ **If you find this project useful, consider starring the repository!**

Made with 🐍 Python and a passion for learning.
