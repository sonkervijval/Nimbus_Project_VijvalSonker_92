# Nimbus_Project_VijvalSonker_92
College Bus fee and Route Management
# College Bus Fee & Route Management System

A comprehensive C-based application for managing college bus routes, students, and fee billing. This project integrates route handling, student registration, billing computation, file storage, and report generation — all in a single, compact C source file.

---

## 🚀 Features

### **1. Route Management**

* Add new bus routes (name, distance, rate per km)
* List all available routes
* Delete existing routes
* Auto-generates route IDs

### **2. Student Management**

* Add students with assigned routes
* List all students
* Remove students by ID
* Auto-generates student IDs

### **3. Billing System**

* Calculates bus fee using:

  * Base fare (₹50)
  * Distance × Rate per km
  * 5% discount for distances < 5 km
* Generates fee slip (appended to `data/receipts.txt`)
* Includes timestamp

### **4. Data Persistence (File I/O)**

* Auto-creates a `data/` directory
* Saves and loads:

  * Routes → `routes.dat`
  * Students → `students.dat`
* Stores data in binary format for efficiency

### **5. Reporting**

* Prints revenue summary per route
* Shows student count and total revenue generated

---

## 📁 Project Structure

```
├── bus_manager.c        # Main program (single-file system)
└── data/
    ├── routes.dat       # Auto-generated route database
    ├── students.dat     # Auto-generated student database
    └── receipts.txt     # Fee slip logs
```

The `data/` folder is created automatically on first run.

---

## 🛠️ How to Compile & Run

### **Compile:**

```
gcc bus_manager.c -o bus_manager
```

### **Run:**

```
./bus_manager
```

---

## 📌 Menu Options (Inside Program)

```
1. Show routes
2. Add route
3. Remove route
4. Show students
5. Add student
6. Remove student
7. Generate fee slip for student
8. Print summary
9. Save data
0. Exit
```

---

## 🧩 Program Flow

1. Load saved routes and students (if files exist)
2. Seed default sample data (only if empty)
3. Run interactive menu loop
4. On exit → auto-save all data

---

## 💡 Highlights

* Dynamic arrays for both routes and students
* Auto ID tracking using global counters
* Safe string handling with `strncpy`
* OS-compatible folder creation (Windows/Linux)
* Organized modular design (though in one file)

---

## 📄 Fee Slip Format (Example)

```
-------------------------------
Date: Tue Nov 23 12:32:10 2025
Student ID: 1
Name: Aman Kumar
Route: North Campus (ID 1)
Distance: 4.50 km | Rate: 6.00 | Amount: 77.45
-------------------------------
```

---

## ✨ Future Enhancements

* Edit/update existing routes or students
* Monthly/semester billing system
* GUI or web-based dashboard
* Export summary as CSV


---

## 👍 Author

Created by **Vijval Sonker** 

---
