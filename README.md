# 📚 Library Management SQL Project

This project contains a **SQL-based Library Management System** designed to model and query a small library database. It includes schema creation, relationships between tables, and various queries to answer common library-related questions such as book availability, borrower details, and branch statistics.

---

## 🗂️ Project Overview

The goal of this project is to build a relational database for managing library data — including books, authors, publishers, branches, and borrowers — and to demonstrate key SQL operations such as joins, aggregations, and filtering.

---

## 🏗️ Database Schema

**Database Name:** `library_analysis`

The system includes the following tables:

| Table Name | Description |
|-------------|-------------|
| `tbl_publisher` | Stores publisher information such as name, address, and contact details. |
| `tbl_book` | Contains book details and links to the publisher. |
| `tbl_book_authors` | Maps books to their respective authors. |
| `tbl_book_copies` | Tracks how many copies of each book are available at different branches. |
| `tbl_borrower` | Contains borrower details including contact information. |
| `tbl_book_loans` | Records which borrower checked out which book, from which branch, and for how long. |
| `tbl_library_branch` | Stores branch names and their addresses. |

---

## 🔑 Key Relationships

- Each **Book** is published by a **Publisher** (`tbl_book` → `tbl_publisher`).
- Each **Book** can have one or more **Authors** (`tbl_book_authors`).
- **Book copies** are distributed across various **Branches** (`tbl_book_copies` → `tbl_library_branch`).
- **Borrowers** can check out **Books** from specific **Branches** (`tbl_book_loans`).

---

## 💡 Example Queries

This project includes SQL queries that demonstrate various real-world scenarios:

1. **Count copies of a specific book in a branch**  
   Example: Find how many copies of *“The Lost Tribe”* are available at the *Sharpstown* branch.

2. **Count copies per branch for a specific book**

3. **List borrowers with no books checked out**

4. **Retrieve book loan details by branch and due date**

5. **Find total books loaned per branch**

6. **List borrowers with more than 5 books checked out**

7. **Find all books by a specific author in a specific branch**  
   Example: Books by *Stephen King* available in the *Central* branch.

---

## ⚙️ How to Use

1. **Clone the repository**
   ```bash
   git clone https://github.com/your-username/library-management-sql.git
   cd library-management-sql
   ```

2. **Run the SQL script**
   ```sql
   SOURCE 'Library management.sql';
   ```

3. **Explore the queries**
   - Open MySQL or any SQL client.
   - Run each `SELECT` query to analyze different aspects of the database.

---

## 🧩 Technologies Used

- **MySQL** (or any SQL-compatible RDBMS)  
- **SQL DDL** (Data Definition Language)  
- **SQL DML** (Data Manipulation Language)

---

## 📈 Future Enhancements

- Add sample data insertion scripts.  
- Implement stored procedures for common operations.  
- Create triggers for automatic due-date notifications.  
- Extend schema to include book genres and employee management.
