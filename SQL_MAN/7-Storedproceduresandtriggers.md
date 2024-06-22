# Stored Procedures

In a database, a stored procedure is a pre-compiled collection of SQL statements that can be executed multiple times with different parameters. Stored procedures can be used to improve performance, modularize code, and reduce the need to write repetitive SQL statements.

To create a stored procedure, the `CREATE PROCEDURE` command is used. For example:

```SQL
CREATE PROCEDURE update_balance (IN user_id INTEGER, IN amount DECIMAL)
BEGIN
UPDATE users SET balance = balance + amount WHERE id = user_id;
END;
```

This creates a stored procedure called `update_balance` that takes two parameters: `user_id` and `amount`. The stored procedure updates the `balance` column of the `users` table by adding the `amount` to the current balance where the `id` is equal to the `user_id` parameter.

To execute a stored procedure, the `CALL` command is used. For example:

```SQL
CALL update_balance(1, 100.00);
```

This executes the `update_balance` stored procedure with the values `1` and `100.00` for the `user_id` and `amount` parameters, respectively.

# Triggers

In a database, a trigger is a set of SQL statements that are automatically executed in response to a specified event, such as the insertion, deletion, or update of a row in a table. Triggers can be used to enforce data integrity, audit data changes, and automate tasks.

To create a trigger, the `CREATE TRIGGER` command is used. For example:

```SQL
CREATE TRIGGER update_timestamp
AFTER UPDATE ON users
FOR EACH ROW
BEGIN
UPDATE users SET updated_at = CURRENT_TIMESTAMP WHERE id = NEW.id;
END;
```

This creates a trigger called `update_timestamp` that is executed after an `UPDATE` event on the `users` table. The trigger updates the `updated_at` column of the `users` table with the current timestamp for the row being updated. The `NEW` keyword refers to the new values of the row after the update.

Triggers can be defined to execute before or after an event, and can be defined for each row or for the entire table. Triggers can also be disabled or dropped using the `DISABLE TRIGGER` and `DROP TRIGGER` commands.
