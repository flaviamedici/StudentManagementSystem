# 🎓 Student Management System

A desktop-based Student Management System built with **Python**, **PyQt6**, and **SQLite**.

This application allows users to:

- View student records
- Add new students
- Search for students
- Store data using SQLite
- Manage records through a graphical user interface (GUI)

---

## 🚀 Features

✅ Desktop GUI built with PyQt6  
✅ Add student records  
✅ Search for students by name  
✅ Display records in a table view  
✅ Store data using SQLite database  
✅ Simple and user-friendly interface  

---

## 🛠️ Technologies Used

- Python 3
- PyQt6
- SQLite3

---

## 📂 Project Structure

```bash
.
├── main.py
├── database.db
└── README.md
```

---

## 🖥️ Application Overview

The application contains:

- A main window displaying student records
- A dialog window for inserting students
- A dialog window for searching students
- SQLite database integration

---

## ⚙️ How It Works

### 1️⃣ Main Window

The `MainWindow` class creates the main application window.

Features include:
- Menu bar
- Student table
- File, Help, and Edit menus

```python
self.setWindowTitle("Student Management System")
```

---

### 2️⃣ Display Student Data

Student records are loaded from the SQLite database into a table widget.

```python
connection = sqlite3.connect("database.db")
result = connection.execute("SELECT * FROM students")
```

---

### 3️⃣ Add Student

The `InsertDialog` class allows users to:
- Enter student name
- Select course
- Add mobile number

```python
cursor.execute(
    "INSERT INTO students (name, course, mobile) VALUES (?, ?, ?)",
    (name, course, mobile)
)
```

---

### 4️⃣ Search Student

The `SearchDialog` class searches for students by name.

```python
result = cursor.execute(
    "SELECT * FROM students WHERE name = ?",
    (name,)
)
```

Matching records are highlighted in the table.

---

## 📋 Database Structure

### `students` Table

| Column | Type |
|--------|------|
| id | INTEGER |
| name | TEXT |
| course | TEXT |
| mobile | TEXT |

---

## ▶️ How to Run

### 1. Clone the repository

```bash
git clone <your-repo-url>
```

---

### 2. Navigate to the project folder

```bash
cd student-management-system
```

---

### 3. Install dependencies

```bash
pip install PyQt6
```

---

### 4. Run the application

```bash
python main.py
```

---

## 🧠 OOP Concepts Used

This project demonstrates:

- Classes and objects
- Inheritance
- GUI event handling
- Database integration
- Encapsulation

---

## 📈 Class Overview

### `MainWindow`

Handles:
- Main application window
- Table display
- Menu actions
- Data loading

---

### `InsertDialog`

Handles:
- Student registration
- Input forms
- Database insertion

---

### `SearchDialog`

Handles:
- Student search functionality
- Table highlighting

---

## 📸 Example Features

### ➕ Add Student
Users can register a new student using:
- Name input
- Course dropdown
- Mobile number field

---

### 🔍 Search Student
Users can search students by entering a name.

Matching records are automatically selected in the table.

---

## ⚠️ Known Issues

There are a few minor typos in the code:

### ❌ Incorrect Method Name

```python
layout.AddWidget(button)
```

✅ Correct Version:

```python
layout.addWidget(button)
```

---

### ❌ Incorrect ComboBox Method

```python
self.course_name.itemtext()
```

✅ Correct Version:

```python
self.course_name.itemText()
```

---

These fixes are required for the application to work correctly.

---

## 💡 Future Improvements

- Add update/edit student functionality
- Add delete student feature
- Improve search filters
- Add form validation
- Add dark mode UI
- Export data to CSV or Excel
- Add login authentication

---

## 🖼️ Example UI Layout

```text
+--------------------------------------+
| Student Management System            |
+--------------------------------------+
| ID | Name | Course | Mobile         |
|--------------------------------------|
| 1  | John | Math   | 1234567890     |
| 2  | Anna | Physics| 9876543210     |
+--------------------------------------+
```

---

## 🤝 Contributing

Contributions are welcome!

1. Fork the repository
2. Create a new branch
3. Commit your changes
4. Open a pull request

---

## 📜 License

This project is for educational purposes only.

---

## ⭐ Support

If you found this project useful, give it a ⭐ on GitHub!
