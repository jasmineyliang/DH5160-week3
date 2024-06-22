# Subqueries

In SQL, a subquery is a query that is nested within another query. Subqueries are used to retrieve data from multiple tables or to perform calculations within a query.

For example:

```SQL
SELECT * FROM users WHERE id IN (SELECT user_id FROM orders WHERE status = 'shipped');
```

This retrieves all rows from the `users` table where the `id` is in a list of `user_id` values from the `orders` table where the `status` is `'shipped'`.

```SQL
SELECT AVG(age) FROM users WHERE age > (SELECT AVG(age) FROM users);
```

This calculates the average `age` of all rows in the `users` table where the `age` is greater than the average `age` of all rows in the `users` table.

# Joins

In SQL, a join is used to combine rows from two or more tables based on a common column. There are several types of joins:

- `INNER JOIN`: Returns rows that have matching values in both tables.

- `LEFT JOIN`: Returns all rows from the left table, and any matching rows from the right table.

- `RIGHT JOIN`: Returns all rows from the right table, and any matching rows from the left table.

- `FULL OUTER JOIN`: Returns all rows from both tables, whether or not there is a match in the other table.

For example:

```SQL
SELECT * FROM users INNER JOIN orders ON users.id = orders.user_id;
```

This retrieves all rows from the `users` and `orders` tables where the `id` from the `users` table matches the `user_id` from the `orders` table.

```SQL
SELECT * FROM users LEFT JOIN orders ON users.id = orders.user_id;
```

This retrieves all rows from the `users` table, and any matching rows from the `orders` table where the `id` from the `users` table matches the `user_id` from the `orders` table. Any rows from the `users` table that do not have a match in the `orders` table will have `NULL` values for the columns from the `orders` table.

```SQL
SELECT * FROM users RIGHT JOIN orders ON users.id = orders.user_id;
```

This retrieves all rows from the `orders
