# **Bank Management System (Python + MySQL)**

A command-line based **Bank Management System** built using **Python** and **MySQL**, allowing users to create accounts, log in, perform transactions, check balances, report issues, verify KYC status, and more.

This project uses:

* **main.py** for menu navigation and overall program flow 
* **login_register.py** for account creation and user authentication 
* **basic_features.py** for all banking operations (deposit, withdraw, transfer, KYC checks, etc.) 
* **requirements.txt** for database setup instructions 

---

## **📌 Features**

### **User Account Management**

* Create a new bank account
* Secure login using account number + PIN
* Auto-generated unique account number

### **Banking Operations**

* Deposit money
* Withdraw money
* Transfer funds to another account
* Real-time balance check
* View last 100 transactions

### **Advanced Features**

* Check loan eligibility based on:

  * Account age
  * Balance
  * Recent transactions
* Report wrongful transactions
* Update account details (address, email, phone, etc.)
* Check KYC verification status

---

## **📂 Project Structure**

```
├── main.py                # Main menu control flow
├── login_register.py      # Login and registration logic
├── basic_features.py      # Core banking operations
├── requirements.txt       # Setup instructions & SQL schema
```

---

## **🔧 Installation & Setup**

### **1. Install Python dependencies**

```
pip install mysql.connector
```

### **2. MySQL Database Setup**

Use the SQL commands provided in `requirements.txt` :

* Create database
* Create tables:

  * `accounts`
  * `kyc`
  * `transactions`
  * `wrongful_reports`

Ensure MySQL credentials in your Python files match your system:

```python
mysql.connect(host="localhost", user="root", password="YOUR_PASSWORD", database="bank_management_cse")
```

---

## **▶️ Running the Project**

Once the database and tables are created:

```bash
python main.py
```

Program Flow:

1. Create an account **or** login
2. Access the Home Menu
3. Perform banking operations

---

## **📘 How It Works**

### **Login & Registration**

`login_register.py` handles account creation and authentication.
New users receive an auto-generated account number. 

### **Core Banking Functions**

`basic_features.py` includes:

* `deposit()`
* `withdraw()`
* `transfer_funds()`
* `check_balance()`
* `view_transaction_history()`
* `check_loan_eligibility()`
* KYC & account detail updates


### **Menu Navigation**

`main.py` provides structured menus for user interaction.


---

## **⚠️ Important Notes**

* Do **not** rename database tables or columns — doing so will break the code.
* KYC status must be `"Verified"` or `"Unverified"` only.
* Perform at least 2–3 transactions to see meaningful history.
* Ensure MySQL is running before executing Python scripts.

---

AUTHOR : ADITYA RAJ
          VIT
