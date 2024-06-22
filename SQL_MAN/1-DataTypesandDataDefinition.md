# Data Types and Data Definition

In a database, data is stored in various formats, known as data types. Some common data types include:

- `INTEGER`: A numeric data type that stores whole numbers.

- `FLOAT`: A numeric data type that stores decimal numbers.

- `VARCHAR`: A character data type that stores a variable number of characters.

- `DATE`: A data type that stores date and time values.

Data definition is the process of creating and modifying the structure of a database. This includes defining the data types and other properties of the data that will be stored in the database.

## Creating a Table

To create a table in a database, the `CREATE TABLE` command is used. For example:

```SQL
CREATE TABLE users (
id INTEGER PRIMARY KEY,
username VARCHAR(255) NOT NULL,
password VARCHAR(255) NOT NULL,
created_at DATE NOT NULL
);
```

This creates a table called `users` with four columns: `id`, `username`, `password`, and `created_at`. The data type for each column is specified, as well as any additional properties such as `PRIMARY KEY` or `NOT NULL`.

## Modifying a Table

To modify an existing table, the `ALTER TABLE` command is used. For example:

```SQL
ALTER TABLE users ADD email VARCHAR(255);
```

This adds a new column called `email` to the `users` table.

## Data Constraints

Data constraints are rules that are applied to the data in a table to ensure data integrity. Some common data constraints include:

- `NOT NULL`: This constraint ensures that a column cannot contain a `NULL` value.

- `UNIQUE`: This constraint ensures that all values in a column are unique.

- `PRIMARY KEY`: This constraint defines a column as the primary key for a table. The primary key is a unique identifier for each row in the table.

- `FOREIGN KEY`: This constraint defines a column as a foreign key, which is a reference to the primary key of another table. This is used to create a relationship between tables.
