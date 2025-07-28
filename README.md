# Meet-Lathiya


#  BudgetBuddy+ - Smart Monthly Expense Tracker

**BudgetBuddy+** is a lightweight, interactive web-based expense tracking tool built using **Python**, **Jupyter Notebook**, **ipywidgets**, **Voila**, and **PostgreSQL (via pgAdmin)**. It allows users to log in, enter expenses, track monthly budgets, and visualize their spending—all from a clean, responsive dashboard.

---

## 📌 Features

- ✅ Secure Login using PostgreSQL (pgAdmin)
- 🧾 Manual and CSV-based Expense Entry
- 📊 Pie Chart Visualization by Category (Plotly)
- 🧮 Monthly Budget Setting with Alerts
- 💾 CSV Upload & Download
- 🌗 Clean and Responsive Dashboard (styled with HTML/CSS)

---

## 🚀 How to Run This Project
step 1 : 
install python , postgresql-17.5-3-windows-x64 and pgadmin
open cmd and install all the dependencies.

Step 2: Install Required Packages

Make sure you have Python installed. Then install the dependencies:

bash:

pip install ipywidgets pandas plotly voila psycopg2

### Step 3: Set Up PostgreSQL and pgAdmin

1. Install **PostgreSQL** and **pgAdmin**.
2. Create a new database (e.g., `budgetbuddy`).
3. Create a `users` table with this schema:

```sql:

CREATE TABLE users (
    id SERIAL PRIMARY KEY,
    username VARCHAR(50) NOT NULL UNIQUE,
    password VARCHAR(100) NOT NULL
);
```

4. Insert a test user (replace with your desired credentials):

```sql
INSERT INTO users (username, password) VALUES ('admin', 'admin123');
```

> 🔐 _Passwords are stored in plaintext here for demonstration—use hashing in production._

### Step 4: Configure Database Credentials in the Notebook

Inside the notebook, make sure your connection string matches:

```python
conn = psycopg2.connect(
    host="localhost",
    database="budgetbuddy",
    user="your_pg_user",            ## in this you have to input the PostgreSQL username 
    password="your_pg_password"	    ## in this you have to input the PostgreSQL password
)
```

### Step 5: Launch the App with Voila

1. Open the project folder where file is downloaded.
2. Right click and open with CMD or terminal(you can directly open this folder path)
3. After open terminal run this below code to open the Budget buddy.ipynb. ("viola Budget buddy.ipynb")


This will open your interactive dashboard in a web browser.


## 📃 License

This project is for educational purposes. Modify and reuse freely with credit.

