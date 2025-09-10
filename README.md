# Database-Laboratory
Café Menu &amp; Order Tracker is a small project for majorly understanding and visualizing the database operations with web inteface. This project was for my academic course CSE 3110 - Database Systems Laboratory (1.5 credit hour).



# ☕ Café Menu & Order Tracker with Ratings

## 📌 Project Overview
The **Café Menu & Order Tracker with Ratings** is a simple **database-driven web application** built as part of the **CSE3110 – Database Systems Laboratory** course.  
It demonstrates **SQL queries, CRUD operations, relational integrity**, and the use of **multiple interlinked tables**.  

The project features:
- A **Customer Interface** for browsing the menu, placing orders, and rating items.  
- An **Admin Panel** for managing customers, menu items, orders, and feedback.  

---

## 🎯 Features
### 👤 Customer
- View café menu (categorized items with prices).  
- Place new orders (select multiple items with quantities).  
- Give ratings (1–5 scale) and optional comments on menu items.  

### 🔧 Admin
- Manage customers (add, update, delete).  
- Manage menu items (add, edit, remove).  
- View and manage orders (track, cancel, update).  
- View and manage ratings/feedback.  

---

## 🗄️ Database Schema
The project uses **5 interlinked tables**:

1. **Customers**  
   - `cust_id` (PK), `name`, `contact`, `email`

2. **Menu**  
   - `item_id` (PK), `item_name`, `category`, `price`

3. **Orders**  
   - `order_id` (PK), `cust_id` (FK → Customers), `order_date`, `total_amount`

4. **Order_Items** (Mapping table)  
   - `order_id` (FK → Orders), `item_id` (FK → Menu), `quantity`

5. **Ratings**  
   - `rating_id` (PK), `cust_id` (FK → Customers), `item_id` (FK → Menu), `rating`, `comment`

---

## 🔗 Relationships
- **Customers → Orders:** One-to-Many (a customer can place many orders).  
- **Orders ↔ Menu (via Order_Items):** Many-to-Many.  
- **Customers ↔ Menu (via Ratings):** Many-to-Many.  
- **Orders → Order_Items:** One-to-Many.  
- **Menu → Ratings:** One-to-Many.  

---

## 📊 ER Diagram
![ER Diagram](docs/ER_Diagram_Cafe.png)

## 🗂️ Database Schema Diagram
![Schema Diagram](docs/Schema_Diagram_Cafe.png)

---

## ⚙️ Tech Stack
- **Frontend:** ASP.NET Web Forms / HTML / CSS / JavaScript  
- **Backend:** C# (Code-Behind), ASP.NET  
- **Database:** MySQL / SQL Server (depending on setup)  
- **Version Control:** GitHub  

---

## 🚀 How to Run
1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/cafe-menu-order-tracker.git
   cd cafe-menu-order-tracker
