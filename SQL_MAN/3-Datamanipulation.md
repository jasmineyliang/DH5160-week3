# Data Manipulation

In a database, data manipulation refers to the process of adding, modifying, and deleting data. This is typically done using SQL commands known as Data Manipulation Language (DML).

## Inserting Data

To insert new rows into a table, the `INSERT INTO` command is used. For example:

```SQL
INSERT INTO users (username, password, created_at) VALUES ('john', 'password123', '2022-01-01');
```


This inserts a new row into the `users` table with the values `'john'`, `'password123'`, and `'2022-01-01'` for the `username`, `password`, and `created_at` columns, respectively.

## Updating Data

To modify existing data in a table, the `UPDATE` command is used. For example:

```SQL
UPDATE users SET password = 'newpassword123' WHERE username = 'john';
```


This updates the `password` column for all rows where the `username` is `'john'` to `'newpassword123'`.

## Deleting Data

To delete rows from a table, the `DELETE` command is used. For example:

```SQL
DELETE FROM users WHERE username = 'john';
```


This deletes all rows from the `users` table where the `username` is `'john'`.

## Selecting Data

To retrieve data from a table, the `SELECT` command is used. For example:

```SQL
SELECT * FROM users WHERE username = 'john';
```


This retrieves all columns and rows from the `users` table where the `username` is `'john'`. The `SELECT` command can also be used to retrieve specific columns, and to sort and filter the data using clauses such as `ORDER BY` and `WHERE`.
