# Bank-Management-System-Flask-Web-App


#  Bank Management Web Application

A web-based banking system built with Flask, **SQLAlchemy, and MySQL, developed as part of a database design project. This application simulates a simple banking environment that allows users to view customer accounts, loans, and transactions through a clean interface.

##  Project Overview

This Flask project supports:

- Viewing all customer account details
- Accessing loaninformation for each customer
- Filtering transaction history based on account number
- Managing backend operations with relational database schemas
- Frontend rendering using HTML + Jinja templates

The app connects to a MySQL database using PyMySQL and uses SQLAlchemy ORM for mapping database tables to Python classes.

##  Tech Stack

- Frontend: HTML, CSS, Jinja2 (template rendering)
- Backend: Python (Flask Framework)
- Database: MySQL
- ORM: SQLAlchemy
- DB Connector: PyMySQL

##  Key Functionalities

### 1. Accounts Page
- Route: `/accounts`
- Function: Displays a list of all accounts
- Query: `Account.query.all()`

### 2. Loans Page
- Route: `/loans`
- Function: Displays a list of all loans
- Query: `Loan.query.all()`

### 3. Transactions Page
- Route: `/transactions/<account_id>`
- Function: Shows all transactions linked to a specific account
- Query: `Transaction.query.filter_by(account_number=account_id).all()`

##  Setup Instructions

1. Clone the Repository
   ```bash
   git clone https://github.com/your-username/flaskProject.git
   cd flaskProject
   ```

2. Create Virtual Environment
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3.Install Dependencies
   ```bash
   pip install -r requirements.txt
   ```

4. Configure Database Connection
   In your config or `.env` file:
   ```python
   SQLALCHEMY_DATABASE_URI = 'mysql+pymysql://username:password@localhost/bankdb'
   SQLALCHEMY_TRACK_MODIFICATIONS = False
  

5. **Run the Application**
   bash
   flask run
   
   

## Learning Outcomes

- Normalization up to 3NF with relational schema design
- One-to-many relationships implemented (e.g., one bank → many branches)
- Use of nested queries, `GROUP BY`, and `HAVING` in SQL
- Modular Flask structure for scalable design
- Environment variable-based configuration for credentials


