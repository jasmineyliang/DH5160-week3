# Aggregate Functions

In SQL, aggregate functions are used to perform calculations on a set of values and return a single result. Some common aggregate functions include:

- `AVG`: Calculates the average of a set of values.

- `COUNT`: Counts the number of values in a set.

- `MAX`: Finds the maximum value in a set.

- `MIN`: Finds the minimum value in a set.

- `SUM`: Calculates the sum of a set of values.

Aggregate functions are typically used with the `SELECT` command and the `GROUP BY` clause. For example:

```SQL
SELECT AVG(age) FROM users;
```

This calculates the average `age` of all rows in the `users` table.

```SQL
SELECT COUNT(*) FROM users WHERE username LIKE 'j%';
```

This counts the number of rows in the `users` table where the `username` starts with `'j'`.

```SQL
SELECT MAX(age) FROM users WHERE gender = 'female';
```

This finds the maximum `age` of all rows in the `users` table where the `gender` is `'female'`.

```SQL
SELECT SUM(salary) FROM employees WHERE department = 'sales';
```

This calculates the sum of the `salary` column for all rows in the `employees` table where the `department` is `'sales'`.

```SQL
SELECT AVG(salary), department FROM employees GROUP BY department;
```

This calculates the average `salary` for each `department` in the `employees` table. The results are grouped by `department`.
