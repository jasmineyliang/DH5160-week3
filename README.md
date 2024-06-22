# FSM

![](https://img.shields.io/bower/l/FSM?color=green) ![](https://img.shields.io/github/commit-activity/t/AmmarAbdelhalem/FSM) ![](https://img.shields.io/github/stars/AmmarAbdelhalem/FSM) ![](https://img.shields.io/github/contributors/AmmarAbdelhalem/FSM)

## What is included?


- [Introduction to databases and SQL](SQL_MAN/0-IntroductiontodatabasesandSQL.md)

- [Data Types and Data Definition](SQL_MAN/1-DataTypesandDataDefinition.md)

- [Creating and modifying database objects](SQL_MAN/2-Creatingandmodifyingdatabaseobjects.md)

- [Data manipulation](SQL_MAN/3-Datamanipulation.md)

- [Aggregate functions](SQL_MAN/4-Aggregatefunctions.md)

- [Subqueries and joins](SQL_MAN/5-Subqueriesandjoins.md)

- [Transactions and concurrency](SQL_MAN/6-Transactionsandconcurrency.md)

- [Stored procedures and triggers](SQL_MAN/7-Storedproceduresandtriggers.md)

- [Advanced topics](https://github.com/AmmarAbdelhalem/FSM/blob/main/SQL_MAN/8-Advancedtopics.md)

*If you find this useful support me with star this repo*

## Contributing

If you find any bug or you want to contribut with any information I accept that, Just create a pull request with the changes and I will check it.

## License

All assets and code are under the [MIT License](https://github.com/AmmarAbdelhalem/FSM/blob/main/LICENSE.md).


--------------------------------------------------------------------------------------------------------------------------------

## Quiz

### Quiz 1: Basic SELECT Query
**Question:**
Write a SELECT statement to fetch all columns from the `students` table.

**Answer:**
```sql
SELECT * FROM students;
```

### Quiz 2: SELECT Specific Columns
**Question:**
Write a SELECT statement to fetch only the `name` and `age` columns from the `students` table.

**Answer:**
```sql

```

### Quiz 3: Basic INSERT Query
**Question:**
Write an INSERT statement to add a new student named 'Alice' who is 20 years old to the `students` table.

**Answer:**
```sql

```

### Quiz 4: INSERT Multiple Values
**Question:**
Write an INSERT statement to add two students: 'Bob' who is 22 years old and 'Charlie' who is 23 years old to the `students` table.

**Answer:**
```sql

```

### Quiz 5: Basic UPDATE Query
**Question:**
Write an UPDATE statement to change the age of the student named 'Alice' to 21.

**Answer:**
```sql

```

### Quiz 6: UPDATE Multiple Columns
**Question:**
Write an UPDATE statement to change the `age` of 'Bob' to 23 and set his `grade` to 'A'.

**Answer:**
```sql

```

### Quiz 7: Basic DELETE Query
**Question:**
Write a DELETE statement to remove the student named 'Charlie' from the `students` table.

**Answer:**
```sql

```

### Quiz 8: DELETE All Records
**Question:**
Write a DELETE statement to remove all students who are older than 22 from the `students` table.

**Answer:**
```sql

```

### Quiz 9: SELECT with WHERE Clause
**Question:**
Write a SELECT statement to fetch all columns from the `students` table where the age is greater than 20.

**Answer:**
```sql

```

### Quiz 10: SELECT with ORDER BY
**Question:**
Write a SELECT statement to fetch all columns from the `students` table and order the results by the `name` column in ascending order.

**Answer:**
```sql

```

### Quiz 11: SELECT with Simple WHERE Conditions
**Question:**
Write a SELECT statement to fetch the `name` and `grade` of students from the `students` table where the grade is 'B'.

**Answer:**
```sql

```


## Assignment 

Patient Records Management
Description:
Create and manage a database for patient records.

Tasks:

Create Tables:

Create a table named patients with columns: id (INT, Primary Key, Auto Increment), name (VARCHAR(50)), age (INT), gender (VARCHAR(10)).
Create a table named visits with columns: id (INT, Primary Key, Auto Increment), patient_id (INT, Foreign Key referencing patients(id)), visit_date (DATE), reason (VARCHAR(255)).

```sql

```

Insert Data:

```sql

```

Insert at least five patients into the patients table.
Insert visit records for each patient.
Queries:

- Write a query to fetch all columns from the patients table.
```sql

```
- Write a query to fetch all visit records for a patient with a given name.
```sql

```
- Write a query to update the reason for a specific visit by visit ID.
```sql

```

## Project
### Mini Project: Health Data Management System

**Project Overview:**
This project involves creating a comprehensive health data management system using SQL. You will design a database schema, populate the database with sample data, and write queries to manage and retrieve data. The project covers creating and managing patient records, medication tracking, and appointment scheduling.

### Part 1: Database Schema Design

**Tables to Create:**

1. **patients**
   - `id` (INT, Primary Key, Auto Increment)
   - `name` (VARCHAR(50))
   - `age` (INT)
   - `gender` (VARCHAR(10))

2. **visits**
   - `id` (INT, Primary Key, Auto Increment)
   - `patient_id` (INT, Foreign Key referencing `patients(id)`)
   - `visit_date` (DATE)
   - `reason` (VARCHAR(255))

3. **medications**
   - `id` (INT, Primary Key, Auto Increment)
   - `name` (VARCHAR(50))
   - `dosage` (VARCHAR(50))

4. **prescriptions**
   - `id` (INT, Primary Key, Auto Increment)
   - `patient_id` (INT, Foreign Key referencing `patients(id)`)
   - `medication_id` (INT, Foreign Key referencing `medications(id)`)
   - `start_date` (DATE)
   - `end_date` (DATE)

5. **appointments**
   - `id` (INT, Primary Key, Auto Increment)
   - `patient_id` (INT, Foreign Key referencing `patients(id)`)
   - `appointment_date` (DATE)
   - `doctor` (VARCHAR(50))

### Part 2: Data Insertion

**Sample Data to Insert:**

```sql
-- Patients
INSERT INTO patients (name, age, gender) VALUES ('John Doe', 30, 'Male');
INSERT INTO patients (name, age, gender) VALUES ('Jane Smith', 25, 'Female');
INSERT INTO patients (name, age, gender) VALUES ('Emily Davis', 40, 'Female');
INSERT INTO patients (name, age, gender) VALUES ('Michael Brown', 50, 'Male');
INSERT INTO patients (name, age, gender) VALUES ('Sarah Wilson', 35, 'Female');

-- Visits
INSERT INTO visits (patient_id, visit_date, reason) VALUES (1, '2024-01-10', 'Routine check-up');
INSERT INTO visits (patient_id, visit_date, reason) VALUES (2, '2024-01-15', 'Flu symptoms');
INSERT INTO visits (patient_id, visit_date, reason) VALUES (3, '2024-01-20', 'Annual physical');
INSERT INTO visits (patient_id, visit_date, reason) VALUES (4, '2024-01-25', 'Chest pain');
INSERT INTO visits (patient_id, visit_date, reason) VALUES (5, '2024-01-30', 'Headache');

-- Medications
INSERT INTO medications (name, dosage) VALUES ('Aspirin', '100mg');
INSERT INTO medications (name, dosage) VALUES ('Ibuprofen', '200mg');
INSERT INTO medications (name, dosage) VALUES ('Amoxicillin', '500mg');
INSERT INTO medications (name, dosage) VALUES ('Metformin', '1000mg');
INSERT INTO medications (name, dosage) VALUES ('Lisinopril', '10mg');

-- Prescriptions
INSERT INTO prescriptions (patient_id, medication_id, start_date, end_date) VALUES (1, 1, '2024-02-01', '2024-02-10');
INSERT INTO prescriptions (patient_id, medication_id, start_date, end_date) VALUES (2, 2, '2024-02-05', '2024-02-15');
INSERT INTO prescriptions (patient_id, medication_id, start_date, end_date) VALUES (3, 3, '2024-02-10', '2024-02-20');
INSERT INTO prescriptions (patient_id, medication_id, start_date, end_date) VALUES (4, 4, '2024-02-15', '2024-02-25');
INSERT INTO prescriptions (patient_id, medication_id, start_date, end_date) VALUES (5, 5, '2024-02-20', '2024-03-01');

-- Appointments
INSERT INTO appointments (patient_id, appointment_date, doctor) VALUES (1, '2024-03-01', 'Dr. Smith');
INSERT INTO appointments (patient_id, appointment_date, doctor) VALUES (2, '2024-03-05', 'Dr. Johnson');
INSERT INTO appointments (patient_id, appointment_date, doctor) VALUES (3, '2024-03-10', 'Dr. Lee');
INSERT INTO appointments (patient_id, appointment_date, doctor) VALUES (4, '2024-03-15', 'Dr. Brown');
INSERT INTO appointments (patient_id, appointment_date, doctor) VALUES (5, '2024-03-20', 'Dr. Williams');
```

### Part 3: SQL Queries

**List of Queries to Implement (without solutions provided):**

1. Retrieve all patient records.
2. Retrieve all visits for a specific patient.
3. Retrieve all medications.
4. Retrieve all prescriptions for a specific patient.
5. Retrieve all appointments for a specific doctor.
6. Update reason for a specific visit. (you can choose any patient and modify to any reason)
7. Update dosage for a specific medication.
8. Update appointment date for a specific appointment.



### Part 4: Additional Tasks (Hard, bonus points)

**Additional SQL Tasks (without solutions provided):**

1. List patients with more than one visit.
2. Find the most prescribed medication.
3. List patients with upcoming appointments.
