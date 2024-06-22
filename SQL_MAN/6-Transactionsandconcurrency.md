# Transactions

In a database, a transaction is a group of SQL statements that are executed as a single unit. If any statement within a transaction fails, the entire transaction is rolled back and no changes are made to the database. This helps to ensure the integrity and consistency of the data.

To start a transaction, the `BEGIN TRANSACTION` command is used. For example:

```SQL
BEGIN TRANSACTION;
```

To commit a transaction, the `COMMIT` command is used. This saves the changes made during the transaction to the database. For example:

```SQL
COMMIT
```

To roll back a transaction, the `ROLLBACK` command is used. This discards any changes made during the transaction and restores the database to its previous state. For example:

```SQL
ROLLBACK
```

For example:

```SQL
BEGIN TRANSACTION;

UPDATE users SET balance = balance - 100 WHERE id = 1;
UPDATE accounts SET balance = balance + 100 WHERE id = 2;

COMMIT;
```

In this example, the `UPDATE` statements are executed as a single transaction. If either of the `UPDATE` statements fails, the entire transaction is rolled back and the balances are not modified.

# Concurrency

In a database, concurrency refers to the ability of multiple users or processes to access and modify data simultaneously. To ensure the consistency and integrity of the data, databases use locks and transactions to control concurrency.

Locks are used to prevent multiple users or processes from accessing or modifying the same data at the same time. There are several types of locks:

- `SHARED LOCK`: Allows multiple users to read a resource, but only one user can write to the resource at a time.

- `EXCLUSIVE LOCK`: Prevents any other users from accessing or modifying the resource until the lock is released.

- `INTENTION LOCK`: Indicates the intention to lock a resource at a later time.

Locks can be applied at different levels, such as at the row, page, or table level. The granularity of the lock depends on the database and the type of operation being performed.

To avoid conflicts and improve performance, it is important to use locks appropriately and to release them as soon as possible.

In addition to locks, transactions can be used to control concurrency. A transaction allows multiple SQL statements to be executed as a single unit, and ensures that the data remains consistent even if multiple users are accessing and modifying it simultaneously.

For example:

```SQL
BEGIN TRANSACTION;

UPDATE accounts SET balance = balance - 100 WHERE id = 1;
UPDATE users SET balance = balance + 100 WHERE id = 2;

COMMIT;
```


In this example, the `UPDATE` statements are executed as a single transaction. If either of the `UPDATE` statements fails, the entire transaction is rolled back and the balances are not modified.

```SQL
SELECT * FROM accounts WHERE id = 1 FOR UPDATE;
```

In this example, a `SELECT` statement is executed with a `FOR UPDATE` clause. This places a lock on the rows being selected, and prevents any other users from modifying them until the lock is released.

```SQL
SELECT * FROM accounts WHERE id = 1 FOR SHARE;
```
