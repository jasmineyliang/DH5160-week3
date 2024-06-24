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

### Quiz 1: Writing a JOIN Query
**Question:** Write a query to fetch employee names and their corresponding department names using an INNER JOIN. (we have both employee and department table, employee table has employees.name and employees.department, department table has department.name and other infomation)

**Answer:**
```sql

```

### Quiz 2: Writing a JOIN Query with Multiple Tables
**Question:** Write a query to fetch employee names and project titles by joining the employees, departments, and projects tables.(we have employee, department table and projects; table has employees.name and employees.department, department table has department.name and other infomation, project table has project.department.name)

**Answer:**
```sql

```

### Quiz 3: Writing a Subquery
**Question:** Write a query to fetch the names of employees who are in the 'Sales' department using a subquery.

**Answer:**
```sql

```

### Quiz 4: Writing a Subquery for Filtering
**Question:** Write a query to fetch employee names who belong to the 'Marketing' department using a subquery.

**Answer:**
```sql


```

### Quiz 5: Basic Query Optimization (Multiple Choice)
**Question:** What is the best optimization technique for the following query?
```sql
SELECT *
FROM employees
WHERE department_id = 5
ORDER BY name;
```
- A) Use a LIMIT clause
- B) Create an index on the `department_id` column
- C) Use a different database
- D) Select fewer columns


### Quiz 6: Writing a JOIN Query with a Condition
**Question:** Write a query to fetch employee names and department names for departments located in 'New York' using a JOIN.

**Answer:**
```sql


```

### Quiz 7: Writing a Subquery with Aggregation
**Question:** Write a query to fetch employee names and salaries where the salary is greater than the average salary across all employees.

**Answer:**
```sql

```

### Quiz 8: Writing a Subquery for Comparison
**Question:** Write a query to fetch employee names and salaries where the salary is greater than the average salary of their department.

**Answer:**
```sql


```

### Quiz 9: Query Optimization (Multiple Choice)
**Question:** What is the best optimization technique for the following query?
```sql
SELECT name
FROM employees
WHERE department_id IN (
    SELECT id
    FROM departments
    WHERE location = 'San Francisco'
);
```
- A) Use a JOIN instead of a subquery
- B) Create an index on the `departments.location` column
- C) Use a DISTINCT clause
- D) Increase the server's memory



### Quiz 10: Writing a LEFT JOIN Query
**Question:** Write a query to fetch employee names and department names, including employees without a department, using a LEFT JOIN.

**Answer:**
```sql


```

### Quiz 11: Query Optimization (Multiple Choice)
**Question:** What is the best optimization technique for the following query?
```sql
SELECT id, name
FROM employees
WHERE name LIKE 'John%';
```
- A) Create an index on the `name` column
- B) Use a FULLTEXT index on the `name` column
- C) Increase the server's CPU
- D) Use an ORDER BY clause










## Assignment 

### Assignment Question: Problem Solving with Fitness Data

**Assignment:** Write a SQL script to analyze a fitness tracking database to answer specific questions about user activities, exercises, and performance. Use advanced SQL commands including JOINs, subqueries, and optimization techniques to complete this assignment.

#### Database Schema:

1. **users**
   - `id` (INT, Primary Key)
   - `name` (VARCHAR)
   - `age` (INT)
   - `gender` (VARCHAR)

2. **activities**
   - `id` (INT, Primary Key)
   - `user_id` (INT, Foreign Key)
   - `activity_date` (DATE)
   - `activity_type` (VARCHAR)
   - `duration_minutes` (INT)
   - `calories_burned` (INT)

3. **workouts**
   - `id` (INT, Primary Key)
   - `user_id` (INT, Foreign Key)
   - `workout_date` (DATE)
   - `workout_type` (VARCHAR)
   - `intensity` (VARCHAR)

#### Problem Statement:

You are tasked with writing a SQL script to answer the following questions:

1. **User Demographics:** 
   Write a query to list the total number of users, the average age of users, and the distribution of users by gender.

2. **Activity Summary:**
   Write a query to list each user along with the total number of activities they have logged and the total calories they have burned.

3. **Popular Activities:**
   Write a query to list the most common activity types, including the activity type and the number of times each activity has been performed.

4. **Workout Summary:**
   Write a query to list each user along with the total number of workouts they have logged and the average intensity of their workouts.

5. **Top Performers:**
   Write a query to find the top 3 users who have burned the most calories in total. List the user name and the total calories burned.

6. **Optimization:**
   Identify at least one index that could be created to optimize the queries you have written. Explain why this index would help.

#### Deliverables:

- A SQL script file (`fitness_data_analysis.sql`) containing the queries for each of the questions above.
- A brief document (`index_optimization.txt`) explaining the index you chose to optimize your queries and why.

### Example Solution:

Here is a starting point for some of the queries:

1. **User Demographics:**
   ```sql
   SELECT 
       COUNT(*) AS total_users,
       AVG(age) AS average_age,
       gender,
       COUNT(*) * 100.0 / (SELECT COUNT(*) FROM users) AS gender_distribution
   FROM users
   GROUP BY gender;
   ```

2. **Activity Summary:**
   ```sql

   
   ```

3. **Popular Activities:**
   ```sql

   
   ```

4. **Workout Summary:**
   ```sql

   
   ```

5. **Top Performers:**
   ```sql

   
   ```

### index_optimization.txt
```text

```

### Mini Project: Comprehensive Health Data Analysis

**Project:** Develop a comprehensive health data analysis system using an extensive health database. The project will involve more complex queries, data processing, and report generation.

#### Database Schema:

1. **patients**
   - `id` (INT, Primary Key)
   - `name` (VARCHAR)
   - `age` (INT)
   - `gender` (VARCHAR)
   - `address` (VARCHAR)
   - `phone_number` (VARCHAR)

2. **doctors**
   - `id` (INT, Primary Key)
   - `name` (VARCHAR)
   - `specialization` (VARCHAR)
   - `experience_years` (INT)

3. **appointments**
   - `id` (INT, Primary Key)
   - `patient_id` (INT, Foreign Key)
   - `doctor_id` (INT, Foreign Key)
   - `appointment_date` (DATE)
   - `reason` (VARCHAR)

4. **treatments**
   - `id` (INT, Primary Key)
   - `appointment_id` (INT, Foreign Key)
   - `treatment_date` (DATE)
   - `treatment_description` (VARCHAR)

5. **medications**
   - `id` (INT, Primary Key)
   - `treatment_id` (INT, Foreign Key)
   - `medication_name` (VARCHAR)
   - `dosage` (VARCHAR)

6. **invoices**
   - `id` (INT, Primary Key)
   - `appointment_id` (INT, Foreign Key)
   - `amount` (DECIMAL)
   - `payment_date` (DATE)
   - `status` (VARCHAR)

#### Problem Statement:

You are tasked with developing a SQL script to perform comprehensive analysis and reporting on the health database. Your analysis should include the following tasks:

1. **Patient Overview:**
   - List all patients with their details and the number of appointments they have had.

2. **Doctor Performance:**
   - List all doctors with their details and the number of appointments they have handled, including their total years of experience.

3. **Appointment Analysis:**
   - List the total number of appointments each month and identify any seasonal trends.

4. **Treatment and Medication Analysis:**
   - List the most common treatments and medications prescribed, including the treatment description and medication name with their respective counts.

5. **Invoice Summary:**
   - List the total revenue generated each month and the breakdown of paid vs. unpaid invoices.

6. **Advanced Insights:**
   - Identify patients who have not visited in the last year.
   - List doctors who have handled the most critical cases (based on appointment reasons).

7. **Optimization:**
   - Identify at least three indexes that could be created to optimize the queries you have written. Explain why these indexes would help.

#### Deliverables:

- A SQL script file (`comprehensive_health_analysis.sql`) containing the queries for each of the tasks above.
- A brief document (`index_optimization.txt`) explaining the indexes you chose to optimize your queries and why.

### Example Solution:

Here is a starting point for some of the queries:

1. **Patient Overview:**
   ```sql

   
   ```

2. **Doctor Performance:**
   ```sql

   
   ```

3. **Appointment Analysis:**
   ```sql

   
   ```

4. **Treatment and Medication Analysis:**
   ```sql

   
   ```

   ```sql


   ```

5. **Invoice Summary:**
   ```sql

   
   ```

6. **Advanced Insights:**
   Patients who have not visited in the last year

   ```sql

   
   ```

   ```sql

   
   ```
