# 📌 VinRestaurant — Restaurant Information & Operations Management System

## 📄 Brief Description

VinRestaurant is a comprehensive Restaurant Management System designed to streamline daily operations including menu management, table reservations, order processing, staff role control, and revenue reporting.  
The system is supported by a robust MySQL database and a modern web interface that provides:

- Centralized data management  
- Seamless restaurant workflow  
- Real-time statistics and dashboard insights  
- Secure authentication with role-based permissions  
- Automated reporting and audit logging  

This system solves common restaurant issues such as manual order tracking, inconsistent inventory control, lack of reporting, and limited operational visibility.

---

## 🎯 Functional & Non-functional Requirements

### ✅ Functional Requirements

#### **1. User Management & Authentication**
- Secure login/logout  
- MySQL-based Role-Based Access Control (Admin, Manager, Waiter)

#### **2. Menu Management**
- CRUD for menu items  
- Category management (Appetizers, Drinks, Main Dishes, Desserts, etc.)  
- Price and availability tracking  

#### **3. Table Management**
- Table registration (number, seats)  
- Track table status: Available / Occupied / Reserved  

#### **4. Order Management**
- Create dine-in orders  
- Assign orders to tables  
- Add/remove menu items  
- Automatic total calculation  
- Order status: Pending → In-progress → Completed → Paid  

#### **5. Reservation System**
- Customer reservation records  
- Assign tables to reservations  
- Automatic conflict detection (via constraints or triggers)

#### **6. Reporting & Statistics**
- Daily/weekly/monthly sales reports  
- Most ordered dishes  
- Table usage statistics  
- Low-stock report (if inventory module enabled)  
- Export reports to CSV/PDF  

#### **7. Audit Logging**
- Triggers to log important activities (price updates, new orders, stock changes)

#### **8. Inventory Management (Optional)**
- Track ingredients  
- Auto-deduct stock based on order completion  
- Low-stock alerts  

---

### 📌 Non-Functional Requirements

#### **Performance**
- Optimized SQL queries  
- Indexing on frequent search fields (menu items, orders, reservations)

#### **Security**
- MySQL user roles and privilege separation  
- Password hashing  
- Input sanitization and parameterized queries

#### **Usability**
- Responsive and intuitive web UI  
- Clear dashboards with visual charts

#### **Reliability**
- ACID-compliant transactions  
- Backup and recovery scripts

#### **Maintainability**
- Clean, modular architecture (DB ↔ API ↔ UI)  
- Consistent naming conventions and documentation

---

## 🧱 Planned Core Entities

### **Main Entities**
- **User** — system login, role assignment  
- **Role** — Admin, Manager, Waiter  
- **MenuCategory** — grouping of menu items  
- **MenuItem** — dish/drink details  
- **Table** — table metadata and status  
- **Order** — order-level information  
- **OrderItem** — items inside an order  
- **Reservation** — customer reservations  
- **InventoryItem** (optional) — tracked ingredients  
- **StockMovement** (optional) — stock in/out logs  
- **AuditLog** — auto-generated using triggers  

### **Database Objects**
- **Stored Procedures**
  - add_order()
  - update_inventory()
  - generate_report()

- **Triggers**
  - log_menu_price_change  
  - auto_decrease_inventory  

- **Views**
  - daily_sales_view  
  - popular_dishes_view  

---

## 🔧 Tech Stack

### **Backend (choose one):**
- Node.js (Express.js)  
- PHP (Laravel or pure PHP)  
- Python Flask  
- Python Django  

### **Database**
- **MySQL**  
  - MySQL Workbench  
  - Tables, relationships, constraints  
  - Stored procedures & triggers  
  - Index and performance tuning  

### **Frontend**
- HTML, CSS, JavaScript  
- TailwindCSS or Bootstrap  

### **Data Visualization**
- Chart.js or D3.js for dashboards  
- SQL views for data feeding  

---

## 👥 Team Members & Roles

| Name        | Role                  | Responsibilities |
|-------------|-----------------------|------------------|
| Tiển Hiếu    | Database Developer    | ERD, schema, stored procedures, triggers, security |
| Trung    | Backend Developer     | API endpoints, routing, authentication, DB integration |
| Nguyễn Hoàng Hiếu | Frontend Developer    | UI/UX, forms, dashboards, styling |
| Thành    | Tester / QA           | Test scenarios, validation, documentation, debugging |


---

## 📅 Timeline (Milestones)

### **Week 1 — Requirements & Design**
- Requirements gathering  
- Entity-relationship diagram (ERD)  
- Schema and use-case definition  

### **Week 2 — Database Implementation**
- Create tables and constraints  
- Add triggers, procedures, views  
- Insert sample data  
- Index and performance tuning  

### **Week 3 — Backend Development**
- Framework setup  
- User authentication  
- CRUD for Menu, Tables, Orders, Reservations  
- Connect procedures & queries  

### **Week 4 — Frontend Development**
- UI pages (Menu, Orders, Reservations, Dashboard)  
- Responsive design  
- Chart integration  

### **Week 5 — Security & Testing**
- MySQL privileges  
- Input validations  
- Functional + integration testing  
- Bug fixing  

### **Week 6 — Finalization**
- UI polish  
- Complete documentation  
- Prepare demo & deployment  

---


