# 💰 Expense Tracker

A beginner-friendly full-stack **Expense Tracker** application built using **React (Vite)** for the frontend, **Node.js + Express** for the backend, and **SQLite (better-sqlite3)** as the database.

The application allows users to record daily expenses, filter and paginate expense records, view monthly spending summaries by category, edit and delete expenses, and store all data locally using SQLite.

---

# ✨ Features

* ➕ Add new expenses
* 📋 View all expenses
* 🔍 Filter expenses by category
* 📄 Pagination support
* 📊 Monthly expense summary
* 📈 Category-wise spending bars
* ✏️ Edit existing expenses
* 🗑 Delete expenses
* 💾 SQLite database with automatic table creation
* ⚡ Fast backend using Express and better-sqlite3

---

# 🛠 Tech Stack

## Frontend

* React
* Vite
* CSS

## Backend

* Node.js
* Express.js
* CORS
* better-sqlite3

## Database

* SQLite (`data.db`)

---

# 📁 Project Structure

```text
project/
│
├── backend/
│   ├── index.js
│   ├── package.json
│   └── data.db
│
└── frontend/
    ├── src/
    │   ├── App.jsx
    │   ├── App.css
    │   ├── main.jsx
    │   └── index.css
    │
    └── package.json
```

---

# 🚀 Getting Started

## 1. Clone the repository

```bash
git clone <repository-url>
cd project-folder
```

---

## 2. Start the Backend

Move into the backend folder:

```bash
cd backend
```

Run the server:

```bash
node index.js
```

The backend runs at:

```
http://localhost:5000
```

---

## 3. Start the Frontend

Open another terminal:

```bash
cd frontend
```

Run the Vite development server:

```bash
npm run dev
```

The frontend will typically be available at:

```
http://localhost:5173
```

---

# 🗄 Database

The application automatically creates a SQLite database named:

```
data.db
```

It also creates the **expenses** table if it does not already exist.

## Expenses Table

| Column     | Type    | Description                       |
| ---------- | ------- | --------------------------------- |
| id         | INTEGER | Primary Key (Auto Increment)      |
| title      | TEXT    | Expense title                     |
| amount     | REAL    | Expense amount                    |
| category   | TEXT    | Expense category                  |
| date       | TEXT    | Expense date (YYYY-MM-DD)         |
| created_at | TEXT    | Timestamp when record was created |

---

# 📡 REST API Endpoints

## Create Expense

**POST**

```
/expenses
```

Creates a new expense.

---

## Get Expenses

**GET**

```
/expenses
```

Supports:

* Pagination
* Category filtering
* Month filtering

Example:

```
/expenses?page=1&limit=10
```

```
/expenses?category=Food
```

```
/expenses?month=2026-07
```

---

## Monthly Summary

**GET**

```
/expenses/summary
```

Returns total spending grouped by category.

Example:

```
/expenses/summary?month=2026-07
```

---

## Update Expense

**PUT**

```
/expenses/:id
```

Updates an existing expense.

---

## Delete Expense

**DELETE**

```
/expenses/:id
```

Deletes an expense.

---

# 💻 Application Features

### Add Expense

Users can enter:

* Expense title
* Amount
* Category
* Date

Validation ensures:

* Title is not empty
* Amount is greater than zero

---

### Monthly Summary

Displays:

* Spending grouped by category
* Horizontal progress bars
* Grand total for the selected month

If no expenses exist for the selected month, a friendly message is shown.

---

### Expense List

Displays:

* Title
* Category
* Amount
* Date
* Delete button

Supports:

* Category filter
* Pagination
* Loading states
* Empty states

---

# ▶️ Running the Project

Start backend:

```bash
cd backend
node index.js
```

Start frontend:

```bash
cd frontend
npm run dev
```

Visit:

```
http://localhost:5173
```

---

# 📚 Learning Concepts

This project demonstrates:

* React Hooks (`useState`, `useEffect`)
* REST APIs with Express
* SQLite database operations
* CRUD operations
* Form validation
* Pagination
* Filtering
* Aggregation using SQL (`SUM`, `GROUP BY`)
* Asynchronous API calls using `fetch()`
* Basic responsive CSS

---

# 👨‍💻 Author

A beginner-friendly full-stack Expense Tracker project built using **React**, **Express**, and **SQLite (better-sqlite3)** for learning full-stack web development.
