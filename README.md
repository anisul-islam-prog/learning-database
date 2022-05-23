# Database Notes

### What is database?

A database is a structured collection of information or data that is often kept electronically in a computer system. A database management system is generally in charge of a database (DBMS). The data and the DBMS, as well as the applications that are linked with them, are together referred to as a database system, which is frequently abbreviated to just database.

### What is a query?

A query can be a request for data results from your database, or it might be a request for action on the data, or it can be both. A query can answer a basic question, conduct computations, aggregate data from many tables, and add, edit, or delete information from a database. It is also known as ***SQL Statement***. Following is an example of a query:
```
SELECT name
FROM users
WHERE role='manager';
```
In the above example, the `SELECT name`, `FROM users` and `WHERE role='manager'` are clauses. `name` is identifier i.e. the column name. Instead of `name`, you can use `*`(*wildcard*) which means the query should return all columns of the queried tables. `users` is the name of the table from where data is being selected.`WHERE role='manager'` is a condition. Here, `WHERE` is a keyword, `role` is a column in the table and it should match the expression `'manager'` for each rows.

Try running the example and changing the condition to `employee` in this [db fiddle](https://www.db-fiddle.com/f/ogAiTgZPjwvDxwVHiVK3Ek/0)


There are various types of queries because queries are so versatile, and you would build one dependent on the task.
| Major query types | Use |
|-------------------|-----|
|Select|To retrieve data from a table or make calculations.|
|Action|Add, change, or delete data. Each task has a specific type of action query.|

### What is a declarative programming language?

A declarative programming language is one example. Expressions do not explicitly describe computations, but rather convey the form of the outcome of some operation. It is the database system's query interpreter's responsibility to develop and execute a computing procedure to produce such a result.

### What is a Relational Database (RDBMS)?

A relational database is a form of database that stores and makes data points connected to one another. Relational databases are based on the relational model, which is a simple and obvious manner of expressing data in tables. Each row in a relational database is a record with a unique ID called the key. The columns of the table carry data attributes, and each record typically includes a value for each attribute, making it simple to construct links between data points.

#### A relational database example:
Here's a simple example of two tables that a small firm may use to process product orders. The first table is a customer information table, which means that each entry contains a customer's name, address, shipping and payment information, phone number, and other contact information. Each piece of information (each attribute) is in its own column, and each row is assigned a unique ID (a key) by the database. Each entry in the second database, a customer order table, provides the ID of the customer who made the order, the product ordered, the quantity, the chosen size and color, and so on—but not the client's name or contact information.

The only thing these two tables have in common is the ID column (the key). However, because of that shared field, the relational database may establish a link between the two tables. The database can then go to the customer order table, pull the correct information about the product order, and use the customer ID from that table to look up the customer's billing and shipping information in the customer info table when the company's order processing application submits an order to the database. The warehouse can then fetch the proper product, the consumer will receive their purchase on schedule, and the corporation will be compensated.

### What is a Relational Database (DBMS)?

A database management system (or DBMS) is essentially just a computerized data storage system. Users of the system are given the ability to execute a variety of operations on it, including data manipulation and database structure maintenance.

### What is Primary key and Foreign key?

A primary key is a specific key in a relational database that works as a unique identifier for each record. It identifies each row/record in a table and its value should be unique for each row in the table. On the other hand, a foreign key is a field in one table that connects two tables.

**As for example:**

> `users` table:

| id | Name | age | gender | interest_id
|--|-----| ----| -- | --| 
|1|A|23|F|i2
|2|B|24|M|i1

> `interests` table:

|id|interests|
|-|--------------------------------------------|
|i1|{'swim', 'play', 'cheescake'}|
|i2|{'plants', 'cooking', 'cheescake'}|

In the above example, column `interest_id` (foreign key) in `users` table is connecting `interests` table.   

### What is a 