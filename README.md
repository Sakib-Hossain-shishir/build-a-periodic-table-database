# Periodic Table Database

A Bash command-line application that queries a PostgreSQL database to retrieve information about chemical elements from the periodic table.

This project was built as part of the FreeCodeCamp Relational Database certification.

---

## 📌 Project Overview

This script allows users to search for an element using:

- Atomic number (e.g., `1`)
- Chemical symbol (e.g., `H`)
- Element name (e.g., `Hydrogen`)

It connects to a PostgreSQL database named `periodic_table` and returns formatted information including:

- Atomic number  
- Name  
- Symbol  
- Type  
- Atomic mass  
- Melting point (°C)  
- Boiling point (°C)  

If the element does not exist, the script responds appropriately.

---

## 🛠 Technologies Used

- Bash
- PostgreSQL
- Git
- Linux command line

---

## 🗄 Database Structure

The database contains three tables:

### `elements`
- `atomic_number` (Primary Key)
- `symbol`
- `name`

### `properties`
- `atomic_number` (Foreign Key)
- `atomic_mass`
- `melting_point_celsius`
- `boiling_point_celsius`
- `type_id`

### `types`
- `type_id` (Primary Key)
- `type`

These tables are joined to produce complete element information.

---

## 🚀 How to Run

Make sure PostgreSQL is installed and the database is set up.

Run the script with:

```bash
./element.sh <argument>
```

### Examples

Search by atomic number:

```bash
./element.sh 1
```

Search by symbol:

```bash
./element.sh H
```

Search by name:

```bash
./element.sh Hydrogen
```

---

## ⚠️ Error Handling

If no argument is provided:

```
Please provide an element as an argument.
```

If the element does not exist:

```
I could not find that element in the database.
```
---

## 👤 Author

Sakib Hossain Shishir

---

## 🧠 What This Project Demonstrates

- Writing structured SQL joins
- Parsing database output in Bash
- Handling user input validation
- Managing Git repositories
- Clean CLI program design

---

If you're reviewing this project, clone it, run it, and test with multiple inputs to verify behavior.
