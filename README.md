# ATM Application (Using Flask Project)

This is a simple **ATM Application** built using Python's Flask framework and a MySQL database (via PyMySQL). It simulates basic ATM functionalities including:
- Cash Withdrawal
- Cash Deposit
- Mini Statement View
- PIN Generation

---

## 🛠️ Tech Stack

- **Backend**: Python (Flask)
- **Frontend**: HTML (with Jinja templates)
- **Database**: MySQL (accessed via PyMySQL)

---

## 📂 Folder Structure

ATM-Application/
│
├── templates/ # HTML Templates
│ ├── home.html
│ ├── withdraw1.html
│ ├── withdraw2.html
│ ├── deposit1.html
│ ├── ministatement1.html
│ ├── ministatement2.html
│ ├── pingeneration1.html
│ ├── pingeneration2.html
│
├── app.py # Main Flask application
├── README.md # This file

---

## 🚀 Features

### 🏦 Withdraw
- Validate account and PIN
- Deduct amount from balance

### 💰 Deposit
- Accept deposits into a valid account

### 📋 Mini Statement
- View account balance and details after PIN verification

### 🔐 PIN Generation
- Set a new PIN for accounts without a PIN

---

## 🔧 Prerequisites

- Python 3.x
- MySQL Server
- Python packages:
  - Flask
  - PyMySQL

## Install dependencies using:

pip install flask pymysql

## 🗃️ MySQL Database Setup
Create a database named ATM and a table named ACCOUNTS using the following sample structure:

CREATE DATABASE ATM;

USE ATM;

CREATE TABLE ACCOUNTS (
    USER_ID INT AUTO_INCREMENT PRIMARY KEY,
    USER_NAME VARCHAR(100),
    USER_EMAIL VARCHAR(100),
    USER_ACCNO VARCHAR(20) UNIQUE,
    USER_PIN INT,
    USER_BALANCE INT
);

## Add some sample data:

INSERT INTO ACCOUNTS (USER_NAME, USER_EMAIL, USER_ACCNO, USER_BALANCE)
VALUES ('Alice', 'alice@example.com', '12345678', 5000);

## ▶️ Running the Application
Run the application with:
python app.py
By default, it will run on http://localhost:5016

## 🧠 Notes
Make sure your MySQL server is running and accessible.
Database credentials are stored in db_config inside app.py.

## 🤝 Contributing
Feel free to fork this repo and submit pull requests. Any contributions to improve the UI or code structure are welcome!

## 📄 License
This project is licensed under the MIT License.
